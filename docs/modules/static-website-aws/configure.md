The following key properties need to be configured for this module:

- **Hosted Zone Domain**: A [Route 53 hosted zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-working-with.html) to which the _Primary Website Domain_ and _Redirect Website Domain_ can be added as records. For instance, a hosted zone domain is `mysite.com` will allow adding the primiary domain `mysite.com` and the redirect domain `www.mysite.com`. Note that this hosted zone must already exist in AWS. Please find instructions of how to set up a hosted zone [here](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingHostedZone.html).
- **Primary Website Domain**: This is the domain your users will use to view the site. For instance, if you configure the domain `mysite.com`, users will be able to view your site by opening the URL `https://mysite.com`.
- **Redirect Website Domain**: This is a domain that will redirect all requests to your _Primary Website Domain_. For instance, if you configure the domain `www.mysite.com` as your redirect domain and `mysite.com` as your primiary domain, users will be redirected to `https://mysite.com` when they attempt to open the URL `https://www.mysite.com`. Note that the _Redirect Website Domain_ must be configured, even if you do not need this functionality. 
- **Default Cache Duration**: The number of seconds that files will be cached in the AWS content delivery network. Setting this to `120` for instance, would mean that, unless otherwise specified, webpages and other resources will be cached for 120 s. In that case, when a new version of a page is deployed, it can take up to 120 s for changes to appear when accessing the deployed version of the application.