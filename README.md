# Update World
Github action to update a helix world


```yaml

name: Update World

on:
  push:
    branches:
      - main

jobs:
  update-package:
    runs-on: ubuntu-latest

    steps:
      - name: Use update world action 
        uses: hypersonic-laboratories/update-world@main
        with:
          # Note: Config.toml will override any other definitions from this action!
          config_toml_path: "Config.toml"
          access_token: ${{ secrets.ACCESS_TOKEN }}
          packages : '{"debug-qa": "latest"}' 
          world_name : 'cybergrind'

``
