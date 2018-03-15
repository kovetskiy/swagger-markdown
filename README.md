swagger-markdown
================

[![npm][npm-image]][npm-url] [![dependencies][david-image]][david-url] [![circle ci][circleci-image]][circleci-url] [![bitHound Overall Score](https://www.bithound.io/github/syroegkin/swagger-markdown/badges/score.svg)](https://www.bithound.io/github/syroegkin/swagger-markdown)

CLI script to turn swagger yaml into markdown files.
Supports swagger 2.0 format only

see [examples](https://github.com/syroegkin/swagger-markdown/tree/master/examples) folder

### Installation

    npm install -g swagger-markdown

    sudo npm install -g 'https://github.com/kovetskiy/swagger-markdown/tarball/master'

### Usage

```
swagger-markdown [-h] [-v] -i  [-o]

Options:
  -h, --help      Show this help message and exit.
  -v, --version   Show program's version number and exit.
  -i , --input    Path to the swagger yaml file
  -o , --output   Path to the resulting md file

```

#### Example:

```javascript
swagger-markdown -i path/to/swagger/file.yaml
```
By default it will create the new file within the same directory with the same name as swagger file but with .md extension.
So, if swagger file is placed in `project/api-doc/swagger.yaml` the new file will be created as `project/api-doc/swagger.md`

You can also use it as a npm script in your package.json:

    npm i --save-dev swagger-markdown

```json
{
    "scripts": {
        "md-docs": "swagger-markdown -i path/to/swagger.yaml",
        ...
    }
}
```

    npm run md-docs

[npm-url]: https://www.npmjs.com/package/swagger-markdown
[npm-image]: https://img.shields.io/npm/v/swagger-markdown.svg

[david-url]: https://david-dm.org/syroegkin/swagger-markdown
[david-image]: https://img.shields.io/david/syroegkin/swagger-markdown.svg

[circleci-url]: https://circleci.com/gh/syroegkin/swagger-markdown/tree/master
[circleci-image]: https://img.shields.io/circleci/project/syroegkin/swagger-markdown.svg
