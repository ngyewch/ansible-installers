# ngyewch.installers

Opinionated software installers for Linux.

## Collection dependencies

```
- source: git+https://github.com/QueraTeam/ansible-github.git
  type: git
```

## Roles

### `install_caddy`

Installs [caddy](https://github.com/caddyserver/caddy) and registers it as a service.

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`caddy_version` |`string` | |Caddy version.
|`email_address` |`string` | |Email address. See https://caddyserver.com/docs/caddyfile/options#email

#### Templates

|Source |Target |Description
|- |- |-
|`etc/caddy/conf.d/*` |`/etc/caddy/conf.d/` |Configuration files.
|`etc/caddy/sites-available/*` |`/etc/caddy/sites-available/` |Available sites.

### `install_oauth2_proxy`

Installs [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy).

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`oauth2_proxy_version` |`string` | |oauth2-proxy version.

### `install_oauth2_proxy_instance`

Registers a [oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy) service.

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`instance_name` |`string` | |Instance name.

#### Templates

|Source |Target |Description
|- |- |-
|`etc/oauth2-proxy/{{ instance_name }}.cfg` |`/etc/oauth2-proxy/{{ instance_name }}.cfg` |Configuration file.

### `install_ory_hydra`

Installs [Ory Hydra](https://github.com/ory/hydra).

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`ory_hydra_version` |`string` | |Ory Hydra version.

### `install_ory_hydra_instance`

Registers an [Ory Hydra](https://github.com/ory/hydra) service.

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`instance_name` |`string` | |Instance name.

#### Templates

|Source |Target |Description
|- |- |-
|`etc/ory/hydra/{{ instance_name }}.yml` |`/etc/ory/hydra/{{ instance_name }}.yml` |Configuration file.

### `install_watchexec`

Installs [watchexec](https://github.com/watchexec/watchexec).

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`watchexec_version` |`string` | |watchexec version.

### `install_watchexec_instance`

Registers a [watchexec](https://github.com/watchexec/watchexec) service.

#### Variables

|Name |Type |Default |Description
|- |- |- |-
|`instance_name` |`string` | |Instance name.
|`working_directory` |`string` | |Working directory.
|`watchexec_args` |`string` | |watchexec args.
