# escape=`

ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ARG NODE_VERSION

USER ContainerAdministrator

WORKDIR C:\downloads
RUN curl.exe -sS -L -o node.zip https://nodejs.org/dist/v%NODE_VERSION%/node-v%NODE_VERSION%-win-x64.zip
    
RUN tar.exe -xf node.zip -C C:\
RUN move C:\node-v%NODE_VERSION%-win-x64 c:\node
RUN del node.zip

RUN SETX /M PATH "%PATH%;C:\node"

USER ContainerUser

RUN npm install -g npm@latest && npm install -g wrangler

WORKDIR C:\project
EXPOSE 8787

CMD [ "node.exe" ]