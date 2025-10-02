# singlefile-click-app cookiecutter template

Cookiecutter template for creating new [Click](https://click.palletsprojects.com/) command-line tools.

Use this template on your own machine with cookiecutter, or create a brand new repository based on this template entirely through the GitHub web interface using [click-app-template-repository](https://github.com/simonw/click-app-template-repository).

## Installation

I recommend just using `uvx` to use this template. (The rest of this README assumes you do).

Or, you can install cookiecutter using `pipx` or `pip`.

## Example

An example of a tool that was initially created using this template:

- [aws-token-updater](https://github.com/hmrd-forpeople/aws-token-updater): A comand-line utility for updating AWS tokens from kion

## Usage

Run `uvx cookiecutter gh:hmrd-forpeople/singlefile-click-app` and then answer the prompts. Here's an example run:
```
$ uvx cookiecutter gh:hmrd-forpeople/singlefile-click-app
app_name []: click app template demo
description []: Demonstrating https://github.com/hmrd-forpeople/singlefile-click-app
hyphenated [click-app-template-demo]:
underscored [click_app_template_demo]:
github_username []: hmrd-forpeople
author_name []: Nicholas Hurley
```
I strongly recommend accepting the suggested value for "hyphenated" and "underscored" by hitting enter on those prompts.

This will create a directory called `click-app-template-demo` - the tool name you enter is converted to lowercase and uses hyphens instead of spaces.

## Developing your command-line tool

Having created the new structure from the template, here's how to start working on the tool.

If your tool is called `my-new-tool`, you can start working on it like so:
```bash
cd my-new-tool
# Create and activate a virtual environment:
uv sync
# Confirm your tool can be run from the command-line
uv run my-new-tool --version
# If you already have this as a git repository, install pre-commit hooks
uv run pre-commit install --install-hooks
```
You should see the following:
```bash
my-new-tool, version 0.1
```
You can run the default test for your tool like so:
```bash
uv run python -m pytest
```
This will execute the test in `tests/test_my_new_tool.py`.

Now you can open the `my_new_tool/cli.py` file and start adding Click [commands and groups](https://click.palletsprojects.com/en/7.x/commands/).

## Creating a Git repository for your tool

You can initialize a Git repository for your tool like this:
```bash
cd my-new-tool
git init
# If you haven't already, initialize the pre-commit hooks
uv run pre-commit install --install-hooks
# Otherwise, you can just carry on from here
git add .
git commit -m "Initial structure from template"
```
## Publishing your tool to GitHub

Use https://github.com/new to create a new GitHub repository sharing the same name as your tool, which should be something like `my-new-tool`.

Push your `main` branch to GitHub like this:
```bash
git remote add origin git@github.com:YOURNAME/my-new-tool.git
git push -u origin main
```
The template will have created a GitHub Action which runs your tool's test suite against every commit.
