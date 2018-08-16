# Shibboleth IdP v3: Metadata resolver extensions

[![License](http://img.shields.io/:license-mit-blue.svg)](https://opensource.org/licenses/MIT)
[![Build Status](https://travis-ci.org/mpassid/shibboleth-idp-metadata-ext.svg?branch=master)](https://travis-ci.org/mpassid/shibboleth-idp-metadata-ext)
[![Coverage Status](https://coveralls.io/repos/github/mpassid/shibboleth-idp-metadata-ext/badge.svg?branch=master)](https://coveralls.io/github/mpassid/shibboleth-idp-metadata-ext?branch=master)

## Overview

This module implements some metadata resolution extensions for [Shibboleth Identity Provider v3](https://wiki.shibboleth.net/confluence/display/IDP30/Home).

## Prerequisities and compilation

- Java 7+
- [Apache Maven 3](https://maven.apache.org/)

```
mvn package
```

After successful compilation, the _target_ directory contains _idp-profile-impl-metadata-\<version\>.jar_.

## Deployment

After compilation, the module's JAR-files must be deployed to the IdP Web
application. Depending on the IdP installation, the module deployment may be achieved for instance 
with the following sequence:

```
cp target/idp-profile-impl-metadata-<version>.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib
cd /opt/shibboleth-idp
sh bin/build.sh
```

The final command will rebuild the _war_-package for the IdP application.

TODO: configuration documentation.
