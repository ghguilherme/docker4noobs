# O que é o arquivo docker-compose.yml

Esse arquivo nada mais é que uma forma mais "entendível" do comando "docker run".

Para um exemplo, vamos levar em conta o seguinte comando (Já utilizado anteriormente):

```
docker run -it --rm -p 80:80 -d usuario-dockerhub/exemplo-docker
```

Nesse comando estamos subindo um container, mapeando a porta 80 do container com a porta 80 da nossa máquina host e utilizando a imagem usuario-dockerhub/exemplo-docker.

Para não termos que escrever tudo isso a todo o momento que formos subir esse container, poderíamos criar um arquivo docker-compose.yml da seguinte forma:

```yml
version '3'

services:
  nomeServico:
    image: usuario-dockerhub/exemplo-docker
    ports:
      - "80:80"
```

Dessa forma, falamos para o arquivo criar um serviço (Com o nome sendo "nomeServico" nesse exemplo). Esse serviço estará utilizando a imagem "usuario-dockerhub/exemplo-docker" e fazendo o mapeamento da porta 80.

Para que o container rode, teremos que utilizar o seguinte comando:

Obs.: O parâmetro "-d" é opcional, mas caso não seja passado, o terminal ficará inutilizável enquanto o container não for destruído.

```
docker-compose up -d
```

Os comandos para entrar no container, inpecionar o mesmo, ver os status e etc, serão os mesmos que utilizaríamos caso tivessemos utilizado o "docker run" para subir o container.

Algo interessante do arquivo docker-compose.yml é que ele te permite muitas outras coisas, como por exemplo:
    - Possibilidade de criar mais de um serviço (container) no mesmo arquivo;
    - Informar o tipo de rede para cada um desses serviços;
    - Passar comandos que serão executados pelo container logo após ele ser criado;
    - Informar variáveis de ambiente;

Mais a frente entraremos em um exemplo de um ambiente para desenvolvimento mais completo, com um webServer + banco de dados. Dessa forma vocês conseguirão ter uma ideia melhor de como criar um ambiente completo na sua máquina, instalando apenas o docker.