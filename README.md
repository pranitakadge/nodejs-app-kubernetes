# nodejs-app-kubernetes

###create a nodejs docker image

```
cd nodejs application
docker build -t nodejs .
docker tag nodejs aws_account_id.dkr.ecr.region.amazonaws.com/nodejs:latest
docker push aws_account_id.dkr.ecr.region.amazonaws.com/nodejs:latest
```

###create a priority class

```
kubectl create -f priorityclass.yaml	
```

###create a deployment

```
kubectl create -f deployment.yaml	
```

###create horizontal pod autoscaler

```
kubectl create -f hpa.yaml	
```

###create a service

```
kubectl create -f service.yaml
```
