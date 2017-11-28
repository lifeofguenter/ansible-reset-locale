[![Build Status](https://travis-ci.org/lifeofguenter/ansible-role-reset-locale.svg?branch=master)](https://travis-ci.org/lifeofguenter/ansible-role-reset-locale)

# lifeofguenter.reset-locale

## Summary

Forked from: **[williamyeh.reset-locale](https://galaxy.ansible.com/list#/roles/2716)**

This Ansible role has the following features:

 - Install specific locale.
 - Manually force locale settings (persistent).

This role is simply an attempt to solve the following problem:

> "your locale in your local machine is set to XXX, which SSH forwards to and tries to use on the server, but your server does not have it installed."  
> Source: [Ask Ubuntu](http://askubuntu.com/questions/144235/locale-variables-have-no-effect-in-remote-shell-perl-warning-setting-locale-f)


If you prefer a more complete locale solution, try alternatives such as [f500.locale](https://galaxy.ansible.com/list#/roles/647), [Stouts.locale](https://galaxy.ansible.com/list#/roles/828), [cecepm.locale](https://galaxy.ansible.com/list#/roles/2188), and [ssilab.locales](https://galaxy.ansible.com/list#/roles/1515).


## Role Variables

### Optional variables

User-configurable defaults:

```yaml
# default locale
locale: "en_US.UTF-8"

# stop accepting locale env vars from your client to the server?
locale_stop: true
```


## Usage

### Step 1: add role

Add role name `lifeofguenter.reset-locale` to your playbook file.


### Step 2: add variables

Set vars in your playbook file.

Simple example:

```yaml
---
# file: simple-playbook.yml

- hosts: all

  roles:
    - lifeofguenter.reset-locale

  vars:
    locale: "en_US.UTF-8"
```


## Dependencies

none

## License

Licensed under the MIT License. See the [LICENSE file](LICENSE) for details.

## Author Information

[Gunter Grodotzki](https://lifeofguenter.de)
