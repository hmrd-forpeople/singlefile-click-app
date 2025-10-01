# {{ cookiecutter.hyphenated }}

[![Changelog](https://img.shields.io/github/v/release/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}?include_prereleases&label=changelog)](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}/releases)
[![Tests](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}/actions/workflows/test.yml/badge.svg)](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}/actions/workflows/test.yml)
[![License](https://img.shields.io/badge/license-CC0%201.0-blue.svg)](https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}/blob/master/LICENSE){% endif %}

{{ cookiecutter.description }}

## Installation

Install this tool from the releases page

## Usage

For help, run:
```bash
{{ cookiecutter.hyphenated }} --help
```

## Development

To contribute to this tool, first install `uv`. See [the uv documentation](http
s://docs.astral.sh/uv/getting-started/installation/) for how.

Next, checkout the code
```bash
git clone https://github.com/{{ cookiecutter.github_username }}/{{ cookiecutter.hyphenated }}
```

Then create a new virtual environment and sync the dependencies:
```bash
cd {{ cookiecutter.hyphenated }}
uv sync
```

To run the tests:
```bash
uv run python -m pytest
```
