ENV NO_UPDATE_NOTIFIER=1
EXPOSE 3000
EXPOSE 5000
ADD . .

# Comando para instalar as dependências
RUN npm install --silent --loglevel=error

# Imagem base derivada do Node
FROM node

# Diretório de trabalho
WORKDIR /app

# Comando para copiar os arquivos para a pasta /app da imagem
COPY . /app

# Comando para inicializar (executar) a aplicação
CMD ["node", "/app/services/shipping/index.js"]