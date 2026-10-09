# List

Terraform lists are ordered collections of values. Access an item by its zero-based index.

```hcl
variable "prefix" {
	default = ["Mr", "Mrs", "Sir"]
	type    = list(string)
}

resource "random_pet" "my-pet" {
	prefix = var.prefix[0]
}
```

The list indexes are `0`, `1`, and `2`, so `var.prefix[0]` evaluates to `"Mr"`.
