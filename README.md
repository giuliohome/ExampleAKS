# Deploy the Bike Sharing sample application to Azure Kubernetes Service

*Bike Sharing* is a microservices-based sample application written in a variety of languages as a good base for users to try our debugging in their language of choice.

![Application Architecture](https://github.com/microsoft/mindaro/raw/master/samples/BikeSharingApp/applicationcomponents.png)


## Helm v3 

Instead of enabling the ingress controller (notice that the level 7 application gateway is quite expensinve in Azure), we can use [the IP and DNS label](https://docs.microsoft.com/en-us/azure/aks/ingress-static-ip?tabs=azure-cli#ip-and-dns-label).


```
helm install nginx-ingress nginx-stable/nginx-ingress --create-namespace --namespace dev-bikesharing --set controller.service.loadBalancerIP=52.154.208.72
helm install bikesharing . --dependency-update --namespace dev-bikesharing --atomic --wait 
```

# Online Demo

I can put the AKS cloudnative demo [online](http://dev-bikesharing.bikesharingweb.giuliohome.com/), thanks to the dns of Cloudflare site hosting, but I'll have to destroy it to ensure that the assets don't accumulate unwanted costs while sitting unused. It can be easily recreated via [terraform](https://docs.microsoft.com/en-us/azure/developer/terraform/create-k8s-cluster-with-tf-and-aks) and helm.



## Documentation

We have guides available in VS Code and Visual Studio.

* [Visual Studio Code Quickstart](https://aka.ms/bridge-to-k8s-vscode-quickstart)
* [Visual Studio Quickstart](https://aka.ms/bridge-to-k8s-vs-quickstart)
