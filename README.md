# elastic-beanstalk-autodeploy

A fairly straightforward example showing a docker-compose application's auto-deploy setup using GitHub Actions and AWS' Elastic Beanstalk. This is a pretty small example that I put together for my portfolio projects [motd-api-ts](https://github.com/hollyplankdev/motd-api-ts).

# Resources Used

- [Muharrem K: AWS Elastic Beanstalk with docker-compose.yml file](https://medium.com/adessoturkey/aws-elastic-beanstalk-with-docker-compose-yml-file-ae5958569b2f)
- [GitHub: Configuring OpenID Connect in Amazon Web Services](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services#adding-the-identity-provider-to-aws)
- [AWS: Creating and managing an OIDC provider (console)](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html#manage-oidc-provider-console)
- [AWS: Creating a role for OIDC](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-idp_oidc.html#idp_oidc_Create)
- [GitHub Actions: configure-aws-credentials](https://github.com/aws-actions/configure-aws-credentials?tab=readme-ov-file#oidc)
- [GitHub Actions: beanstalk-deploy](https://github.com/einaregilsson/beanstalk-deploy)

# Using in a Project

## EB CLI

Make sure that you have the Elastic Beanstalk CLI [installed](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html) and [configured](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-configuration.html).

## Initialize Elastic Beanstalk Application

Before we setup autodeploy, we need something to deploy TO. 
- Make sure that you're repository is configured to work as an EB application (in the case of docker, ensure that there is a Dockerfile or docker-compose.yml in the root).
- 

# Dev Log

Configure [OIDC between AWS & GitHub](https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services)

- Followed this https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html
- Followed this https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_create_for-idp_oidc.html#idp_oidc_Create
- ![](docs/role-creation.png)
- Gave it permissions `AWSElasticBeanstalkWebTier` and `AWSElasticBeanstalkManagedUpdatesCustomerRolePolicy`
-
