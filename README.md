# Jupiter's Conclusion
TBD

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