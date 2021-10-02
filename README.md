# Conversao Temperatura (Iniciativa Kubernetes)

## Passo-a-passo do processo de montagem e execução da aplicação utilizando Docker
  1 - Criar arquivo Dockerfile dentro do diretório: /src, contendo as instruções para criação da imagem da aplicação   
  2 -  Fazer o build da imagem da aplicação:
  ```bash 
  docker image build -t brunocesar96/conversao-temperatura:v1 .
  ```
  3 - Rodar aplicação em um container Docker:
  ```bash 
  docker container run -d -p 8080:8080 brunocesar96/conversao-temperatura:v1
  ```
## Passo-a-passo do processo de implementação do projeto no Kubernetes
  Pré requisitos:    
  - Arquivo Dockerfile já configurado no projeto
  - Cluster já instanciado para aplicação do kubernetes. Para confirmar:
  ```bash
  docker container ls
  ```
  
  1 - Criar diretório ks8 na raíz do projeto
  ```bash
  mkdir ks8
  ```
  2 - Criar e configurar o arquivo de deployment
  
  3 -  Fazer o build da imagem da aplicação:
  ```bash 
  kubectl apply -f deployment.yaml
  ```
  4 - Verificar configuração do kubernetes aplicada:
  ```bash 
  kubectl get all
  ```  

