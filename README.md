<<<<<<< envoy
## Kubernetes Volumes

To demonstrate Kubernetes Volumes in this branch we added a new service the SA-Feedback. For newcomers to Kubernetes or that want to understand this Microservice application please read up in: [Learn kuberntes in under 3 hours: A detailed guide to Orchestrating Containers](https://medium.freecodecamp.org/learn-kubernetes-in-under-3-hours-a-detailed-guide-to-orchestrating-containers-114ff420e882)

### The SA-Feedback service

Stores users feedback if the Sentiment Analysis was correct or not in a SQLite database. In a real app it would be used to train the Sentiment Analysis model, in our case we use it as an opportunity to showcase **Kubernetes Volumes**.

#### Setting up the service

**Prerequisite:** install `dotnet core 2.1` 

To run the app execute the command below (from the directory of sa-feedback)

```
$ dotnet run
```

For additional technical information follow the README in [SA-Frontend directory](sa-feedback\README.md)
=======
This repository contains the source files needed to follow the series [Kubernetes and everything else](https://rinormaloku.com/series/kubernetes-and-everything-else/) or summarized as an article in [Learn Kubernetes in Under 3 Hours: A Detailed Guide to Orchestrating Containers](https://medium.freecodecamp.org/learn-kubernetes-in-under-3-hours-a-detailed-guide-to-orchestrating-containers-114ff420e882)

To learn more about Kubernetes and other related topics check the following examples with the **Sentiment Analysis** application:

* [Kubernetes Volumes in Practice](https://rinormaloku.com/kubernetes-volumes-in-practice/):
* [Ingress Controller - simplified routing in Kubernetes](https://www.orange-networks.com/blogs/210-ingress-controller-simplified-routing-in-kubernetes)
* [Docker Compose in Practice](https://github.com/rinormaloku/k8s-mastery/tree/docker-compose)
* [Istio around everything else series](https://rinormaloku.com/series/istio-around-everything-else/)
* [Simple CI/CD for Kubernetes with Azure DevOps](https://www.orange-networks.com/blogs/224-azure-devops-ci-cd-pipeline-to-deploy-to-kubernetes)
* Envoy series - to be added!
>>>>>>> master
