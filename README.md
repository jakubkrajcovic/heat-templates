heat-templates
==============

These heat templates are intended to work with the Rackspace public cloud and the Rackspace private cloud
Ideally, comments will be added to the templates in-line so they should be self-explanatory.

Your shell environment for use with Rackspace should look something like this:

```export OS_AUTH_URL=https://identity.api.rackspacecloud.com/v2.0/
export OS_AUTH_SYSTEM=rackspace
export OS_REGION_NAME=SYD
export OS_USERNAME=your_username
export OS_TENANT_NAME=your_tenant_id
export OS_TENANT_ID=your_tenant_id
export NOVA_RAX_AUTH=1
export OS_PASSWORD=your_api_key
export OS_PROJECT_ID=you_tenant_id
export OS_NO_CACHE=1

export REGION=syd
export HEAT_URL=https://${REGION}.orchestration.api.rackspacecloud.com/v1/${OS_TENANT_ID}

alias heat="heat -k --os-password \"your_actual_password" "
```

There is a discrepancy between Nova and Heat in that Nova expects `OS_PASSWORD` to be the API key, 
but Heat expects it to be the actual password.
