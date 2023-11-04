# ansible-role-skeleton-customizer

Rough sketch for creating an Ansible role skeleton customizer.

The Ansible role skeleton is really handy for quickly creating new Ansible roles, however, if you wish to reuse your role skeleton in another context, for example at work instead of home, then you may find yourself manually editing multiple files in your role skeleton.

## Example

This clunky example uses [robertdebock/ansible-role-skeleton](https://github.com/robertdebock/ansible-role-skeleton) as a base. It has been **partially customized** as a proof of concept (POC) to allow for changes to a few items

## Two Step Process

### Create your customized Ansible role skeleton

1. Clone this repository
2. Make changes to the available vars in `playbook.yaml` and/or role template contents found in the  templates directory.
3. Run the included  `playbook.yaml`
    1. With the default settings this will output your customized Ansible role skeleton to the directory `custom-role-skeleton`

### Create a new role from your custom Ansible role skeleton

To create a new role using  `ansible-galaxy init` 

```shell
ansible-galaxy init --role-skeleton=custom-role-skeleton your_new_role_name_here
```

Make sure to credit Robert for his awesome work or create your own customizable role template.

## Skeleton Template Customization Notes

You will need to ensure that Jinja2 template variables for the role name as well as Jinja2 reserved characters are escaped. See the flowing documentation for details:

* [https://jinja.palletsprojects.com/en/3.0.x/templates/#escaping



