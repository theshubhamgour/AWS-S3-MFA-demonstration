## Configuring AWS MFA profile for S3 MFA delete
```
aws configure --profile root-mfa-delete-demo
```

## Enable MFA on S3 
```
aws s3api put-bucket-versioning --bucket <bucket-name> --versioning-configuration Status=Enabled,MFADelete=Enabled --mfa "arn:aws:iam::123456789012:mfa/your-username 654321"
```

## Disable MFA on S3
```
aws s3api put-bucket-versioning --bucket <bucket-name> --versioning-configuration Status=Enabled,MFADelete=Disabled --mfa "arn:aws:iam::123456789012:mfa/your-username 654321"
```
