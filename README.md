# terraform-101 -  Installation



***website***: [\[terraform.io\]\](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)

**MacOs** test

```
brew tap hasicorp/tap
brew install hasicorp/tap/terraform
```

**Windows**

```
choco install terraform

```
**Ubuntu**

```
sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
```


**Install the HashiCorp [GPG key](https://apt.releases.hashicorp.com/gpg "HashiCorp GPG key").**

```
wget -O- https://apt.releases.hashicorp.com/gpg | \
gpg --dearmor | \
sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg > /dev/null
```


**Verify the key's fingerprint.**

```
gpg --no-default-keyring \
--keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
--fingerprint
```


**Add the official HashiCorp repository to your system. The `lsb_release -cs` command finds the distribution release codename for your current system, such as `buster`, `groovy`, or `sid`.**


```
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
sudo tee /etc/apt/sources.list.d/hashicorp.list
```

**Download the package information from HashiCorp.**

```
sudo apt update
```

**Install Terraform from the new repository.**

```
sudo apt-get install terraform
```
