## Iniciar os teste com o Minikube.

```bash
minikube start --driver=none
```

```bash
minikube addons enable metrics-server
```

```bash
kubectl apply -f https://raw.githubusercontent.com/roelal/minikube/5093d8b21c0931a6c63fa448538761b4bf100ee0/deploy/addons/ingress/ingress-rc.yaml
kubectl apply -f https://raw.githubusercontent.com/roelal/minikube/5093d8b21c0931a6c63fa448538761b4bf100ee0/deploy/addons/ingress/ingress-svc.yaml
```

```bash
minikube addons enable metallb
```

```bash
minikube ip
```

*OBS.: Pegar o endereço IP e setar no "Start" e "End" do "Load Balancer" das configurações do comando metallb.*

```bash
minikube addons configure metallb
```

- *Enter Load Balancer Start IP: 192.168.15.3*
- *Enter Load Balancer End IP: 192.168.15.3*


## Caso preicise limpar o Minikube e iniciar do zero, executar o stop e o delete!

```bash
minikube stop
```

```bash
minikube delete
```
