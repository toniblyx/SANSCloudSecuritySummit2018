Tools and code used during my talk at SANS Cloud Security Summit 2018 in San Diego
========

[__Forensics as a Service: IRDF in the Cloud__](https://www.sans.org/event/cloud-security-summit-2018/summit-agenda)

February 19th, 2018

------

## Presentation in PPTX format
See file __Forensics-as-a-Service-Toni-de-la-Fuente-SanDiego-2018.pptx__ in this repo. You can easier use all links in the __References__ slide. All links are also below in this README. 

## Some commands used during my Demo
1- ./prowler -c forensics-ready

2- Incident Response aws_ir (Tools Instance): 

[Demo Video instance compromise](https://www.youtube.com/watch?v=-dnljYRMMsU)

[Demo Video key compromise](https://www.youtube.com/watch?v=-OY0L4BMyLY)

* ```aws_ir --bucket-name ir-caseXXXXX --examiner-cidr-range IP.AD.DR.ES/S instance-compromise \
  --target i-12345678901234 --user ubuntu --ssh-key ~/key-toplay.pem \
  --plugins gather_host,snapshotdisks_host,tag_host,examineracl_host,get_memory,isolate_host,stop_host```
* ```volatility -f IP-2017-02-23T02\:15\:48-mem.lime imageinfo```
* ```volatility -f IP-2017-02-23T02\:15\:48-mem.lime --profile=Ubuntu14043 linux_pslist```
* ```aws_ir key-compromise --access-key-id AKIAJTEST```

4- Hardening template, SecurityMonkey 

[Demo Video](https://www.youtube.com/watch?v=xeAfXc9rIwU)

* hardening template from [here](https://github.com/awslabs/aws-security-benchmark/tree/master/aws_cis_foundation_framework)
* run prowler (ssh to Tools Instance, aws-cli must be configured)
* ```cd /opt/aws-cis-security-benchmark```
* ```./prowler```
* show securitymonkey

## All links and tools mentioned during the talk 

* https://github.com/dagrz/aws_pwn
* Serverless Security https://www.rsaconference.com/writable/presentations/file_upload/asd-f01_serverless-security-are-you-ready-for-the-future.pdf
* https://github.com/devsecops/lambhack
* https://blyx.com/2016/03/11/forensics-in-aws-an-introduction/
* https://blyx.com/2016/06/16/cloud-forensics-caine7-on-aws/
* https://s3-us-west-2.amazonaws.com/threatresponse-static/us-16-Krug-Hardening-AWS-Environments-and-Automating-Incident-Response-for-AWS-Compromises-wp.pdf
* https://aws.amazon.com/premiumsupport/trustedadvisor/
* https://aws.amazon.com/cloudtrail/
* https://azure.microsoft.com/en-us/resources/videos/azure-operational-insights-overview/
* https://aws.amazon.com/cloudformation/
* https://aws.amazon.com/config/
* https://github.com/Alfresco/prowler
* https://github.com/nccgroup/Scout2
* https://github.com/Netflix/security_monkey
* https://github.com/Netflix/edda
* https://github.com/Netflix/Fido
* https://github.com/capitalone/cloud-custodian
* https://github.com/awslabs/aws-security-benchmark
* https://github.com/cloudsploit
* https://github.com/widdix/aws-cf-templates/tree/master/security#account-password-policy
* https://github.com/jantman/awslimitchecker
* https://blogs.msdn.microsoft.com/azuresecurity/2017/01/04/get-hands-on-experience-with-oms-security-with-oms-suite-experience-center/
* https://github.com/spotify/gcp-audit
* https://github.com/awslabs/git-secrets
* https://wazuh.com 
* https://aws.amazon.com/macie/
* https://github.com/andresriancho/nimbostratus
* https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/log-analytics/log-analytics-overview.md
* https://azure.microsoft.com/en-us/resources/videos/azure-operational-insights-overview/
* https://github.com/mwrlabs/Azurite
* https://github.com/azsdk/azsdk-docs
* https://github.com/Azure/AzureStack-Tools
* https://www.sans.org/reading-room/whitepapers/cloud/digital-forensic-analysis-amazon-linux-ec2-instances-38235


