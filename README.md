# ansible-fluentd

ansible-galaxy の williamyeh.fluentd をベースに改良する

```
$ ansible-galaxy install williamyeh.fluentd -p roles
```

## Setup

- `production` の ip アドレス変更

## Usage

```
$ ansible-playbook -i production site.yml --private-key="~/.ssh/priv_key.pem"
```
