
Buildando a imagem Atlassian teste: `docker build -t soso/selfhostedagent .`

Rodando a imagem Atlassian para container self-hosted local: `docker container run -d -v /tmp:/tmp -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/docker/containers:/var/lib/docker/containers:ro --name runner-customizado soso/selfhostedagent:latest`

Links úteis: 

[https://support.atlassian.com/bitbucket-cloud/docs/runners/](https://support.atlassian.com/bitbucket-cloud/docs/runners/)

[https://support.atlassian.com/bitbucket-cloud/docs/use-your-docker-images-in-self-hosted-runners/](https://support.atlassian.com/bitbucket-cloud/docs/use-your-docker-images-in-self-hosted-runners/)

[https://support.atlassian.com/bitbucket-cloud/docs/use-docker-images-as-build-environments/#Custom-build-environments](https://support.atlassian.com/bitbucket-cloud/docs/use-docker-images-as-build-environments/#Custom-build-environments)


## Estudos para construir imagem ubuntu e instalar dependências, nvm, node, pnpm, docker e docker compose

Comandos para builder imagens e rodar container:

`docker build -t sostenes198/ubuntu:latest -f Ubuntu_Base_Image_Dockerfile  .`

`docker build -t soso/node-app -f node-app-example/Dockerfile node-app-example/`

`docker run -d --rm -v /var/run/docker.sock:/var/run/docker.sock --name app-node-test soso/node-app`

Publicando no `docker.io` a imagem:

`docker push sostenes198/ubuntu:latest`
