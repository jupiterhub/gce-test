# Jupiter's Conclusion
Google cloud platform is very easy to use covering different features from clusters, vm instances, load balancing, dns management, persistent storage, and makes upgrading very easy with Kubernetes integration.

In terms of pricing the cheapest instance is a micro (only free if in US, $4/month) and an n1-standard ($24/month) which has a decent spec. When you start running clusters in containers that is multiplied by the number of nodes you deploy on your cluster

There is also a preemptible instance which terminates after 24hours, with this you can save about 70% of your monthly instance cost. However it is not covered by SLA, and can terminate anytime. Good for batches but not for frontfacing applications

# gce-test
- Trying out Google Container Engine, deploying using Kubernetes

## guestbook
- Contains the Manifests to deploy to Google Cloud Containers
- https://cloud.google.com/container-engine/docs/tutorials/guestbook

## wordpress-persistent-disk
- Wordpress with Mysql + PersistentDisk
- Persistent storage means that the file stored lives even when the container dies
- https://cloud.google.com/container-engine/docs/tutorials/persistent-disk/

## http-balancer
- An alternative to LoadBalancer (TCP) defined in a Service
- https://cloud.google.com/container-engine/docs/tutorials/http-balancer

## pubsub
- Cloud Pub/Sub using Service Accounts
- It is recommended to create a new service account instead of using a default
- https://cloud.google.com/container-engine/docs/tutorials/authenticating-to-cloud-platform

## domain-test
- Set domain name for a given static IP using an Ingress (Service is not recommended because it uses TCP)
- check the ```helloweb-ingress.yaml``` it defines both an Ingress and a Service in 1 file
- Requires you to have an actual domain to test
- https://cloud.google.com/container-engine/docs/tutorials/configuring-domain-name-static-ip 

## node-pool
- Configure different settings for the nodes created by the cluster
- Node pools, cordon it and then remove. The pods will automatically be relocated at the new pool
- https://cloud.google.com/container-engine/docs/tutorials/migrating-node-pool

## jenkins-cd
- Deploying Jenkins container using Compute Image and Disk then mouning to the container
- https://cloud.google.com/solutions/jenkins-on-container-engine-tutorial

## Continuous Delivery
- A chart explaining continuous deployment is available at the link below
- https://cloud.google.com/solutions/continuous-delivery-jenkins-container-engine
- Skip cleanup. Follow this for Continuous Delivery: https://cloud.google.com/solutions/continuous-delivery-jenkins-container-engine