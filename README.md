sbog/dovecot
============

Role to install and configure Dovecot

#### Requirements

Ansible 2.4

#### Role Variables

```yaml
mail_domain: example.ru
mail_hostname: mail.example.ru
mail_ssl_enabled: true
mysql_bind_address: "127.0.0.1"
postfix_db_name: postfix
postfix_db_user: postfix
postfix_db_password: postfixpassword
# MX hosts var is rather unneeded, it's just useful to remember which
# names you need to put into TLS certificate
mx_hosts:
  - mail.example.ru
  - smtp.example.ru
  - imap.example.ru
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install and configure Dovecot
  hosts: localhost
  remote_user: root
  roles:
    - dovecot
```

#### License

Apache 2.0

#### Author Information

Stanislaw Bogatkin (https://sbog.ru)
