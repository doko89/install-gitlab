This is playbook to deploy github ee on your server
============

### example playbook
------------

```
- hosts: repo
  env_file:
    - env.yml
  roles:
    - install-gitlab
```

## Example env.yml
```
domain: repo.local.dev

letsencrypt: false
email: admin@mail.com

```



### Note
---------
if ram less than 1GB
you can add create-swap role on playbook [create-swap](https://github.com/doko89/create-swap.git)


###

### example playbook with create swap
------------

```
- hosts: repo
  env_file:
    - env.yml
  roles:
    - create-swap
    - install-gitlab
```
