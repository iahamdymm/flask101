
kubectl apply -f https://raw.githubusercontent.com/tektoncd/catalog/main/task/git-clone/0.4/git-clone.yaml



kubectl create secret docker-registry acr-credentials --docker-server=qppacr.azurecr.io  --docker-username=41cdeb37-6726-4edf-97c9-b30d033fa649 --docker-password=84E8Q~ZYMbh.nhhvW8vXlCfreeE3YDe9zmcd1aQP   --docker-email=mtaha@pp.gov.qa
