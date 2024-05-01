# elastic-beanstalk-autodeploy
An example project demonstrating using GitHub Actions to autodeploy to AWS Elastic Beanstalk.


# Dev Log

Configure [OIDC between AWS & GitHub](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services)
- Followed this https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html
- Followed this https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-idp_oidc.html#idp_oidc_Create
- ![](docs/role-creation.png)
- Gave it permissions `AWSElasticBeanstalkWebTier` and `AWSElasticBeanstalkManagedUpdatesCustomerRolePolicy`
- 