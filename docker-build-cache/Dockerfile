## Specify a base image
FROM node:alpine

# workdir dizini yoksa yaratilacaktir ve current dir yapilacak
WORKDIR /use/app 

### Install some dependencies

# asagidaki gibi once package.js i kopyalayip npm install yapiyoruz. Boylelikle RUN npm install sonuna kadar cache leniyor 
# ve tekrar build islemi sirasinda bize hiz kazandiriyor
COPY ./package.js ./
RUN npm install
COPY ./ ./

## Default command
CMD ["npm", "start"]
