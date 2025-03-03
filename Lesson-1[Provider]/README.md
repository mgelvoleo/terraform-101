Website different provider: registry.terraform.io/browse/providers
Ref for local provider: https://registry.terraform.io/providers/hashicorp/local/latest/docs

Local

https://registry.terraform.io/providers/hashicorp/local/latest/docs/resources/file

terraform {
  required_providers {
    local = {
      source = "hashicorp/local"
      version = "2.5.2"
    }
  }
}






Multi Region

```
provider "aws"{
	alias = "us-east"
     region = "us-east-1"
}

resource "aws_instance" "example" {
	ami = "67890-fdfsdfd"
	instance_type = "t3.macro"
	provider = "aws.us-east-1"
}

```


**Multi Provider**

**aws**

```
provider "aws"{
     region = "us-east-1"
}
```

**azure**

```
provider "azurerm" {
	sub...
	client_id = ""
	client_secret = "secrete"
	tenant_id
}

```


Command: 

```
terraform init 
```


