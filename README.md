# Setup VSCode for development

- Install VSCode `$ brew install --cask visual-studio-code`
- Install VSCode [Python Extention](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
- Install black, isort, and pylint
```shell
$ pip3 install black
$ pip3 install isort
$ pip3 install pylint
```
- Open VSCode settings.json and paste this
```json
{
  "python.formatting.provider": "black",
  "python.linting.pylintEnabled": true,
  "python.linting.pylintArgs": [
    "--enable=W0614",
    "--disable=c,broad-except,attribute-defined-outside-init"
  ],
  "[python]": {
    "editor.codeActionsOnSave": {
      "source.organizeImports": true,
      "source.organizeImports.python": true
    },
    "editor.formatOnSave": true
  },
  "python.sortImports.args": [
    "--profile",
    "black"
  ]
}
```
- Always use [virtual environment](https://docs.python.org/3/library/venv.html)

