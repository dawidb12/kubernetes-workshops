## Testing

First apply all the YAML configuration files.

```sh
kubectl apply -f 001-httpbin.yaml
kubectl apply -f 002-echo-server.yaml
kubectl apply -f 003-nginx-configmap.yaml
kubectl apply -f 004-nginx.yaml
```
Then expose the application outside the vagrant VM.

```sh
k port-forward --address=0.0.0.0 svc/nginx-proxy 8080:80 -n proxy-test
```

Enter in your web browser: http://<ip_of_a_vm>:8080/httpbin/ip or http://<ip_of_a_vm>:8080/echo