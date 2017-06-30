jenkins_badges
================
A teeny tiny flask server that provides badge images based on data from jenkins

Supported Badges
----------------
- coverage, e.g 
.. image:: https://img.shields.io/badge/coverage-82.75%25-brightgreen.svg?maxAge=30


Requirements
-------------
- Jenkins with cobertura plugin
- requests
- flask

Installation
-------------

jenkins_badges can be installed via pip::

  pip install jenkins_badges


Quickstart
-----------
jenkins_badges can be run in an interpreter:

.. code:: python

 import jenkins_badges
 app = jenkins_badges.create_app()
 app.run()

it can also be placed inside a wsgi file:

.. code:: python

  #exampleapp.wsgi
  
  import os
  os.environ['JENKINS_BADGES_SETTINGS'] = '/home/ubuntu/.jenkins_badges'
  from jenkins_badges import create_app
  application = create_app()
  




