---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_stack_destructor Resource - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_stack_destructor is used to destroy the resources of a Stack before deleting it. depends_on should be used to make sure that all necessery resources (environment variables, roles, integrations, etc.) are still in place when the destruction run is executed.
---

# spacelift_stack_destructor (Resource)

`spacelift_stack_destructor` is used to destroy the resources of a Stack before deleting it. `depends_on` should be used to make sure that all necessery resources (environment variables, roles, integrations, etc.) are still in place when the destruction run is executed.

## Example Usage

```hcl
resource "spacelift_stack" "k8s-core" {
  // ...
}

resource "spacelift_environment_variable" "credentials" {
  // ...
}

resource "spacelift_stack_destructor" "k8s-core" {
  depends_on = [
    spacelift_environment_variable.credentials,
  ]

  stack_id = spacelift_stack.k8s-core.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- **stack_id** (String) ID of the stack to delete and destroy on destruction

### Optional

- **deactivated** (Boolean) If set to true, destruction won't delete the stack
- **id** (String) The ID of this resource.

