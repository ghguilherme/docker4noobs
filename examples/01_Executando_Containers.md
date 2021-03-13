# Executando o Ubuntu

```
docker run -i -t --rm ubuntu:latest bash
```

Explicando o Comando:

- docker run

  Roda um comando em um novo container.

- -i

  Modo Iterativo.

- -t

  Modo TTY (Permite digitar no terminal).

- --rm

  Remove o container automaticamente do histórico.

- ubuntu:latest

  Imagem a ser executada para criar o container.

- bash

  Comando a ser executado dentro do container. Neste caso irá ser executado o bash do ubuntu.