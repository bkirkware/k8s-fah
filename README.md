# k8s-fah
Run folding@home on Kubernetes.

The folding project recently added support for the Corona virus (2019-nCoV). 

https://foldingathome.org/2020/02/27/foldinghome-takes-up-the-fight-against-covid-19-2019-ncov/

This is a quick deployment that lets you run this on Kubernetes, should you have any spare cluster-power you'd like to donate. 

&nbsp;

# Install

1. Customize ```config.xml``` for your folding@home username and team ID.
1. Build the docker image<br>```docker image build . --tag fah```
1. Push the image to a container registry.<br>```docker push fah harbor.pks.kirklab.io/fah/fah```
1. Customize ```folding.yaml``` to change number of replicas, container location, and resource limits.
1. Deploy to Kubernetes<br>```kubectl apply -f folding.yaml```  