## Apigee GraphQL Demo OAUth

### Description

This repo contains an Apigee API Proxy that is meant to be used with the [Apigee GraphQL Demo](https://github.com/micovery/apigee-graphql-demo).
The repo makes use of the [Apigee maven deploy plugin](https://github.com/apigee/apigee-deploy-maven-plugin).

### How it works

This API Proxy implements an OAuth authorization server with support for the **client_credentials** grant type. 
It uses the [Apigee OAuth V2](https://docs.apigee.com/api-platform/reference/policies/oauthv2-policy)
to generate OAuth access tokens for client apps. (registered in Apigee Edge).

### How to deploy it

To deploy the API proxy and its config assets run the following command:

```bash
    mvn -ntp install \
        -Ptest \
        -Dapigee.username=${APIGEE_USERNAME} \
        -Dapigee.password=${APIGEE_PASSWORD} \
        -Dapigee.org=${APIGEE_ORG} \
        -Dapigee.env=${APIGEE_ENV}
```
    
This will deploy the `graphql-oauth` API Proxy to the specified $APIGEE_ORG organization under the `test` environment.

## Not Google Product Clause

This is not an officially supported Google product.