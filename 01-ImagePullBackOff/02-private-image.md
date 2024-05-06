# Private Image

We will learn how to create a Pod that uses a Secret to pull an image from a private container image registry or repository. 

### Create a Secret by providing Docker credentials on the command line

```
kubectl create secret docker-registry demo --docker-server=<your-registry-server> --docker-username=<your-name> --docker-password=<your-pword> --docker-email=<your-email>
```

### Create a Secret by providing AWS ECR credentials on the command line

```
kubectl create secret docker-registry  \
  --docker-server=${AWS_ACCOUNT}.dkr.ecr.${AWS_REGION}.amazonaws.com \
  --docker-username=AWS \
  --docker-password=$(aws ecr get-login-password) \
  --namespace=default
```



My secret
kubectl create secret docker-registry demo --docker-server=https://index.docker.io/v1/ --docker-username=chaitanya795 --docker-password=chaitanya@9 --docker-email=chaitanyareddycharla123@gmail.com -n chaitanya
