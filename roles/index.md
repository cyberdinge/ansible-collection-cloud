# Install

Documentation for the collection.

[TOC]

# Use the collection in your project

Create or edit a file called `requirements.yaml` in your project root.

``` yaml linenums="1"
---
collections:

  # - name: https://github.com/cyberdinge/ansible-collection-cloud.git
  #   type: git
  #   version: <git branch or tag name>

  - name: https://github.com/cyberdinge/ansible-collection-cloud.git
    type: git
    version: 1.0.10

```

To install all dependencies of your project run 

``` shell linenums="1"
ansible-galaxy collection install -r requirements.yaml
```
## Maintain the collection

### build the collection to a tar file

``` bash linenums="1"
ansible-galaxy collection build
```

### run collection tests

```
ansible-test sanity --docker default
```

## License

please see [LICENSE file](LICENSE) for license details