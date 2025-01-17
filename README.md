# AWSGoat : A Damn Vulnerable AWS Infrastructure

![1](https://user-images.githubusercontent.com/65826354/179526664-cb123612-7f9a-41fe-bab2-eb6b3b2518d7.png)

Compromising an organization's cloud infrastructure is like sitting on a gold mine for attackers. And sometimes, a simple misconfiguration or a vulnerability in web applications, is all an attacker needs to compromise the entire infrastructure. Since the cloud is relatively new, many developers are not fully aware of the threatscape and they end up deploying a vulnerable cloud infrastructure.

AWSGoat is a vulnerable by design infrastructure on AWS featuring the latest released OWASP Top 10 web application security risks (2021) and other misconfiguration based on services such as IAM, S3, API Gateway, Lambda, EC2, and ECS. AWSGoat mimics real-world infrastructure but with added vulnerabilities. It features multiple escalation paths and is focused on a black-box approach.

The project will be divided into modules and each module will be a separate web application, powered by varied tech stacks and development practices. It will leverage IaC through terraform and GitHub actions to ease the deployment process.

**Presented at**

- [OWASP Singapore Chapter](https://owasp.org/www-chapter-singapore/)
- [BlackHat USA 2022](https://www.blackhat.com/us-22/arsenal/schedule/index.html#awsgoat--a-damn-vulnerable-aws-infrastructure-27999)
- [DC 30: Demo Labs](https://forum.defcon.org/node/242059)

### Developed with :heart: by [INE](https://ine.com/) 

## Built With

* AWS
* React
* Python 3
* Terraform

## Vulnerabilities

The project is scheduled to encompass all significant vulnerabilities including the OWASP TOP 10 2021, and popular cloud misconfigurations.
Currently, the project  contains the following vulnerabilities/misconfigurations.

* XSS
* SQL Injection
* Insecure Direct Object reference
* Server Side Request Forgery on Lambda Environment
* Sensitive Data Exposure and Password Reset
* S3 Misconfigurations
* IAM Privilege Escalations

# Getting Started

### Prerequisites
* An AWS Account
* AWS Access Key with Administrative Privileges


### Installation

To ease the deployment process the user just needs to fork this repo, add their AWS Account Credentials to GitHub secrets, and run the Terraform Apply Action. This workflow will deploy the whole infrastructure and output the hosted application's URL. 

Here are the steps to follow:

**Step 1.** Fork the repo

**Step 2.** Set the GitHub Action Secrets:

```
AWS_ACCESS_KEY
AWS_ACCOUNT_ID
AWS_SECRET_ACCESS_KEY
```

![2](https://user-images.githubusercontent.com/65826354/179526772-16e84787-3ac9-4fd2-b57c-0c794dad5e4f.png)

**Step 3.** From the repository actions tab, run the ``Terraform Apply`` Workflow.

![3](https://user-images.githubusercontent.com/65826354/179526776-f03918c2-d944-4480-a098-f9483156b570.png)

**Step 4.** Find the application URL in the Terraform output section.

![4](https://user-images.githubusercontent.com/65826354/179526780-b01d5c3f-9968-45e9-b698-a9b1905b32b9.png)


### Manual Installation

Manually installing AWSGoat would require you to follow these steps:

**Step 1.** Clone the repo
```sh
git clone https://github.com/ine-labs/AWSGoat
```

**Step 2.** Configure AWS User Account Credentials
```sh
aws configure
```

**Step 3.** Use terraform to deploy AWSGoat
```sh
terraform init
terraform apply --auto-approve
```

# Modules

## Module 1

The first module features a serverless blog application utilizing AWS Lambda, S3, API Gateway, and DynamoDB. It consists of various web application vulnerabilities and facilitates exploitation of misconfigured AWS resources.

Overview of escalation paths for module-1

![10](https://user-images.githubusercontent.com/65826354/179526761-7f473e3d-f71c-429d-bf49-16958c5cb7a6.png)


**Recommended Browser:** Google Chrome

## Module 2

The second module is under development and would feature an internal HR Payroll application, utilizing the AWS ECS infrastructure. The module will be released after Black Hat USA 2022.

# Contributors

Jeswin Mathai, Chief Architect, Lab Platform, INE  <jmathai@ine.com>

Nishant Sharma, Director, Lab Platform, INE <nsharma@ine.com>

Sanjeev Mahunta, Software Engineer (Cloud), INE <smahunta@ine.com>

Shantanu Kale, Cloud Developer, INE  <skale@ine.com>


# Solutions

The manuals are available in the [solutions](solutions/) directory 

Module 1 Exploitation Videos: https://youtube.com/playlist?list=PLcIpBb4raSZEMosUmY8KpxPWtjKRMSmNx

# Documentation

For more details refer to the "AWSGoat.pdf" PDF file. This file contains the slide deck used for presentations.

# Screenshots

Blog Application HomePage

![5](https://user-images.githubusercontent.com/65826354/179526784-2a1d7023-5c6f-4cfb-97b7-74b572b12829.png)

Blog Application Login Portal

![6](https://user-images.githubusercontent.com/65826354/179526792-2dad1a3b-f871-4128-a82b-9d1ba3b334f5.png)

Blog Application Register Page

![7](https://user-images.githubusercontent.com/65826354/179526796-fa4fa422-ffb5-4ff4-a2eb-1468e9c81fd6.png)

Blog Application Logged in Dashboard

![8](https://user-images.githubusercontent.com/65826354/179526801-6eb85d63-b7df-4fac-98f6-8afb834d2f49.png)

Blog Application User Profile

![9](https://user-images.githubusercontent.com/65826354/179526804-78f87773-965d-4eee-a5bf-fb1c1d448234.png)

## Contribution Guidelines

* Contributions in the form of code improvements, module updates, feature improvements, and any general suggestions are welcome. 
* Improvements to the functionalities of the current modules are also welcome. 
* The source code for each module can be found in ``modules/module-<Number>/src`` this can be used to modify the existing application code.

# License

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License v2 as published by the Free Software Foundation.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

# Sister Projects

- [AzureGoat](https://github.com/ine-labs/AzureGoat)
- GCPSheep (Coming Soon)
- [PA Toolkit (Pentester Academy Wireshark Toolkit)](https://github.com/pentesteracademy/patoolkit)
- [ReconPal: Leveraging NLP for Infosec](https://github.com/pentesteracademy/reconpal) 
- [VoIPShark: Open Source VoIP Analysis Platform](https://github.com/pentesteracademy/voipshark)
- [BLEMystique](https://github.com/pentesteracademy/blemystique)
