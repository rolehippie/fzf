# fzf

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/fzf) [![Build Status](https://img.shields.io/drone/build/rolehippie/fzf/master?logo=drone)](https://cloud.drone.io/rolehippie/fzf) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/fzf)](https://github.com/rolehippie/fzf/blob/master/LICENSE) 

Ansible role to install the command-line fuzzy finder. 

## Sponsor 

[![Proact Deutschland GmbH](https://proact.eu/wp-content/uploads/2020/03/proact-logo.png)](https://proact.eu) 

Building and improving this Ansible role have been sponsored by my employer **Proact Deutschland GmbH**.

## Table of content

* [Default Variables](#default-variables)
  * [fzf_binary_download](#fzf_binary_download)
  * [fzf_static_version](#fzf_static_version)
  * [fzf_wrapper_download](#fzf_wrapper_download)
* [Dependencies](#dependencies)
* [License](#license)
* [Author](#author)

---

## Default Variables

### fzf_binary_download

URL to download the static binary

#### Default value

```YAML
fzf_binary_download: https://github.com/junegunn/fzf-bin/releases/download/{{ fzf_static_version
  }}/fzf-{{ fzf_static_version }}-linux_amd64.tgz
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

## Dependencies

* None

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
