Google App Engine Pipeline API with Mutlitenancy Support
========================================================

*Forked from http://code.google.com/p/appengine-pipeline/*

Installation
------------

***WARNING*** This version is incomplete and not stable.

### Add the pipeline library to your app.yaml

To use the library, add it to your list of handlers at the top. The login access to these handlers should not be admin or login restricted. That behavior is enforced by the pipeline library itself.

```yaml
application: pipeline-test
version: 1
runtime: python27
api_version: 1
threadsafe: true

handlers:
- url: /_ah/pipeline(/.*)?
  script: pipeline.handlers._APP
# Your handlers follow
```

### Unit testing

UnitTests can be run with [py.test](http://pytest.org/latest/).

```zsh
$ py.test --cov=pysucker --cov-report=html -n=4
```

Usage
-----

See [Getting started with the Google App Engine Pipeline API ](https://code.google.com/p/appengine-pipeline/wiki/GettingStarted).
