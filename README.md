# Purpose
Read JSON property from a file and use the property in a github action

# Usage
``` yaml
name: Get JSON Value
on: [workflow_dispatch, push]

jobs:
  get-json-value:
    uses: fiddlermikey/json-property-to-action-variable/.github/workflows/action.yml@v0.1.0
    with:
      json-ID: "name" # JSON property to lookup
      json-path: "manifest.json" # JSON file to use
  output-read-value:
    runs-on: ubuntu-latest
    needs: get-json-value
    steps:
      - run: echo ${{ needs.get-json-value.outputs.json_value}}

 ```
