# Python Package Setup Guidelines

- Setup local environment
```bash 
python3 -m venv env
source env/bin/activate
pip install setuptools wheel twine
```

- Setup `setup.py` file
```python
from setuptools import setup, find_packages

setup(
    name='PACKAGE_NAME',
    version='0.1',
    packages=find_packages(),
    include_package_data=True,
    license='MIT',
    description='PROJECT_DESCRIPTION',
    long_description=open('README.md').read(),
    long_description_content_type='text/markdown',
    url='GITHUB_URL',
    author='NAME',
    author_email='AUTHOR_EMAIL',
    classifiers=[
        'Environment :: Web Environment',
        'Framework :: Django',
        'Framework :: Django :: 3.2',
        'Intended Audience :: Developers',
        'License :: OSI Approved :: MIT License',
        'Operating System :: OS Independent',
        'Programming Language :: Python',
        'Programming Language :: Python :: 3',
        'Programming Language :: Python :: 3.6',
        'Programming Language :: Python :: 3.7',
        'Programming Language :: Python :: 3.8',
        'Topic :: Internet :: WWW/HTTP',
        'Topic :: Internet :: WWW/HTTP :: Dynamic Content',
    ],
)
```

## Local installation for local environment
```bash
pip install -e .
```

## Upload to PyPi
```bash
python setup.py sdist bdist_wheel
twine upload dist/*
```

