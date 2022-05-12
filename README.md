## Minikube + HELM

### Pré-requesitos

1º Aplicação:

- docker
- conntrack
- sudo
- minikube
- kubectl
- helm

2º Configuração

- 4 GB de Memória RAM;
- 2 Nucleos (Processador).

### Download e Install minikube:

```bash
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube
```
[URL-Minikube](https://minikube.sigs.k8s.io/docs/start/)


### Iniciar os teste com o Minikube.

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

### Instalar HELM

```bash
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3
chmod 700 get_helm.sh
./get_helm.sh
```

### Caso preicise limpar o Minikube e iniciar do zero, executar o stop e o delete!

```bash
minikube stop
```

```bash
minikube delete
```
