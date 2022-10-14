---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_current_space Data Source - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_current_space is a data source that provides information about the space that an administrative stack is in if the run is executed within Spacelift by a stack or module. This  makes it easier to create resources within the same space.
---

# spacelift_current_space (Data Source)

`spacelift_current_space` is a data source that provides information about the space that an administrative stack is in if the run is executed within Spacelift by a stack or module. This  makes it easier to create resources within the same space.

## Example Usage

```terraform
data "spacelift_current_space" "this" {}

resource "spacelift_context" "prod-k8s-ie" {
  description = "Configuration details for the compute cluster in 🇮🇪"
  name        = "Production cluster (Ireland)"
  space_id    = data.spacelift_current_space.this.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `id` (String) The ID of this resource.

