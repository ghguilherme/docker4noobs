# Publicando Portas com Nginx

```
docker run -i -t --rm -p 8087:80 nginx:latest
```

Após executar o comando, abra o navegador e acesse localhost:8087. Caso apareça a página "Welcome to nginx!", quer dizer que deu certo.

Explicando o Comando:

- docker run

  Roda um comando em um novo container.

- -i

  Modo Iterativo.

- -t

  Modo TTY (Permite digitar no terminal).

- --rm

  Remove o container automaticamente do histórico.

- -p

  Faz a publicação da porta do container para o host. Devemos passar o seguinte formato <porta_host>:<porta_container>.

  Neste caso estamos fazendo a publicação da porta 80 do container na porta 8087 do host. Ou seja, quando acessarmos localhost:8087, estaremos acessando o localhost:80 do nginx.

- nginx:latest

  Imagem a ser executada para criar o container (Nginx).