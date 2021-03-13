<p align="center">
  <h1 align="center">Docker</h1>
  <p align="center"><img src="./assets/docker.png" alt="Docker" width="300"></p>
</p>

# Índice

  - [Introdução](#introdução)
    - [Conceitos](#conceitos)
  - [Exemplos](#exemplos)
    - [Executando Containers](examples/1_Executando_Containers/README.md)
    - [Publicando Portas](examples/2_Publicando_Portas/README.md)
    - [Acessando Arquivos pelo Container](examples/3_Acessando_Arquivos_Pelo_Container/README.md)
  - [Como Contribuir](#como-contribuir)
  - [Autores](#autores)

# Introdução

De uma forma bem simples, o docker é uma plataforma aberta, criada com a ideia de permitir que sua aplicação rode em uma "sandbox" (Chamada de contêiner). Existem algumas vantagens em se colocar a aplicação em um contêiner, tais como:
- Facilidade no gerenciamento;
- Agilidade para compartilhar o ambiente e aplicação com o restante da equipe;
- Diminuição do tempo de configuração da máquina, visto a infraestrutura para executar a aplicação estar dentro desse container;
- Minimização da frase "Na minha máquina funciona";

Quanto ao último item poderíamos até dizer que removeríamos a frase, mas existe um ponto importante a ser dito: O docker foi criado inicialmente para rodar no linux, assim sendo poderão existir alguns raros problemas ao executar o mesmo no Windows ou MacOS, visto que nesses SOs o docker precisará ser virtualizado, ou seja, existirá uma "máquina virtual" linux instalada onde o docker-machine será executado. Mas caso não seja necessário algo muito crítico, não ocorrerá nenhum problema na execução do docker nesses SOs.

## Conceitos

Alguns conceitos básicos que devemos saber são:

- Docker host

  Máquina onde o docker está instalado. Caso seja uma máquina Linux, o kernel da máquina será compartilhado entre os contêineres criados.

- Imagens

  "Receita de bolo" que será utilizada para criação do container. Uma imagem contém tudo o que é necessários para executar contêineres a partir de uma imagem.

- Contêiner ou Container

  Local onde estará a tua aplicação e que executará a mesma. Contém tudo o que é necessário para executar a aplicação. O container é criado a partir de uma imagem e cada container é uma aplicação isolada.

- Docker Registry

  Repositório de imagens docker a partir do qual podemos obter as imagens para criação de nossos contêineres. O Registry pode ser público ou privado.

- Docker Hub

  O [Docker Hub](https://hub.docker.com/) é o registro mais comum para hospedar e baixar diversas imagens.

- Dockerfile

  Arquivo de texto escrito com uma sintaxe simples, contendo um passo a passo para criação novas imagens.

- Docker Compose

   É uma ferramenta que nos auxiliará na criação de múltiplos contêineres Docker, com ela podemos configurar tudo o que é necessário para executar cada um desses contêineres (Por exemplo: portas, variáveis de ambiente, volumes, redes, etc).

<!-- CONTRIBUTING -->

# Como Contribuir

1. Realize um Fork do projeto
2. Crie um branch com a nova alteracao (`git checkout -b feature/description`)
3. Salve as alterações e realize o Commit (`git commit -m 'Adicionado um novo conteudo'`)
4. Realize o Push do branch (`git push origin feature/description`)
5. Abra um Pull Request

# Autores

- **Guilherme Henrique** - [@ghguilherme](https://github.com/ghguilherme)
