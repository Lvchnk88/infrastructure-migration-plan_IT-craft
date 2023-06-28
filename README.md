Version
Terraform v1.3.6


TEST DESCRIPTION
----------------

### 1 Theoretical part
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


### 2 Technical part
```
Develop Terraform manifests for EC2 instance configuration - during instance
creation should be installed nginx web server on the instance through user data and passed index.html page with “Hello world!”. 
All variables should be defined in variables.tfvars (set of variables on your choice).

Definition of done
After terraform apply, I should be able to view “hello world” page using instance public IP.
```