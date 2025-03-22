# TinyRadius-Netty

[![Gradle Build](https://github.com/globalreachtech/tinyradius-netty/actions/workflows/gradle.yml/badge.svg)](https://github.com/globalreachtech/tinyradius-netty/actions/workflows/gradle.yml)
[![Maintainability](https://api.codeclimate.com/v1/badges/a6b90f85717d753228eb/maintainability)](https://codeclimate.com/github/globalreachtech/tinyradius-netty/maintainability)
[![Coveralls](https://coveralls.io/repos/github/globalreachtech/tinyradius-netty/badge.svg?branch=master)](https://coveralls.io/github/globalreachtech/tinyradius-netty?branch=master)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=globalreachtech_tinyradius-netty&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=globalreachtech_tinyradius-netty)
[![Known Vulnerabilities](https://snyk.io/test/github/globalreachtech/tinyradius-netty/badge.svg)](https://snyk.io/test/github/globalreachtech/tinyradius-netty)

[![Maven Central](https://img.shields.io/maven-central/v/com.globalreachtech/tinyradius-netty)](https://search.maven.org/artifact/com.globalreachtech/tinyradius-netty)
[![javadoc](https://javadoc.io/badge2/com.globalreachtech/tinyradius-netty/javadoc.svg)](https://javadoc.io/doc/com.globalreachtech/tinyradius-netty)

TinyRadius-Netty is a Java Radius library, loosely based off the TinyRadius Radius library, rebuilt with Java 8 and Netty patterns/features.

## Features
- Sends/receives Radius packets
- Signs and verifies Request Authenticator for Access and Accounting requests/responses
- Supports verifying and encoding for PAP, CHAP, and EAP (Message-Authenticator)
- Attach arbitrary attributes to packets
- Loads dictionaries recursively from file system or classpath (Radiator/FreeRadius format)

### Improvements over TinyRadius
- Netty for async IO, timeouts, thread management
- Handlers follow Netty's interceptor filter pattern, blocking calls use promises
- log4j2 instead of commons-logging
- Java 6-11 features (generics, NIO, lambdas, streams)
- Packets and Attributes are fully immutable
- 80%+ test coverage
- Proxy no longer a separate implementation, but a promise-based adapter between the client and server classes

## Usage

See the [e2e tests](src/test/java/org/tinyradius/e2e/EndToEndTest.java) on usage as Client/Server/Proxy.

## Maintainers

- Ensure you have user tokens for [Central Portal](https://central.sonatype.org/publish-ea/publish-ea-guide/) instead of
  legacy OSSRH
- [Set up GPG](https://central.sonatype.org/publish/requirements/gpg/) for artifact signing
- [Publish locally](https://jreleaser.org/guide/latest/examples/maven/staging-artifacts.html#_gradle) and confirm
  artifacts
- Use JReleaser
  following [Portal Publisher config](https://jreleaser.org/guide/latest/examples/maven/maven-central.html#_gradle)

## License
Copyright Matthias Wuttke and contributors:
- http://tinyradius.sourceforge.net/
- https://github.com/ctran/TinyRadius
- https://github.com/globalreachtech/tinyradius-netty

Licensed under LGPL 2.1
