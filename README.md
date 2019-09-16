# AWS Resources for CICD Pipeline

This repository contains cloudformation templates for CICD pipeline to deploy WSO2 products in Amazon Web Services(AWS).

For each of the product devlopment, staging and production cloudformation templates are available.
    
   - _cf-dev.yaml_ - Cloud formation template for Development environment
    
   - _cf-staging.yaml_ - Cloud formation template for Staging environment
    
   - _cf.yaml_ - Cloud formation template for Production environment

The cloudformation templates use the following AMI's to provision the deployment.

    Monitoring AMI - Contains the configurations and services necessary for Grafana dashboards.

    Logging AMI - Contains the configurations and services necessary to get the product logs on kibana dashboard.

    Product AMI: Contains the product pack, databse scripts. This is a parameter of the cloudformation stack.

A sample cloudformation template is provided under sampleCFN folder. This cloudformation template can be used to deploy the product in any environment. This sampe CFN template is configured with Logging.
        
   **Note:** Change the userdata section of the auto scaling groups according to the deployed product.