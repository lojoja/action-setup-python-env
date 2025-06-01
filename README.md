# action-setup-python-env

A composite action that sets up python, poetry/uv, caching, and installs project dependencies.

This repository is not meant to be referenced in third-party workflows; please fork the repository if you would like to use it in your project.

## Inputs

| Name              | Description                                       | Default |
| ----------------- | ------------------------------------------------- | ------- |
| cache             | Whether to cache project dependencies.            | "true"  |
| package_manager   | The package manager to use ("poetry" or "uv").    | "uv"    |
| python_version    | The python version to use in SemVer range syntax. | "3.13"  |
| working_directory | The working directory for the action.             | "."     |

## Outputs

| Name           | Description                  |
| -------------- | ---------------------------- |
| python_version | The installed python version |

## Examples

### Poetry

```
jobs:
  python:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-setup-python-env@main
        with:
          cache: "true"
          package_manager: poetry
          python_version: "3.13"
```

### UV

```
jobs:
  python:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-setup-python-env@main
        with:
          cache: "true"
          package_manager: uv
          python_version: "3.13"
```

## License

action-setup-python-env is released under the [MIT License](./LICENSE)
