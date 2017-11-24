Lynis
=====

[![Build Status](https://travis-ci.org/maxlareo/ansible-lynis.svg?branch=master)](https://travis-ci.org/maxlareo/ansible-lynis) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-lynis-blue.svg)](https://galaxy.ansible.com/maxlareo/lynis/)

Install and configure Lynis in Debian-like systems

Requirements
------------

None

Role Variables
--------------

### About the `/etc/lynis/custom.prf` file

- `lynis_colors`: [default: `'yes'`]: Use colored output
- `lynis_compressed_uploads`: [default: `'yes'`]: Compressed uploads (set to zero when errors with uploading occur)
- `lynis_error_on_warnings`: [default: `'no'`]: Show non-zero exit code when warnings are found
- `lynis_language`: [default: `''`]: Use Lynis in your own language (by default auto-detected)
- `lynis_license_key`: [default: `''`]: Lynis Enterprise license key
- `lynis_machine_role`: [default: `server`]: Defines the role of the system (personal, workstation or server)
- `lynis_profile_name`: [default: `Default Audit Template`]: Profile name, will be used as title/description
- `lynis_pause_between_tests`: [default: `0`]: Number of seconds to pause between every test (0 is no pause)
- `lynis_quick`: [default: `'no'`]: Enable quick mode (no waiting for keypresses, same as --quick option)
- `lynis_refresh_repositories`: [default: `'yes'`]: Refresh software repositories to help detecting vulnerable packages
- `lynis_show_report_solution`: [default: `'yes'`]: Show solution for findings
- `lynis_show_tool_tips`: [default: `'yes'`]: Show inline tips about the tool
- `lynis_skip_plugins`: [default: `'no'`]: Skip plugins
- `lynis_skip_tests`: [default: `[]`]: Skip a test (one per line) or skip a particular option within a test (when applicable)
- `lynis_test_scan_mode`: [default: `full`]: Scan type - how deep the audit should be (light, normal or full)
- `lynis_upload`: [default: `'no'`]: Upload data to central server
- `lynis_upload_server`: [default: `''`]: The hostname/IP address to receive the data
- `lynis_upload_options`: [default: `''`]: Provide options to cURL (or other upload tool) when uploading data. Upload-options=--insecure   --> use HTTPS, but skip certificate check (e.g. self-signed)
- `lynis_verbose`: [default: `'no'`]: Verbose output
- `lynis_plugins`: [default: `[]`]: Lynis Plugins

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - lynis
```

License
-------

MIT

Author Information
------------------

[Maxime Lareo](https://github.com/maxlareo)

Feedback, bug-reports, requests, ...
------------------------------------

Are [welcome](https://github.com/maxlareo/ansible-lynis/issues)!
