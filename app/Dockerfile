# imagem
FROM node:12-alpine
# diretorio de trabalho
WORKDIR /app
# copia o package para subir as dependencias primeiro
COPY package.json .
# executar a instalaçao dependencias da app na construicao da imagem
RUN apk add --no-cache python2 g++ make
# instalacao do yarn
RUN yarn install --production
# copiar arquivos da pasta atual para uma pasta do workdir  
COPY . .
# executar a aplicaçao apos construcao
CMD ["node","src/index.js"]
# expor a porta do container
EXPOSE 3000 
# 