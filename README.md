# Helm Setup

## Local Setup

Requires minikube

Steps: 

 1. Start minikube in a VM (for ingress support) `minikube start --vm=true`
 2. Enable ingress support: `minikube addons enable ingress`
 3. Add the ghcr secret: `kubectl create secret docker-registry oec --docker-server=https://openexperiencecloud.jfrog.io/docker`
 4. Get minikube's IP: `minikube ip`
 5. Update /etc/hosts with entries for `www.openexperience.local` and `cms.openexperience.local` for minikube's IP\
 6. Install the helm chart with: `heml install main ./src/main/helm`