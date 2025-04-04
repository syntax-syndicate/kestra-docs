---
# generated by https://github.com/hashicorp/terraform-plugin-docs
title: kestra_group
editLink: false
description: |-
  Manages a Kestra Group.
  -> This resource is only available on the Enterprise Edition https://kestra.io/enterprise
---

# kestra_group (Resource)

Manages a Kestra Group.

::alert{type="info"}
This resource is only available on the [Enterprise Edition](https://kestra.io/enterprise)
::

## Example Usage

```hcl
resource "kestra_group" "example" {
  namespace   = "company.team"
  name        = "Friendly name"
  description = "Friendly description"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) The group name.

### Optional

- `description` (String) The group description.
- `namespace` (String) The linked namespace.

### Read-Only

- `id` (String) The ID of this resource.
- `tenant_id` (String) The tenant id.

## Import

Import is supported using the following syntax:

```shell
terraform import kestra_group.example {{group_id}}
```
