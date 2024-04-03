# Kubernetes Resume Challenge

This repository holds the code for my solution to Forrest Brazzeal/KodeKloud's Kubernetes Resume Challenge, which I built on Google Cloud's GKE.

## Objectives

Deploy a scalable, consistent, and highly available e-commerce website with a database to Kubernetes using a cloud provider of your choosing.

## Locations

The web-app directory contains the files forked from the given KodeKloud repository. Extra CSS files were created for the dark mode feature, and the index.php file was slightly edited to check for an environment variable and change the CSS files depending on the value.

The docker-compose-test directory holds Docker files used for experimenting with the e-commerce app, pre-deployment to Kubernetes.

The kubernetes-files directory holds K8s files used for the initial deployment of the e-commerce app to GKE.

The helm-ecom-app directory contains the final files used for the Helm deployment of the e-commerce app to GKE.

## Images

I have since taken the cluster down to save credits, but the following images show the final app accessed through the load balancer.

Normal:
<img src="images\Normal.png"/>
Dark Mode:
<img src="images\Dark Mode.png"/>

## Blog

[Dev.to](https://dev.to/bit-of-a-git/kubernetes-resume-challenge-google-cloud-gke-395l)

## Reflection

This was a very enjoyable challenge that allowed me to use knowledge gained both from work projects and the Cloud Resume Challenge. Although I had Kubernetes experience I did not have experience with Helm or HPA. After this challenge, I am really interested in exploring Helm further and will hopefully have more opportunities to use this and Kubernetes in the future.

## Automation and CI/CD

Upon a push to the main branch, a GitHub Actions job runs to build a Docker image. Next, a job runs to authenticate to GCP and deploy the app using Helm.