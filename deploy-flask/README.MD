

1. Create a Service Principal: create a service principal in Azure that has access to the ACR


az ad sp create-for-rbac --name acrServicePrincipal --role acrpush --scopes /subscriptions/4c321266-69a0-401d-8fa7-124c5298816e/resourceGroups/QPP-ACR-RG/providers/Microsoft.ContainerRegistry/registries/qppacr

{
  "appId": "58406571-a616-43c5-82a8-ca7dc9306e7f",
  "displayName": "acrServicePrincipal",
  "password": "p-58Q~YKBUR_OrHpvBB6trnVMsHos5rqIHC_sbA-",
  "tenant": "b9c70ecd-4404-43a8-8924-be54c3f81ae1"
}

2. Create a Kubernetes Secret: Create a secret with the service principal's details:

kubectl create secret generic azure-creds --from-literal=clientId=58406571-a616-43c5-82a8-ca7dc9306e7f --from-literal=clientSecret=p-58Q~YKBUR_OrHpvBB6trnVMsHos5rqIHC_sbA- --from-literal=tenantId=b9c70ecd-4404-43a8-8924-be54c3f81ae1
