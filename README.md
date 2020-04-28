# Ask Schools

[
![PyPI](https://img.shields.io/pypi/v/sp_ask_report_chats_per_school.svg)
![PyPI](https://img.shields.io/pypi/pyversions/sp_ask_report_chats_per_school.svg)
![PyPI](https://img.shields.io/github/license/guinslym/sp_ask_report_chats_per_school.svg)
](https://pypi.org/project/sp_ask_report_chats_per_school/)
[![TravisCI](https://travis-ci.org/guinslym/sp_ask_report_chats_per_school.svg?branch=master)](https://travis-ci.org/guinslym/sp_ask_report_chats_per_school)


This package helps to filter Chats


## Installation

**Ask Schools** can be installed from PyPI using `pip` or your package manager of choice:

```
pip install sp_ask_report_chats_per_school
```

## Requirement

lh3api is a requirement for this package[ lh3api configuation files](https://gitlab.com/libraryh3lp/libraryh3lp-sdk-python/) need to be installed first.


In ~/.lh3/config::

    [default]
    server = libraryh3lp.com
    timezone = UTC
    salt = "you should probably change this"

The `salt` is used when generating system-level utility accounts.
This is not something you do often.  If your `salt` is unique, your
passwords will be unique.

In ~/.lh3/credentials::

    [default]
    username = <ADMIN_USER>
    password = <ADMIN_PASS>

    [test]
    username = <TEST_USER>
    password = <TEST_PASS>


## Usage


Example:

```python

from sp_ask_report_chats_per_school import get_nbr_of_chats_per_school_for_this_day

chats_DataFrame = get_nbr_of_chats_per_school_for_this_day(year=2020, month=3, day=11)
chats_DataFrame.to_excel("chats_per_school.xlsx", index=True)
# see mockup image below
```
<p float="left">
<img src="images/mockup.png" width="300"/>
</p>
## Code of Conduct

Everyone interacting in the project's codebases, issue trackers, chat rooms, and mailing lists is expected to follow the [PyPA Code of Conduct](https://www.pypa.io/en/latest/code-of-conduct/).

## Todo

1.  Add tests
2.  ~~Add column for Date~~
3.  Add Makefile
4.  ~~Add pypi~~
5.  ~~Create python package~~
6.  ~~Add screenshot to Readme.md~~
7.  Create a README.rst for pypi