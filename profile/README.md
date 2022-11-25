# PYNOSAUR

# PyPi Instructions

### Ubuntu

1. Create a virtual environment for the project
``` 
python3 -m venv venv
```

2. Activate your environment
```
. venv/bin/activate
```

3. Upgrade pip/Make sure pip is up to date
``` 
python3 -m pip install --upgrade pip
```

4. Configure the TOML file
```
[build-system]
requires = ["setuptools>=61.0"]
build-backend = "setuptools.build_meta"
[project]
name = "PROJECT NAME"
version = "0.0.0"
authors = [
  { name="AUTHOR'S NAME", email="AUTHOR'S EMAIL" },
]
maintainers = [
    { name="MAINTAINER'S NAME", email="MAINTAINER'S EMAIL" },
]
description = "SHORT DESCRIPTION"
readme = "README.md"
requires-python = ">=3.10"
classifiers = [
    "Programming Language :: Python :: 3",
    "License :: OSI Approved :: MIT License",
    "Operating System :: OS Independent",
]

[project.urls]
"Homepage" = "HTTPS HOMEPAGE ADDRESS URL"
"Bug Tracker" = "HTTPS BUG TRACKER PAGE URL"
```

5. Upgrade/Make sure build module is up to date
```
python3 -m pip install --upgrade build
```

6. Build the project
```
python3 -m build
```
Note: Two files should be generated in the dist directory.
```
dist/
├── PACKAGE_NAME-0.0.0-py3-none-any.whl
└── PACKAGE_NAME-0.0.0.tar.gz
```

7. Upload the files to Pypi
```
python3 -m pip install --upgrade twine
python3 -m twine upload --repository testpypi dist/*
```
