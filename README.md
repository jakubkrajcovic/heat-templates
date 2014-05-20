heat-templates
==============

These heat templates are intended to work with the Rackspace public cloud and the Rackspace private cloud
Ideally, comments will be added to the templates in-line so they should be self-explanatory.

## Overview
Organization of this repository is as follows:
* [Customers](https://github.com/jakubkrajcovic/heat-templates/customers "Customers") contains Heat templates built for specific customer environments
* [building-blocks](https://github.com/jakubkrajcovic/heat-templates/building-blocks "Building Blocks") contains a list of well documented single-purpose code snippets that aim to complement the main [Heat Documentation](http://docs.openstack.org/developer/heat/template_guide/ "Heat Template Guide")
* [Templates](https://github.com/jakubkrajcovic/heat-templates/templates "Templates") contains (hopefully) usable templates that have not yet been classified for any specific use

## Shell env setup
Your shell environment for use with Rackspace should look something like this:

```bash
export OS_AUTH_URL=https://identity.api.rackspacecloud.com/v2.0/
export OS_AUTH_SYSTEM=rackspace
export OS_REGION_NAME=your_region_uppercase
export OS_USERNAME=your_username
export OS_TENANT_NAME=your_tenant_id
export OS_TENANT_ID=your_tenant_id
export NOVA_RAX_AUTH=1
export NOVA_OS_PASSWORD=your_api_key
export OS_PASSWORD=your_password
export OS_PROJECT_ID=you_tenant_id
export OS_NO_CACHE=1

export HEAT_URL=https://${OS_REGION_NAME}.orchestration.api.rackspacecloud.com/v1/${OS_TENANT_ID}

alias nova="nova --os-password ${NOVA_OS_PASSWORD} "
alias heat="heat -k "
```

There is a discrepancy between Nova and Heat in that Nova expects `OS_PASSWORD` to be the API key,
but Heat expects it to be the actual password. Therefore we have to define not only `OS_PASSWORD` but `NOVA_OS_PASSWORD` as well.


