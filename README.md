# Instação do Ingress Controller

## Pre-requisitos

As etapas estão numeradas sequencialmente, atente para as ativdade de criação de 'POD' que dependera da conclusão para dar continuidade.

## 1. Criando Namespace, SA, Secret e ConfigMap.

Inicie então a execução pelo diretório common.

1. Criando os namespaces

  ```
  kubectl create -f common/0_0ns.yaml
  ```

1. Criando os serviceAccount
  ```
  kubectl create -f common/0_0sa.yaml
  ```
1. Criando uma secret com um certificado TLS e uma key para o servidor default no NGINX
  ```
  kubectl create -f common/0_1default-server-secret.yaml
  ```
1. Criado um configmap
  ```
  kubectl create -f common/0_3nginx-config.yaml
  ```

## 2. Configurando RBAC
1. Alterando o diretório
  ```
  kubectl create -f rbac/1_0rbac.yaml
  ```
