## Download e Install minikube:

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
[URL-Minikube](https://minikube.sigs.k8s.io/docs/start/)



## Iniciar os teste com o Minikube.

```bash
minikube start --driver=none
```

```bash
minikube addons enable metrics-server
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
