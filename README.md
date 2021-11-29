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
  <groupId>care.smith.top</groupId>
  <artifactId>top-api</artifactId>
  <version><!-- the version number --></version>
</dependency>
```
2. Add annotation `@ComponentScan("care.smith.top.backend")` to your application class.
3. Create implementations for the delegate interfaces in `de.uni_leipzig.imise.top.backend.api` (e.g., `CodeSystemApiDelegate`).

## Typescript Axios

1. Add the file .npmrc to the project folder, with the following content:
```properties
@onto-med:registry=https://npm.pkg.github.com
```
2. Authenticate at GitHub Packages registry (you will be prompted for username and password aka. personal access token):
```sh
npm login --scope=@onto-med --registry=https://npm.pkg.github.com
```
3. Add `@onto-med/top-api` as dependency, e.g.:
```sh
yarn add @onto-med/top-api
```
