# Introdução

De uma forma bem simples, o docker é uma plataforma aberta, criada com a ideia de permitir que sua aplicação rode em uma "sandbox" (Chamada de contêiner). Existem algumas vantagens em se colocar a aplicação em um contêiner, tais como:
- Facilidade no gerenciamento;
- Agilidade para compartilhar o ambiente e aplicação com o restante da equipe;
- Diminuição do tempo de configuração da máquina, visto a infraestrutura para executar a aplicação estar dentro desse container;
- Minimização da frase "Na minha máquina funciona";

Quanto ao último item poderíamos até dizer que removeríamos a frase, mas existe um ponto importante a ser dito: O docker foi criado inicialmente para rodar no linux, assim sendo poderão existir alguns raros problemas ao executar o mesmo no Windows ou MacOS, visto que nesses SOs o docker precisará ser virtualizado, ou seja, existirá uma "máquina virtual" linux instalada onde o docker-machine será executado. Mas caso não seja necessário algo muito crítico, não ocorrerá nenhum problema na execução do docker nesses SOs.