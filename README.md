# TypeHub Fusio Push

This GitHub action allows you to push the API specification of a [Fusio](https://www.fusio-project.org/)
instance to the [TypeHub](https://typehub.cloud/) platform.

## Inputs

## `document`

The target TypeHub document name.

## `client_id`

**Required** The TypeHub client id, this is either your username or an app key.

## `client_secret`

**Required** The TypeHub client secret, this is either your password or an app secret.

## `filter`

Optional an API filter

## Example usage

```yaml
name: TypeHub
on:
  - pull_request
  - push
jobs:
  push:
    runs-on: ubuntu-latest
    steps:
      - name: Push
        uses: apioo/typehub-fusio-action@v0.1.0
        with:
          document: sdk
          client-id: ${{ secrets.TYPEHUB_CLIENT_ID }}
          client-secret: ${{ secrets.TYPEHUB_CLIENT_SECRET }}
          filter: app
```
