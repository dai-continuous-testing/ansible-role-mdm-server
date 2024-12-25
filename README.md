Experitest - MDM Server ansible role
=========

This role will install \ uninstall mdm server for linux os hosts

Requirements
------------

* This role assumes that you have [postgresql server](https://github.com/ExperitestOfficial/ansible-role-postgresql-server) already installed.<br>
* Supports linux os hosts only.

Role Variables
--------------

| Name | Description | Type | Default | Required |
|------|-------------|:----:|:-----:|:-----:|
| state | should the application be present or absent | present, absent | present | no |
| app_version | application version to install | string | 21.5.37 | no |
| server_port | port number for the server | number | 443 | no |
| extra_application_properties | additional props to be override in application.properties file | dict | {} | no |
| extra_application_encrypted_properties | additional props to be override in application-encrypted.properties file | dict | {} | no |
| db_connection_string | connection string to postgres | string | jdbc:postgresql://localhost:5432/mdmserver | no |
| db_username | username for db connection | string | postgres | no |
| db_password | password for db connection | string |  | yes |
| installation_root_folder | the root folder in which the application will be installed under mdmserver-{version} folder | string | for linux: /opt/Experitest | no |
| java_version | java jre version to install | string | 17.0.3_7 | no |
| custom_download_url | custom url to download the installation from (zip format) | string |  | no |
| custom_download_username | username to download from custom url on windows | string |  | no |
| custom_download_password | password to download from custom url on windows | string |  | no |
| start_after_install | should application start after installation is completed | boolean | True | no |
| clear_temp_folder | remove temp folder after installation | boolean | False | no |
| clear_before_install | removing old installation before installing new version | boolean | False | no |

Example Playbook
----------------

#### [see working example](/example)
