# Auto

[![Build Status](https://travis-ci.org/google/auto.svg?branch=master)](https://travis-ci.org/google/auto)

A collection of source code generators for [Java][java].

## This fork (frankbenoit)

This fork adds modification to the auto-factory that I need for Eclipse based projects.
1. The APT argument `-AnullAnnotations=JDT`. This causes that generated factories are annotated with `@NonNullByDefault`, and take care about arguments having `@Nullable`.
Fixing [#881](https://github.com/google/auto/issues/881)
2. The maven build generates a `-annotations.jar` for the project dependency
3. The maven build generates a `-jar-with-dependencies.jar` to have a single jar to configure in the Eclipse settings (.factorypath).
Fixing [890](https://github.com/google/auto/issues/890)

## Auto‽

[Java][java] is full of code that is mechanical, repetitive, typically untested
and sometimes the source of subtle bugs. _Sounds like a job for robots!_

The Auto subprojects are a collection of code generators that automate those
types of tasks. They create the code you would have written, but without
the bugs.

Save time.  Save code.  Save sanity.

## Subprojects

  * [AutoFactory] - JSR-330-compatible factories

    [![Maven Central](https://img.shields.io/maven-central/v/com.google.auto.factory/auto-factory.svg)](https://mvnrepository.com/artifact/com.google.auto.factory/auto-factory)

  * [AutoService] - Provider-configuration files for [`ServiceLoader`]

    [![Maven Central](https://img.shields.io/maven-central/v/com.google.auto.service/auto-service.svg)](https://mvnrepository.com/artifact/com.google.auto.service/auto-service)

  * [AutoValue] - Immutable [value-type] code generation for Java 7+.

    [![Maven Central](https://img.shields.io/maven-central/v/com.google.auto.value/auto-value.svg)](https://mvnrepository.com/artifact/com.google.auto.value/auto-value)

  * [Common] - Helper utilities for writing annotation processors.

    [![Maven Central](https://img.shields.io/maven-central/v/com.google.auto/auto-common.svg)](https://mvnrepository.com/artifact/com.google.auto/auto-common)

## License

    Copyright 2013 Google LLC

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[AutoFactory]: https://github.com/google/auto/tree/master/factory
[AutoService]: https://github.com/google/auto/tree/master/service
[AutoValue]: https://github.com/google/auto/tree/master/value
[Common]: https://github.com/google/auto/tree/master/common

[java]: https://en.wikipedia.org/wiki/Java_(programming_language)
[value-type]: http://en.wikipedia.org/wiki/Value_object
[`ServiceLoader`]: http://docs.oracle.com/javase/7/docs/api/java/util/ServiceLoader.html
