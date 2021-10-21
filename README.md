# JavaScript

## Objectivo

Neste repositório compartilho algumas experiências desenvolvendo códigos JavaScript no ambiente linux com aplicações básicas, editor de texto com suporte a highlight de js (xed, gedit ou vim) e o navegador de internet firefox.



## Além disso

Aqui também ficarão guardados trabalhos, projetos ou exercícios realizados especificamente com JavaScript. Porém algumas dicas podem incluir outras linguagens como python3 e shell.



## O _Live Server_

Uma ferramenta importante no desenvolvimento web é o _Live Server_ que apresenta o resultado do código no navegador. Em algums aplicativos de ambiente de desenvolvimento (IDE), existe a extensão _Live Server_. Mas também existe a possibilidade de ter a mesma funcionalidade com um simples script shell executado apenas com recursos que vem com linux, como python3 e firefox.

```shell
python3 -m http.server & firefox --private-window localhost:8000
echo 'Enter pra sair'
read a
kill `pgrep python3`
```

Cole esses comandos em um arquivo com que tenha o nome fácil de reconhecer como por exemplo `executar` ou `liveserver` e dê permisão de execução pelo menu gráfico ou pelo terminal com `chmod u+x executar` então para executar seu _Live Server_ basta clicar 2x no arquivo e escolher "executar no terminal" ou executar `./executar` no terminal. 

Basicamente o que esse script faz é iniciar python3 e rodar um servidor local, deixar em _background_ então iniciar uma janela privativa firefox no endereço que o servidor local foi configurado.
A segunda linha serve para mostrar a mensagem no terminal com o comando para encerrar o servidor. A terceira linha aguarda qualquer tecla (do teclado) ser pressionada antes de executar a última linha que prontamente encerra o servidor python3.

****Por que iniciar uma janela de navegador privativa?**** R. Experimentando percebi que o firefox pode usar dados em _cache_ e não carregar todas as alterações que você acabou de fazer. Iniciando uma janela privativa resolve esse problema. Pode ser que o `CTRL+F5` também funcione mas ainda não testei.

*Execute o arquivo `executar` em uma pasta vazia para ver o resultado.* Uma página apresentando o conteúdo da pasta se abrirá já que não existe um arquivo `index.html`.
