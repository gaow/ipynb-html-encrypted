# Sharing private Jupyter notebooks

Convert a Jupyter notebook to encrypted HTML file for sharing with private parties

## Objective

This script converts a Jupyter notebook to HTML file using a template provided by the `SoS` software program,
and encrypt it using `StatiCrypt`.

## Requirements

You need to install

- SoS
- Docker

## Usage

```
./encrypt.sos -h

Global Workflow Options:
  --notebook . (as path)
                        Path to notebook or markdown file (required)
  --password ''
                        Set password. If unspecified a random password will be generated, reported and used.
  --tpl . (as path)
                        Path to login page template
  --title 'staticrypt protected page'
                        Login page title
  --outdir ''
                        Path to output file directory

Sections
  default_1:            Generate plain HTML
  default_2:            Encypt HTML
```

### Default template

```
./encrypt.sos --notebook test_page.ipynb
```

### Customized title and template

```
./encrypt.sos --notebook test_page.ipynb --tpl password_template_chs.html --title "样例文档"
```

### Markdown input support

Markdown files can also be used as input, eg,

```
./encrypt.sos --notebook README.md
```

## Choice of password

I suggest using default random passwords. You should see a password generated and printed on the screen, something like

```
	Password set to: <a random string>
```

then keep a record of this randomly generated password for sharing with authorized readers.

Alternatively you can use `--password` option to the `./encrypt.sos` command if you want to use a specified password.
