# Purpose
Read JSON property from a file and use the property in a github action

# Usage
``` yaml
jobs:
  get-json-value:
    uses: fiddlermikey/json-property-to-action-variable/action.yml@main
    with:
      json-ID: "name" # JSON property to lookup
      json-path: "integration-manifest.json" # JSON file to use
  output-read-value:
    runs-on: ubuntu-latest
    needs: get-json-value
    steps:
 ```
