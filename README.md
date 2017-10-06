# ansible-fluentd

## What's?

- fluentd を ansible で構築する
- ansible-galaxy の [williamyeh.fluentd](https://github.com/William-Yeh/ansible-fluentd) をベースに改良する
- S3 にログファイルをアップロードする設定テンプレート

## Setup

- `production` の ip アドレス変更

## Usage

plugin を追加したいときは `site.yml` の下記に追加

```
vars:
  tdagent_plugins:
```

設定テンプレート

- `roles/williamyeh.fluentd/templates/td-agent.conf.j2`

### Deploy

```
$ ansible-playbook -i production site.yml --private-key="~/.ssh/priv_key.pem"
```

## Install williamyeh.fluentd from ansible-galaxy if needed

```
$ ansible-galaxy install williamyeh.fluentd -p roles
```
