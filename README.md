## Configuring AWS MFA profile for S3 MFA delete
```
aws configure --profile root-mfa-delete-demo
```

## Enable MFA on S3 
```
aws s3api put-bucket-versioning --bucket <bucket-name> --versioning-configuration Status=Enabled,MFADelete=Enabled --mfa "arn-of-mfa-device mfa-code" --profile root-mfa-delete-demo
```

## Disable MFA on S3
```
aws s3api put-bucket-versioning --bucket <bucket-name> --versioning-configuration Status=Enabled,MFADelete=Disabled --mfa "arn-of-mfa-device mfa-code" --profile root-mfa-delete-demo
```
