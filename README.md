# nonsymmetrical-narvanso

[![Linux](https://img.shields.io/badge/Linux-Ubuntu-orange?style=flat&logo=linux)](https://ubuntu.com/#developer)
[![Python](https://img.shields.io/badge/Python-3.9-blue?style=flat&logo=python)](https://www.python.org/downloads/release/python-396/)
[![linting: pylint](https://img.shields.io/badge/linting-pylint-yellowgreen)](https://github.com/PyCQA/pylint)

## About

The application will use https://pypi.org/rss/packages.xml, which will retrieve all package information once a day and index it in any full-text search system(elastic search).

The application will be created on Django, it will be a search engine that will allow searching for a package in the created index by author, author's email, package description, package title, keywords, current version, and data of the person maintaining the package (name, email). The search engine will have one input field.

After searching, the data will be presented in pagination, set in system environment variables.

In case of failure of the full-text search system, it is possible to restore it from the database(PostgreSQL).

The application uses Docker to work independently of the operating system (e.g. in Windows there are no curl or crontab commands as standard).
