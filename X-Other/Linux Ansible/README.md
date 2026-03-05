## Table of contents for this directory:

ad_to_unix.yaml
* check if pbis exists
* add group to access.conf
* List all pbis service status'
* Generate a support pack for pbis
* remove a grouip from access.conf

add_user.yaml
* check if SSSD or pbis is being used
* stop sssd or pbis
* Create new local user
* restart SSSD or pbis

append_file.yaml
* Confirm dns does not exist in dhcpdc.conf
* Ensure GROUP_NAME exists in access.conf
* Update chrony.conf
* Add second time server

dhcp.yaml
* Confirm dns does not exist in dhcpdc.conf
* update dhcpcd.conf if missing dns

hello_world.yaml
* basic hello world

linux_services.yml
* Start service httpd, if not started
* Stop service httpd, if started
* Restart service httpd, in all cases
* Reload service httpd, in all cases

local_user.yaml
* Local user with password, shell, super group (wheel, adm, sudo, etc)

network.yaml
* Confirm dns does not exist in dhcpdc.conf
* Ensure GROUP_NAME exists in access.conf
* Check if we have chrony.conf
* Update chrony.conf
* Add second time server
* Confirm resolv.conf has lines

packages.yaml
* Confirm tmux is installed
* Confirm tmux, python3 and vim-enhanced are installed
* Install the latest version of emacs

private_lin_hello.yml
* Tag example with hello statements

puppet.yaml
* Stop Puppet and Disable Service if exists
* Command line disable puppet agent with message
* Stop puppet agent with comment in logs
* output puppet agent stopping

puppet_disable.yaml
* Stop Puppet and Disable Service if exists
* Command line disable puppet agent with message
* Stop puppet agent with comment in logs
* output puppet agent stopping

splunk_deploy.yml
* Pull rpm locally
* Import GnuPG Public Key for Splunk package
* Install Splunk Forwarder RPM package on remote servers.
* Install Splunk Forwarder RPM package on remote servers.
* Add server config
* Start Splunk forwarder service.
* Check Splunk forwarder service.
* Report Splunk forwarder Status.
* Set fact splunkforwarder_installed
* Enable Splunk forwarder service at boot (stop)
* Enable Splunk forwarder service at boot (enable)
* Enable Splunk forwarder service at boot (start)

ssh_ntp_check_restart.yaml
* check if ntpd or sshd are running
* if running restart ntpd or sshd

sshd_service_check_restart.yaml
* check if service exists and what state

sudoers.yaml
* Add webteam members to sudoers.d
* Add L3 support members to sudoers.d
* Add backup team members to sudoers.d
* Add numerous team members to sudoers.d

user_creation_local.yaml
* Create Local User on system with luseradd vs adduser, useradd, etc

yum.yaml
* Confirm tmux is installed
* Get hostname
* Which python
* print result
* Yum example
* Yum install screen
* Yum install tmux
* Run yum update only on RHEL 6
* Run dnf / yum update only on RHEL 7
* Run dnf update only on RHEL 8
* Get list of packages that were update


yum_packages.yaml
* Confirm tmux is installed
* Confirm tmux, python3 and vim-enhanced are installed
* Install the latest version of emacs
