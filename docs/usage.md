To use this action, make a file `.github/workflows/docker-template.yml`. Here's a template to get started:

```yaml
name: action-docker-template

on:
  pull_request:
  push:
    branches: [main]

jobs:
  confluence:
    runs-on: ubuntu-20.04
    steps:
      - name: Check out a copy of the repo
        if: ${{ !env.ACT }}
        uses: actions/checkout@v2
        with:
          fetch-depth: 0

      - name: action-docker-template
        uses: hadenlabs/action-docker-template@0.0.0
        with:
          args: ''
```
