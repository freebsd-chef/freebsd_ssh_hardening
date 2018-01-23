# freebsd_ssh_hardening (Chef Cookbook)

## Description

This cookbook provides secure ssh-client and ssh-server configurations for FreeBSD. 
###!CAUTION This is not production ready and is under development.
## Requirements

* Chef >= 12.5.1

### Platform
- FreeBSD 11.0

## Attributes

Below you can find the attribute documentation and their default values.

Notice: Some of attribute defaults of this cookbook are set in the recipes. You should use a higher [attribute precedence](https://docs.chef.io/attributes.html#attribute-precedence) level for overriding of such attributes. Such attributes are flagged with `#override attribute#` in the list below. Example for overriding a such attribute:

```ruby
override['freebsd-ssh-hardening']['ssh']['server']['listen_to'] = node['ipaddress']
```
* `['freebsd-ssh-hardening']['ssh']['ports']` - `22`. Ports to which ssh-server should listen to and ssh-client should connect to


## Usage

Add the recipes to the run_list:

    "recipe[freebsd-ssh-hardening]"

This will install ssh-server and ssh-client. You can alternatively choose only one via:

    "recipe[freebsd-ssh-hardening::server]"
    "recipe[freebsd-ssh-hardening::client]"
