ansible-graylog-alert-exporter
=========

Install graylog alert exporter using ansible.

more infomation [Graylog alert exporter](https://github.com/StartloJ/graylog-alert-exporter)

Requirements
------------

- Ansible >= 2.9

Role Variables
--------------

| Name of Variables                          | Description                                                             | Type    | Example                | Required |
|--------------------------------------------|-------------------------------------------------------------------------|---------|------------------------|----------|
| graylog_alert_exporter_version             | Choose version package to install. see source repo                      | number  | 0.1.0                  | yes      |
| graylog_alert_exporter_binary_local_dir    | Path of folder that store binary file                                   | string  | /tmp/graylog           | no       |
| graylog_alert_exporter_binary_name         | Binary file name to relate in `graylog_alert_exporter_binary_local_dir` | string  | graylog-alert-exporter | no       |
| graylog_alert_exporter_listen_address      | Config to listener address for receive webhook and prometheus scraped   | string  | 0.0.0.0:9889           | yes      |
| graylog_alert_exporter_metrics_path        | Http sub-path for provide metrics and receive hook                      | string  | /metrics               | yes      |
| graylog_alert_exporter_timeout             | Expectation for keep problem metrics in second                          | number  | 3600                   | yes      |
| graylog_alert_exporter_interval            | Time to counter timeout in every x second                               | number  | 5                      | yes      |
| graylog_alert_exporter_labels_created      | Create promethues labels with dict variable                             | Map     | app: "Example"         | no       |
| graylog_alert_exporter_debug               | Enable debug log on console                                             | boolean | true                   | no       |
| graylog_alert_exporter_caller              | Enable advance debug log on console with request parameter              | boolean | false                  | no       |
| _graylog_alert_exporter_binary_install_dir | Path to install package binary in destination host                      | string  | /etc/exporter/graylog  | yes      |
| _graylog_alert_exporter_system_group       | User's group name to run binary process                                 | string  | exporter               | yes      |
| _graylog_alert_exporter_system_user        | System's username to run process                                        | string  | exporter               | yes      |

Example Playbook
----------------

```yaml
- hosts: all
  gather_facts: true
  roles:
    - ansible-graylog-alert-exporter
```

## Local Testing
These steps are use to locally testing the role with [molecule](https://github.com/ansible-community/molecule).

1. Install test requirements via `pip install -r test-requirements.txt`.

2. Simple run `molecule test`.

> You can test all step with wrapper use  
> `$ tox`   
> and configure in **tox.ini**

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
