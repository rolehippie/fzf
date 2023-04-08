# fzf

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&amp;logoColor=white)](https://github.com/rolehippie/fzf)
[![General Workflow](https://github.com/rolehippie/fzf/actions/workflows/general.yml/badge.svg)](https://github.com/rolehippie/fzf/actions/workflows/general.yml)
[![Readme Workflow](https://github.com/rolehippie/fzf/actions/workflows/readme.yml/badge.svg)](https://github.com/rolehippie/fzf/actions/workflows/readme.yml)
[![Galaxy Workflow](https://github.com/rolehippie/fzf/actions/workflows/galaxy.yml/badge.svg)](https://github.com/rolehippie/fzf/actions/workflows/galaxy.yml)
[![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/fzf)](https://github.com/rolehippie/fzf/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/badge/role-rolehippie.fzf-blue)](https://galaxy.ansible.com/rolehippie/fzf)

Ansible role to install the command-line fuzzy finder.

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Requirements](#requirements)
- [Default Variables](#default-variables)
  - [fzf_binary_arch](#fzf_binary_arch)
  - [fzf_binary_download](#fzf_binary_download)
  - [fzf_static_version](#fzf_static_version)
  - [fzf_wrapper_download](#fzf_wrapper_download)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Requirements

- Minimum Ansible version: `2.10`


## Default Variables

### fzf_binary_arch

Architecture of the static binary

#### Default value

```YAML
fzf_binary_arch: "{{ 'arm8' if ansible_architecture == 'aarch64' else 'amd64' }}"
```

### fzf_binary_download

URL to download the static binary

#### Default value

```YAML
fzf_binary_download: https://github.com/junegunn/fzf-bin/releases/download/{{ fzf_static_version
  }}/fzf-{{ fzf_static_version }}-linux_{{ fzf_binary_arch }}.tgz
```

### fzf_static_version

Version of the static release

#### Default value

```YAML
fzf_static_version: 0.21.1
```

### fzf_wrapper_download

URL to download the tmux wrapper

#### Default value

```YAML
fzf_wrapper_download: https://raw.githubusercontent.com/junegunn/fzf/{{ fzf_static_version
  }}/bin/fzf-tmux
```

## Discovered Tags

**_fzf_**


## Dependencies

- None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
