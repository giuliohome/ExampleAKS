# Deploy the Bike Sharing sample application to Azure Kubernetes Service

*Bike Sharing* is a microservices-based sample application written in a variety of languages as a good base for users to try our debugging in their language of choice.

![Application Architecture](https://github.com/microsoft/mindaro/raw/master/samples/BikeSharingApp/applicationcomponents.png)


## Helm v3 

```
helm install bikesharing . --dependency-update --namespace dev-bikesharing --atomic --wait 
```

# Online Demo

Enjoy the AKS cloudnative demo [online](http://dev-bikesharing.bikesharingweb.giuliohome.com/), thanks to the dns of Cloudflare site hosting



## Documentation

We have guides available in VS Code and Visual Studio.

* [Visual Studio Code Quickstart](https://aka.ms/bridge-to-k8s-vscode-quickstart)
* [Visual Studio Quickstart](https://aka.ms/bridge-to-k8s-vs-quickstart)
