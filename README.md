Version
Terraform v1.3.6

---
![Screenshot 2023-06-28 at 10 31 37](https://github.com/Lvchnk88/test_task_IT-Craft/assets/53876938/1ddf78eb-c4fa-41c6-a33c-05f286a1f59e)


### Clone repository


```bash
git clone https://github.com/Lvchnk88/test_task_IT-Craft.git
cd test_task_IT-Craft
```

### Run this commands to authenticate in AWS:

```bash
export AWS_ACCESS_KEY_ID= < Your aws access key >
export AWS_SECRET_ACCESS_KEY= < Your aws secret access key >
```

### Run Terraform commands to deploy the infrastructure:

```bashgit 
cd terraform
terrafirm init
terraform plan
terraform apply
```

###  After the deployment is complete, you will see the output with the IP address

```bash
ec2_global_ips = [
  [
    "52.207.129.65",
  ],
]
```

---
###TEST DESCRIPTION

#### 1 Theoretical part
You need to create and explain a detailed plan with diagrams for the infrastructure migration from on-premise hosting to AWS Cloud.
On premise infrastructure:
```
- Self-hosted Kubernetes clusters in Open Stack with 10 nodes: 128 GB RAM/64 CPU each;
- Database servers for MySQL hosting with 5 nodes: 256 RAM/128 CPU each;
- NAS storage for static files: 5 TB
- HAProxy for load balancing between clusters;
- Elasticsearch cluster + Kibana + Logstash for logging;
- Redis cluster with 3 nodes (Database size 50gb);
```
Diagram have shown the most cost-optimized solution in AWS with services explanation, and it’s usage.


#### 2 Technical part
```
Develop Terraform manifests for EC2 instance configuration - during instance
creation should be installed nginx web server on the instance through user data and passed index.html page with “Hello world!”. 
All variables should be defined in variables.tfvars (set of variables on your choice).

Definition of done
After terraform apply, I should be able to view “hello world” page using instance public IP.
```