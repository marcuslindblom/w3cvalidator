# The Nu Html Checker

Quickly and easily check document-conformance to catch unintended mistakes

A simple example:

```yml
on:
  deployment_status

jobs:
  conformance:
    name: Check document-conformance
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
        with:
          repository: marcuslindblom/w3cvalidator
      - uses: marcuslindblom/w3cvalidator@main
        with:
          url: ${{ secrets.URL }}
          level: error
```

Example output:
