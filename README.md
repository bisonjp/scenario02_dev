# Zscaler Demo Scenario2
## Prequisite
- Prepare following Zscaler licenses
    - Zscaler Internet Access license
    - Zscaler Private Access license
    - Zscaler Cloud Connector license 
- Create AWS IAM account who is assigned PowerUserAccess and IAMFullAccess policy
- Subscribe Zscaler Private Access Connector on AWS
- Terrafrom Cloud account
- Github account

## Overview
This scenario is for testing secure access to private application which is deployed on AWS via Zscaler Private Access. Also, deployed Windows Server go through internet securely via Zscaler Cloud Connector.
This code will make following AWS environment. Also App Connector will connect to ZPA Serivce Edge automatically.  

![image](https://github.com/bisonjp/scenario02_dev/assets/39214022/a1bd956d-f4f6-418f-879d-97a43009145c)


## Directory structure
    ├── README.md
    ├── main.tf
    ├── aws_ac.tf
    ├── aws_cc.tf
    ├── modules
    |      ├── terraform-zscc-ccvm-aws
    |      |          ├── README.md
    |      |          ├── main.tf
    |      |          ├── variables.tf
    |      |          ├── versions.tf
    |      |          └── output.tf     
    |      └── terraform-zscc-iam-aws
    |                 ├── README.md
    |                 ├── main.tf
    |                 ├── variables.tf
    |                 ├── versions.tf
    |                 └── output.tf     
    ├── zpa.tf
    ├── variable.tf
    └── output.tf
