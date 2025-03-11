# action-setup-python-env

A composite action that sets up python, poetry, caching, and installs project dependencies.

This repository is not meant to be referenced in third-party workflows; please fork the repository if you would like to use it in your project.

```
- uses: lojoja/action-setup-python-env@main
  with:
    python-version: ""
```

See [actions/setup-python](https://github.com/actions/setup-python/blob/main/README.md) for possible `python-version` values.

## License

action-setup-python-env is released under the [MIT License](./LICENSE)
