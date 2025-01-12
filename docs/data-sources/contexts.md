---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "spacelift_contexts Data Source - terraform-provider-spacelift"
subcategory: ""
description: |-
  spacelift_contexts represents all the contexts in the Spacelift account visible to the API user.
---

# spacelift_contexts (Data Source)

`spacelift_contexts` represents all the contexts in the Spacelift account visible to the API user.

## Example Usage

```terraform
data "spacelift_contexts" "contexts" {}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- `contexts` (List of Object) (see [below for nested schema](#nestedatt--contexts))
- `id` (String) The ID of this resource.

<a id="nestedatt--contexts"></a>
### Nested Schema for `contexts`

Read-Only:

- `context_id` (String)
- `description` (String)
- `labels` (Set of String)
- `name` (String)
- `space_id` (String)


