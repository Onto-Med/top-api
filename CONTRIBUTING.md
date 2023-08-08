# Contributing Guide

Thank you for investing your time in contributing to our project!

Read our [Code of Conduct](./CODE_OF_CONDUCT.md) to keep our community approachable and respectable.

## Issues and Support

If you find a problem or have a question about the content in this repository and how to use it, please create an issue in the [Issues Tracker](https://github.com/Onto-Med/top-api/issues).
Make sure you describe the problem as clearly as possible.

## Workflow to Make Contributions

We are very happy about contributions!

The TOP API is automatically generated from the OpenAPI schema specification located in [schemas/top-api.yml](https://github.com/Onto-Med/top-api/blob/main/schemas/top-api.yml).
If you want to contribute changes to the API, please do so by:

1. cloning this repository (forking for external contributors)
2. creating a new feature branch
3. applying your changes
4. formatting the OpenAPI schema file with the npm package [openapi-format](https://www.npmjs.com/package/openapi-format) by calling:

        npx openapi-format schemas/top-api.yml --output schemas/top-api.yml

5. committing and pushing all changes
6. creating a [pull request](https://github.com/Onto-Med/top-api/pulls)
