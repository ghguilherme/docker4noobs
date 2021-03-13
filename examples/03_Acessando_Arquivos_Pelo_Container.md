# Publicando Portas com Nginx

```
docker run -i -t --rm -p 8087:80 -v $(pwd)/files/03_Acessando_Arquivos_Pelo_Container/html:/usr/share/nginx/html nginx:latest
```

Obs.: Caso vá rodar o comando da forma que está acima, é necessário que o seu terminal esteja aberto nesta pasta.

Após executar o comando, abra o navegador e acesse localhost:8087. Se aparecer o conteúdo do arquivo index.html localizado na pasta html desde diretório, quer dizer que deu certo.

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

- -v

  Faz o "vínculo" de uma pasta/arquivo do container com uma pasta/arquivo do host. Devemos passar o seguinte formato <arquivo_ou_diretorio_host>:<arquivo_ou_diretorio_container>.

  Neste caso, está vinculando a pasta html desde diretório com a pasta html localizada no diretório /usr/share/nginx do container.

  Obs.: O nome do arquivo ou pasta no host não precisa ser igual ao que está dentro do container

- nginx:latest

  Imagem a ser executada para criar o container (Nginx).