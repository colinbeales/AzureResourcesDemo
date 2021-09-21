# AzureResourcesDemo

A simple Java spring web application deployable onto Azure AKS via Azure Container Registry.

Two GitHub Actions workflows are in-place:
- AKS.yml - This sets up all Azure resources required for the demo including Azure Container Registry and AKS with AKS given permissions to pull images from the newly created registry with a system identity.
- build.yml - This uses Maven to build our spring application, before packaging into a container and pushing this into the Azure Container Registry. Once in the registry AKS can deploy the code onto pods hosted on the cluster.

