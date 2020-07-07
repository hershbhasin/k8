```bash
#check images
docker images
#enable kubernetes in docker desktop

nano ~/.bash_profile
#alias
alias k=kubectl

#check context
kubectl config get-contexts
k get nodes

#install extensions
kubernates /Microsoft... 
this will also install the yaml extension. Get Yamlversion 0.4.1 as latest version has a bug that prevents kubernates extension from generating YAML files.
--click the gear ico & install another version

# add a file deployment.yaml
--type deploy and choose scaffold snippet

#Fill
metadata/name: hello-world
template/labels/app: hello-world-pod
spec/selector/matchlabel: hello-world-pod

spec/container: hello-world-container
spec/container/image: helloworld:v1
ports/containerport: 80

#apply
k apply -f deployment.yaml

k get deployments
k get pods
k get logs podname


# forwatd: pod
kubectl port-forward pod/mypod 8080:80
#forward: deployment
kubectl port-forward deployment/<deployment-name> 8080:80
k port-forward deployment/helloworld 8080:80 -n hb-namespace

#Service
new file: service.yaml
--service and scaffold

# fill
metadata/name: hello-world-service
spec/selecter/app: hello-world-pod
ports/port: 8080 (external)
ports/targerPort: 80

Add (by typing)
type: LoadBalancer

k apply -f service.yaml
k  get services

http://localhost:8080/WeatherForecast

#aws
externalip/WeatherForecast

a1e542fad2c21400a9f13e67af730f6c-2123300240.us-east-1.elb.amazonaws.com/WeatherForecast
```

