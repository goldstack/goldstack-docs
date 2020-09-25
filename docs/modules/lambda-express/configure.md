The following key properties need to be configured for this module:

- **Lambda Name**: The [name](https://docs.aws.amazon.com/lambda/latest/dg/API_CreateFunction.html#SSS-CreateFunction-request-FunctionName) to be used for this lambda. This needs to be unique per AWS region.
- **API Domain**: The domain where the API should be deployed to. For instance, to be able to call the API endpoint `https://api.mydomain.com/` the API domain `api.mydomain.com` needs to be configured. 
- **Hosted Zone Domain**: A [Route 53 hosted zone](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/hosted-zones-working-with.html) that will allow adding the _API Domain_ as a record. For instance, in order to configure the API domain `api.mydomain.com`, the hosted zones `api.mydomain.com` or `mydomain.com` would be valid. Note that this hosted zone must already exist in AWS. Please find instructions of how to set up a hosted zone [here](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/CreatingHostedZone.html). 