# ansistrano-php

## Project

### Add ansistrano-php to your project

*needs to be done once*

```bash
git submodule add https://github.com/artack/ansistrano-php.git deployment
```

### Copy dist-files to your project

*needs to be done once*

```bash
cp deployment/ansible.cfg.dist ansible.cfg
cp deployment/hosts.yaml.dist hosts.yaml
cp deployment/deploy.yaml.dist deploy.yaml
cp deployment/rollback.yaml.dist rollback.yaml
```

Multistage ist also possible when copy the deploy.yaml.dist and rollback.yaml.dist multiple times, e.g.:

```bash
cp deployment/deploy.yaml.dist deploy_prod.yaml
cp deployment/deploy.yaml.dist deploy_stag.yaml
cp deployment/rollback.yaml.dist rollback_prod.yaml
cp deployment/rollback.yaml.dist rollback_stag.yaml
```

### Modify your copied files - these are YOURS
Adjust, comment, uncomment any variables like:
- git repo & branch
- paths
- project type (role)
