---
layout: "acme"
page_title: "ACME: Amazon Lightsail DNS Challenge Provider"
sidebar_current: "docs-acme-dns-providers-lightsail"
description: |-
  Provides a resource to manage certificates on an ACME CA.
---
<br>

-> **NOTE:** The following documentation is auto-generated from the
ACME provider's API library [lego](https://go-acme.github.io/lego/).
Some sections may refer to lego directly - in most cases, these
sections apply to the Terraform provider as well.

# Amazon Lightsail DNS Challenge Provider

The `lightsail` DNS challenge provider can be used to perform DNS challenges for
the [`acme_certificate`][resource-acme-certificate] resource with
[Amazon Lightsail](https://aws.amazon.com/lightsail/).

[resource-acme-certificate]: /docs/providers/acme/r/certificate.html

For complete information on how to use this provider with the `acme_certifiate`
resource, see [here][resource-acme-certificate-dns-challenges].

[resource-acme-certificate-dns-challenges]: /docs/providers/acme/r/certificate.html#using-dns-challenges

## Example

```hcl
resource "acme_certificate" "certificate" {
  ...

  dns_challenge {
    provider = "lightsail"
  }
}
```
## Argument Reference

The following arguments can be either passed as environment variables, or
directly through the `config` block in the
[`dns_challenge`][resource-acme-certificate-dns-challenge-arg] argument in the
[`acme_certificate`][resource-acme-certificate] resource. For more details, see
[here][resource-acme-certificate-dns-challenges].

[resource-acme-certificate-dns-challenge-arg]: /docs/providers/acme/r/certificate.html#dns_challenge

In addition, arguments can also be stored in a local file, with the path
supplied by supplying the argument with the `_FILE` suffix. See
[here][acme-certificate-file-arg-example] for more information.

[acme-certificate-file-arg-example]: /docs/providers/acme/r/certificate.html#using-variable-files-for-provider-arguments

* `AWS_ACCESS_KEY_ID` - Access key ID.
* `AWS_SECRET_ACCESS_KEY` - Secret access key.
* `DNS_ZONE` - DNS zone.

* `LIGHTSAIL_POLLING_INTERVAL` - Time between DNS propagation check.
* `LIGHTSAIL_PROPAGATION_TIMEOUT` - Maximum waiting time for DNS propagation.


