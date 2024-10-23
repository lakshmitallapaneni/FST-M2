#specify base container
FROM node:18-alpine
#creating working directory
WORKDIR /usr/app
#copying json packages to current directory
COPY package.json ./
#Install the depenecies clear	
RUN npm install
#copying all files under the current folder to current directory
COPY ./ /usr/app
#start the server
CMD ["npm","start"]
