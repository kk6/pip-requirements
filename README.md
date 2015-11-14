# snake-pit
[![CircleCI](https://img.shields.io/circleci/project/kk6/snake-pit.svg?style=flat-square)](https://circleci.com/gh/kk6/snake-pit)
[![Coverage Status](https://img.shields.io/coveralls/kk6/snake-pit.svg?style=flat-square)](https://coveralls.io/github/kk6/snake-pit?branch=master)
[![Requires.io](https://img.shields.io/requires/github/kk6/snake-pit.svg?style=flat-square)](https://requires.io/github/kk6/snake-pit/requirements/)
[![Code Climate](https://img.shields.io/codeclimate/github/kk6/snake-pit/badges/gpa.svg?style=flat-square)](https://codeclimate.com/github/kk6/snake-pit)

Depending on the installation or uninstall packages, and then edit the requirements file.

## Install snake-pit

```
$ pip install snake-pit
```

## Usage

### install

```
$ echo '#requirements.in' > requirements.in

$ pit install flask pytest
...
Successfully installed Jinja2-2.8 MarkupSafe-0.23 Werkzeug-0.11.1 flask-0.10.1 itsdangerous-0.24 py-1.4.30 pytest-2.8.2
Append the following packages in requirements.in: flask, pytest

$ cat requirements.in
#requirements.in
flask
pytest
```

### uninstall

```
$ cat requirements.in
#requirements.in
requests
nose

$ pit uninstall nose
Do you want to continue? [y/N]: y
Uninstalling nose-1.3.7:
  Successfully uninstalled nose-1.3.7
Remove the following packages from requirements.in: nose

$ cat requirements.in
#requirements.in
requests
```

## Aliases

```
$ pit i django  # install django
$ pit u django  # uninstall django
```

## Develop

### Update README

```
$ pandoc -f markdown -t rst README.md > README.rst
```

## License
MIT
