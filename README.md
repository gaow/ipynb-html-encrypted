# Sharing private Jupyter notebooks

Convert ipynb to encrypted HTML file for sharing with private parties

## Objective

This script converts ipynb to HTML file using a template provided by the `SoS` software program,
and encrypt it using `StatiCrypt`.

## Requirements

You need to install

- SoS
- Docker

## Usage

### English version

```
./encrypt.sos --notebook test_page.ipynb --password Cyoa93
```

### Chinese version

```
./encrypt.sos --notebook test_page.ipynb --password Cyoa93 --tpl password_template_chs.html --title "样例文档"
```
