# TOP API

This repository contains the OpenAPI 3 specification of the TOP framework.
Please see [top-deployment](https://onto-med.github.io/top-deployment) for an onverall description of the framework.
The schema file is located at [schemas/top-api.yaml](schemas/top-api.yaml)

[![DOI](https://zenodo.org/badge/429797878.svg)](https://zenodo.org/badge/latestdoi/429797878)
[![Swagger UI](https://img.shields.io/badge/-Swagger%20UI-%23Clojure?style=flat&logo=swagger&logoColor=white)](https://onto-med.github.io/top-api/)

[![Publish snapshots](https://github.com/Onto-Med/top-api/actions/workflows/publish-snapshots.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/publish-snapshots.yml)
[![Publish packages and create release](https://github.com/Onto-Med/top-api/actions/workflows/release.yml/badge.svg)](https://github.com/Onto-Med/top-api/actions/workflows/release.yml)

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

Because the Maven package is hosted at [GitHub Packages](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry),
you need to make some modifications to your Maven installation in order to download and install the package. Please follow the [Authenticating to GitHub Packages](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry#authenticating-to-github-packages) instructions.

### Typescript Axios

1. Add the file .npmrc to the project folder, with the following content:
    ```properties
    @onto-med:registry=https://npm.pkg.github.com
    ```
2. Authenticate to [GitHub Packages](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry)
  (you will be prompted for username and password aka. personal access token, see [Authenticating to GitHub Packages](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry#authenticating-to-github-packages)):
    ```sh
    npm login --scope=@onto-med --registry=https://npm.pkg.github.com
    ```
3. Add `@onto-med/top-api` as dependency, e.g.:
    ```sh
    yarn add @onto-med/top-api
    ```

## Contribution and Development

Please see our [Contributing Guide](https://github.com/Onto-Med/top-api/blob/main/CONTRIBUTING.md).

## License

The code in this repository and the packages `care.smith.top:top-api` and `@onto-med/top-api` are licensed under [MIT](LICENSE).
