#base Image
FROM node:9.6.1

#set working dir
RUN mkdir /usr/src/app
WORKDIR /usr/src/app

#add usr src app node_modules to the $PATH
ENV PATH /usr/src/app/node_modules/.bin:$PATH

#install cache and app dependencies
#Copy the package.json file from local to docker
COPY package.json /usr/src/app/package.json
RUN npm install
RUN npm install react-scripts@1.1.1 -g 

#start app
CMD ["npm","start"]
