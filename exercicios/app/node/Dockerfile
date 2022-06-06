# De onde deve ser pega a imagem e a versão. Nesse caso do repositório padrão do Docker, a imagem do node

# FROM node:alpine
FROM daveamit/node-alpine-grpc

# Autor/Mantenedor
MAINTAINER Jonathan Baraldi

# Definir diretório de trabalho
RUN mkdir -p /src 
WORKDIR /src
ADD . /src

# Prover camada de cached para os módulos do Node
RUN npm install

# Instalar MariaDB SQL e rodar o script para injetar o SQL
RUN npm install mysql

# Expor porta 80
EXPOSE  8080

# Rodar o app usando nodemon
CMD ["node", "/src/index.js"]
