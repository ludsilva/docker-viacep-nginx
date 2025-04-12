# ViaCEP com Docker + Nginx
Este mini projeto executa um container Docker com Nginx, servindo uma página HTML com integração à API ViaCEP.

## Objetivo
Demonstrar como usar o Docker para servir uma aplicação HTML estática utilizando a imagem oficial do Nginx.

A página é baseada nos exemplos oficiais da [API ViaCEP](https://viacep.com.br/) e preenche os campos de endereço automaticamente com base no CEP informado.

## Estrutura

- `Dockerfile`: constrói a imagem baseada em Nginx
- `\html`: diretório com os arquivos .HTML e .JS (integração ViaCEP)
- `README.md`: documentação do projeto

## Como rodar o projeto

- Pré requisito: Docker instalado

1. Clone o repositório:

```bash
git clone https://github.com/ludsilva/docker-viacep-nginx.git
cd docker-viacep-nginx
```

2. Dentro do repositório, construa a imagem Docker:
```bash
docker build -t ludsilva/nginx-viacep:latest
```

3. Rode o container:
```bash
docker container run --name -nginx-viacep-container -p 8080:80 -d ludsilva/nginx-viacep:latest
```

4. Acesse no seu navegador

http://localhost:8080


## Tecnologias
- Docker
- Nginx
- HTML + JS
- API ViaCEP

## Creditos
Exemplo baseado no site oficial: [ViaCEP](https://viacep.com.br/)