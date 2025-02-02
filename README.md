# Cloudmart Application
This project was done as part of a 5-day training with Jean Rodrigues on MultiCloud DevOps & AI Bootcamp. We leveraged AI as well to generate templates as well as incorporate a chatbot into the application. My key takeaways from a project like this are:
- Be organized and methodical:  It is very easy to lose track of what goes where and I had to learn the hard way. But at the same time, troubleshooting is also part of the process and there is a degree of satisfaction when you resolve an issue. So keep grinding.
- Little by little:  As you keep adding to the application, understand the current architecture and visualize its future state. This will help you connect the dots and figure out what happens when trouble appears
- Student mentality:  Understand that it takes years to get familiar with all of this and that mistakes will happen, but the key thing is to remain with an open mind, always learning and upskilling

## Part 1: Provisioning resources in AWS with Terraform
- Using Claude AI as an assistant, a Terraform script was created to provision unique S3 buckets and DynamoDB tables
- To do this, we connected to an EC2 instance, installed Terraform, copied the script onto a file named main.tf, and then ran the terraform commands init. plan, and apply to run the script and provision the resources

## Part 2: Docker and Kubernetes
- The cloudmart application was containerized and deployed on a AWS EKS cluster
- The integration with DynamoDB tables was validated
- ECR registries were created to push Docker images to run the application
- Use kubectl to deploy the app on EKS
- Configure IAM roles to ensure proper permissions

## Part 3: Automate Deployment with a CI/CD Pipeline
- Prepared this Github repository, remote clone it into the EC2 instance, and pushed the necessary files via git push origin main, and used an authentication token to connect the AWS service with Github
- Configure AWS CodePipeline to automate deployment
- Configure environment setting environment variables to eliminate hardcoding URIs into the Dockerfiles and buildspec files
- Configure IAM roles to ensure proper permissions

## Part 4: Build AI Agents with Amazon Bedrock and OpenAI
- Once again use Terraform to assist in the creation of a script to provision resources including IAM roles, DynamoDB connectivity, and Lambda functions
- Created an AI Agent on Bedrock to handle product recommendations
- Set up OpenAI API to handle customer support

