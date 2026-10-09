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

![
]({099D90B3-7B7F-4C4D-BE5A-4C24BD88842C}.png)

![alt text]({F464485D-2D9F-410C-B15F-409E1A3BE8DD}.png)
