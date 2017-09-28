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