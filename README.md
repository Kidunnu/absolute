#
DOCUMENTATION TO DESCRIBE FRAMEWORK This explains the framework for deploying the new project "Absolute Agent web service".

Steps:

Provision s3 bucket in aws using terraform see s3_bucket.tf for example

Connect my s3 bucket to on-premise Kubenetes cluster using direct connect

Use terraform module to creates AWS CloudFront with for customer access

Update the DNS records for your domain to point your website's CNAME to your CloudFront distribution's domain name.

Configure security framework to protect s3 bucket.
Add a bucket policy that allows public read access via cloudfront to the bucket that you created.

Use SSL (HTTPS) for your website. Use a custom domain with HTTPS, select Custom SSL certificate
