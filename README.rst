=======================
Django Background Tasks – CFPB fork
=======================

This repo is a temporary fork of Django Background Task is a database-backed work queue for Django. The upstream code is loosely based around `Ruby's DelayedJob`_ library, and the Python version was adapted from lilspikey_ `django-background-task` and updated for compatibility with Django5 and Python 3.13.

.. _Ruby's DelayedJob: https://github.com/tobi/delayed_job
.. _lilspikey: https://github.com/lilspikey/

The upstream code is available on PyPI as django-background-tasks, but it hasn't been updated since 2024 and has a number of standing issues. Unfortunately a growing number of uncoordinated forks have fixed different issues at different times and resulted in conflicting database migrations. This fork is intended as a stable version that unifies the fixes and migrations, removes Python2 code and results in a package that is compatible with both Python 3.13 and Django 5. The tests in this repo run in under those specs.

Since upstream issues are no longer being addressed, we will not be pushing this version upstream as a pull request, nor will it be pushed to PyPi, where there's already too much version and fork confusion.

There are two parts to using background tasks:

- creating the task functions and registering them with the scheduler
- setup a cron task (or long running process) to execute the tasks

Tasks are implemented as functions or any other callable.


Upstream docs
====
See `Read the docs`_.

.. _Read the docs: http://django-background-tasks.readthedocs.io/en/latest/

