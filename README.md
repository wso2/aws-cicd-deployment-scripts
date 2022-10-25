# AWS Resources for CICD Pipeline
> **Warning**
>
>   The CICD pipeline is deprecated.
>

This repository contains CloudFormation templates for CICD pipeline to deploy WSO2 products in Amazon Web Services(AWS).

   - _cf-dev.yaml_ - CloudFormation template for Development environment
    
   - _cf-staging.yaml_ - CloudFormation template for Staging environment
    
   - _cf.yaml_ - CloudFormation template for Production environment
   
   - _network.yaml_ - ClouFormation template contains network resources shared in development and staging environments.

The CloudFormation templates use the following AMI's to provision the deployment.

    Monitoring AMI - Contains the configurations and services necessary for Grafana dashboards.

    Logging AMI - Contains the configurations and services necessary to get the product logs on kibana dashboard.

    Product AMI - Contains the product pack, databse scripts. This is taken as a parameter in the CloudFormation stack.

A sample CloudFormation template is provided under sampleCFN folder. This CloudFormation template can be used to deploy the product in any environment. This sample.yaml template is configured with Logging.
        
   **Note:** Change the userdata section of the auto scaling groups according to the deployed product.