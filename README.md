# aws-cli-s3-command
Manaage S3 bucket by aws cli command 

- Remove all bucket at once  forcefully
```git
for bucket in $(aws s3 ls | awk -F" " '{print $3}'); do aws s3 rb "s3://${bucket}" --force; done
```
