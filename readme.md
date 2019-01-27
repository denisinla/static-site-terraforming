Terraform a static site on AWS with S3, Cloudfront, Route53, ACM
Setup assumes the following:

  - AWS credentials configured
  - Domain Nameservers on Route53 with a Zone ID
  - ACM certificate issued


Usage:

```
module "s3site" {
  source = "github.com/denisinla/static-site-terraforming"

  region = "us-east-1"
  domain = "mysite.com"
  zone_id = "route53_zone_id"
  certificate_arn = "cert_arn"
}
```
