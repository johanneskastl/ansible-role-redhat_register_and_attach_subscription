![Ansible Lint](https://github.com/johanneskastl/ansible-role-redhat_register_and_attach_subscription/workflows/Ansible%20Lint/badge.svg)

redhat_register_and_attach_subscription
=========

Register a RedHat machine and add a subscription to it

Requirements
------------

None.

Role Variables
--------------

To register, you need to provide a `username` and a `password`.

- `redhat_username`: (String) The username used for registration.
- `redhat_password`: (String) The password used for registration.

The role by default attaches a subscription to your machine. This can be changed by setting the following variable to `false`:

- `redhat_subscription_auto_attach`: (Boolean) Whether to auto-attach a subscription, default value is `true`

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: 'johanneskastl.redhat_register_and_attach_subscription'
          redhat_username: 'austin.powers'
          redhat_password: 'IshouldreallynotbehereincleartextbutratherencryptedwithAnsibleVault'

License
-------

BSD-3-Clause

Author Information
------------------

I am Johannes Kastl, reachable via kastl@b1-systems.de.
