# TypeHub-Fusio-Action

You can use this GitHub action at your Fusio project to automatically push your
API specification to TypeHub. The following example shows you can use the action:

```yaml
name: TypeHub
on:
  - pull_request
  - push
jobs:
  app:
    name: App
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
