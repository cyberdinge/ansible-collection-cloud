# Ansible Collection - cyberdinge.cloud

Documentation for the collection.

## Use the collection in your project

Create or edit a file called `requirements.yaml` in your project root.

```yaml
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

```sh
ansible-galaxy collection install -r requirements.yaml
```

## Docs

The collection docs are made with `mkdocs`.

You can start the doc server locally with:

```
mkdocs serve -f mkdocs.yml 
```

Or build a static copy: 

```
mkdocs build -f mkdocs.yml --clean
```

## Maintain the collection

### build the collection to a tar file

```
ansible-galaxy collection build
```

### run collection tests

```
ansible-test sanity --docker default
```

## License

please see [LICENSE file](LICENSE) for license details