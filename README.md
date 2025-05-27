# VPM Cookie

An open source [cookiecutter](https://github.com/cookiecutter/cookiecutter) template for VPM packages

## File Structure

```text
cookiecutter-vpm-package/
├── cookiecutter.json
├── hooks/
|   └── pre_gen_project.py
└── {{cookiecutter.package_name}}/
    ├── package.json
    ├── README.md
    ├── LICENSE
    ├── .gitignore
    ├── Runtime/
    │   └── {{cookiecutter.namespace}}.Runtime.asmdef
    ├── Editor/
    │   └── {{cookiecutter.namespace}}.Editor.asmdef
    ├── Documentation~/
    │   └── CHANGELOG.md
    └── .github/
        └── workflows/
            └── build-package.yml
```

## Usage

### Option A Template (Recommended)

- Copy this repo as a template
- In new repository Actions > Replace Repository with Cookiecutter > Run Workflow
- Fill in fields
- Run workflow

### Option B Manual

```bash
git clone <this package>
cd <this package>
cookiecutter -o ../ . # makes package in a sibling folder

# Prompts:
# package_name: com.myname.package
# display_name: Shader FX Collection  
# version: 1.0.0
# description: Custom Avatar Addon
# author_name: myname
# unity_version: 2022.3
```

#### Manual Requirements

- cookiecutter
- python3

Template generates VPM packages with vrc-get extensions included by default (see the [WIP spec](https://github.com/vrc-get/vrc-get/blob/133b03467efb454af0ed336881e4042e60551171/docs/vpm-spec.md)).
