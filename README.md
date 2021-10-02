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
