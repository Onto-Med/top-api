# TOP API

This repository contains the OpenAPI 3 specification of the TOP framework. The schema file is located at [schemas/top-api.yaml](schemas/top-api.yaml)

[![Publish snapshots](https://github.com/Onto-Med/top-api/actions/workflows/publish-snapshots.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/publish-snapshots.yml)
[![Publish packages and create release](https://github.com/Onto-Med/top-api/actions/workflows/release.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/release.yml)
[![Swagger UI](https://img.shields.io/badge/-Swagger%20UI-%23Clojure?style=flat&logo=swagger&logoColor=white)](https://onto-med.github.io/top-api/)

## Usage

### Spring Boot Skeleton

1. Add maven dependency
    ```xml
    <dependency>
      <groupId>care.smith.top</groupId>
      <artifactId>top-api</artifactId>
      <version><!-- the version number --></version>
    </dependency>
    ```
2. Add annotation `@ComponentScan("care.smith.top.backend")` to your application class.
3. Create implementations for the delegate interfaces in `care.smith.top.backend.api` (e.g., `EntityApiDelegate`).

### Typescript Axios

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

## Versioning

There will always be a snapshot version available with latest changes pushed to the main branch. Snapshots have a **higher** version number than the latest release.

## Development

We recommend to use a [Visual Studie Code](https://code.visualstudio.com) [devcontainer](https://code.visualstudio.com/docs/remote/containers) to modify the specification file.
The container has the [OpenAPI (Swagger) Editor](https://marketplace.visualstudio.com/items?itemName=42Crunch.vscode-openapi) extension preinstalled.

### Format Schema File

You can use the npm package [openapi-format](https://www.npmjs.com/package/openapi-format) to automatically format the OpenApi schema file.

```
npx openapi-format schemas/top-api.yml --output schemas/top-api.yml
```

### Releases

Create new releases via GitHub Workflow [publish-snapshots.yml](.github/workflows/publish-snapshots.yml). Doing so will automatically build and publish a new Spring Boot skeleton and typescript-axios package, generated with [openapi-generator-maven-plugin](https://github.com/OpenAPITools/openapi-generator/tree/master/modules/openapi-generator-maven-plugin).

## License

The code in this repository and the packages `care.smith.top:top-api` and `@onto-med/top-api` are licensed under [GPL-3.0](LICENSE).
