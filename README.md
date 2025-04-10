# setup-go-package #

[![GitHub Build Status](https://github.com/cisagov/setup-go-package/workflows/build/badge.svg)](https://github.com/cisagov/setup-go-package/actions)

A [GitHub composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action)
to install a given Go package with the specified version/tag.

## Usage ##

### Inputs ###

| Name | Description | Interpreted Type | Default | Required |
|------|-------------|------------------|---------|:--------:|
| source | The source for the Go package to install. | `string` | n/a | yes |
| version | The version or tag to use for the Go package. | `string` | n/a | yes |

### Outputs ###

None.
<!--
| Name | Description | Output Type |
|------|-------------|-------------|
| output_name | The output's description. | `output_type` |
-->

### Sample GitHub Actions workflow ###

```yml
---
name: The workflow

on:
  pull_request:
  push:

jobs:
  my_job:
    # This job does not need any permissions
    permissions: {}
    runs-on: ubuntu-latest
    steps:
      - name: Install terraform-docs
        uses: cisagov/setup-go-package@e7d5a7d8c497f15addbc13c54c8cb6f3822ed2d5 # v1.0.0
        with:
          source: github.com/terraform-docs/terraform-docs
          version: "1.2.3"
```

## Contributing ##

We welcome contributions!  Please see [`CONTRIBUTING.md`](CONTRIBUTING.md) for
details.

## License ##

This project is in the worldwide [public domain](LICENSE).

This project is in the public domain within the United States, and
copyright and related rights in the work worldwide are waived through
the [CC0 1.0 Universal public domain
dedication](https://creativecommons.org/publicdomain/zero/1.0/).

All contributions to this project will be released under the CC0
dedication. By submitting a pull request, you are agreeing to comply
with this waiver of copyright interest.
