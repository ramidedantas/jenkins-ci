# Usando imagem Ubuntu como base, última versão (latest) 
FROM ubuntu:latest 
# Atualizando a base de pacotes de software 
RUN apt-get update 
# Instalando Gradle e OpenJDK (-y força a instalação sem perguntar) 
RUN apt-get install -y gradle openjdk-11-jdk 
# Copiando a pasta do projeto para dentro da imagem 
COPY ./ /Jenkins-CI/ 
# Mudando o diretório de trabalho para o diretório do projeto 
WORKDIR /Jenkins-CI/ 
# Rodando o gradle. Rodado ao executar docker start. 
CMD gradle build 