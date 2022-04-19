# cross-account-cloudformation

Customer will create stack using this cloudformation template; allowing Admin access to SUDO. This will send an SNS notification to a custom lambda in the SUDO account.

## Deploy stack using aws cli

```bash
aws cloudformation create-stack --stack-name sudo-access \
--template-body file://sudo-access-template.yml \
--parameters file://parameters.json \
--capabilities CAPABILITY_NAMED_IAM \
--region us-east-1
```
