# TOP API

This repository contains the OpenAPI 3 specification of the TOP framework. The schema file is located at [schemas/top-api.yaml](schemas/top-api.yaml)

[![Node.js Package](https://github.com/Onto-Med/top-api/actions/workflows/npm-publish.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/npm-publish.yml)
[![Maven Package](https://github.com/Onto-Med/top-api/actions/workflows/maven-publish.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/maven-publish.yml)

## Development

We recommend to use a [Visual Studie Code](https://code.visualstudio.com) [devcontainer](https://code.visualstudio.com/docs/remote/containers) to modify the specification file.
The container has the [OpenAPI (Swagger) Editor](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi) extension preinstalled.

Creating a release will automaticaly build and publish a new Spring Boot skeleton package, generated with [https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator-maven-plugin](openapi-generator-maven-plugin).
Please update the version number in the [pom.xml](pom.xml) file before drafting a new release.

## Spring Boot Skeleton

Usage of the skeleton in your Spring Boot application:

1. Add maven dependency
```xml
<dependency>
  <groupId>de.uni_leipzig.imise.top</groupId>
  <artifactId>top-api</artifactId>
  <version><!-- the version number --></version>
</dependency>
```
2. Add annotation `@ComponentScan("de.uni_leipzig.imise.top.backend")` to your application class.
3. Create implementations for the delegate interfaces in `de.uni_leipzig.imise.top.backend.api` (e.g., `CodeSystemApiDelegate`).
