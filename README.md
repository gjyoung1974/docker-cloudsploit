# docker-cloudsploit
dockerized-cloudsplot, CloudSploit is a security and configuration scanner that can detect hundreds of threats in your AWS account. Don't let a single misstep compromise your entire infrastructure.     

Cloudsploit is an AWS Account monitoring solution

- Monitor security relevant configuration    
- Monitor configuration regulatory compliance levels    
[CloudSploit](https://cloudsploit.com)      


Set up an AWS IAM "Service Account" user    

Run this like:

Either:

```
$ docker run -e scan_username=${scan_username} -e scan_password=${scan_password} quay.io/verygoodsecurity/cloudsploit
```
username and password are AWS KeyID and Secret key for the service account IAM user

use somthing like KIAM to use an instance profile identity for the pod/job         


