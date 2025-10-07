## Testing

First check the minikube ip:

```sh
minikube ip
```

Copy the ip address and paste it to /etc/hosts:

```sh
<minikube_ip_address>   ingress.test
```

Then run the command

```sh
curl http://ingress.test/httpbin/ip
```

or

```sh
curl http://ingress.test/echo
```