# Remote-State

I created this set of templates because IaC. So, if your Terraform remote state dependencies are not codified, you're doing it incorrectly.

### Getting Started

1. Clone the repository.
2. Update the `remote-state-params.json` file.
3. Create your S3 bucket to store your CloudFormation templates.
4. Upload the applicable files into your S3 bucket.
5. Update the `remote-state-orch.json` file with the applicable URLs to your files in S3.
6. Kick off a CloudFormation create stack.

```shell script
aws --profile $profileName cloudformation $operationName \
   --region $regionName \
   --stack-name $stackName \
   --template-body $templateBody \
   --parameters $paramFile \
   --capabilities CAPABILITY_NAMED_IAM
```

---

### Reference

As a reference, below is a list of variables/values needed to run the template.

###### remote-state-params.json
ParameterKey | ParameterValue
--- | ---
iamPolicyDesc | As per your needs
iamPolicyName | As per your needs
iamRoleName | As per your needs
iamRoleDesc | As per your needs
iamRoleSvc | As per your needs
iamRoleAction | As per your needs
iamMgdPolArn | As per your needs
iamMaxSesDur | As per your needs
envName | As per your needs
regName | As per your needs
roleName | As per your needs
iamInstProfName | As per your needs
iamGroupName | As per your needs
iamUserName | As per your needs
kmsKeyDesc | As per your needs
kmsKeyName | As per your needs
alias/cloudorch-key | As per your needs
kmsEnable | As per your needs
kmsRotation | As per your needs
kmsPolicySid | As per your needs
kmsPolicyAction | As per your needs
kmsUsage | As per your needs
kmsPendingDays | As per your needs
bucketName | As per your needs
boolTrue | As per your needs
boolFalse | As per your needs
s3Versioning | As per your needs
sseAlgo | As per your needs
dynTblName | As per your needs
dynAttrName | As per your needs
dynAttrType | As per your needs
dynBillMode | As per your needs
dynSchemaKeyType | As per your needs