# Configurações iniciais para enviar arquivos para o GitHub
- Criar uma chave SSH
- Criar um repositório 
- Clonar repositório
- Enviar arquivos/códigos para o github

## Configurando o Gitbub com SSH:

Por que SSH?

Além de ser mais simples, é mais segura, pois você pode conectar com o github sem fornecer seu nome de usuário e personal access token a cada visita. E você também pode usar uma chave SSH para assinar confirmações. 

Então, caso não possua essas chaves, é preciso gerar.


- Primeiro é necessário instalar o Git. Você pode instalar por este link: https://git-scm.com/downloads

Mas o que é esse tal de Git?

Git é uma ferramenta, um software, de versionamento de código, ela permite que os desenvolvedores colaborem entre si de forma organizada na construção de um projeto que envolva código.


Depois do git instalado, caso use windows, vá na pesquisa e pesquise por git bash:

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/git%20bash.png)

Entre no git bash e digite:

- `ssh-keygen` e pressione a tecla Enter, vai aparecer essa mensagem:

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/keygen.png)

 Só ir digitando enter, que sua chave será criada.

Uma tela semelhante a essa aparecerá:

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/ssh%20criado.png)

Sendo assim sua chave ssh estará criada, agora precisamos pegá-la, digite os seguintes comandos:

1 - Entre na pasta ssh: `cd ~/.ssh`

2 - Com `ls` podemos ver os arquivos que estão na pasta, precisamos achar um arquivo que chama: `id_rsa.pub`,  é nele que a chave se encontra.

3 - Com `vim id_rsa.pub` vai abrir o editor com a chave SSH, aí é só copiarmos, para enfim colocar no github. Caso não tenha o VIM, será necessário instalar, você pode usar este site:  https://www.vim.org/download.php

OBS: Se estiver no Ubuntu/Linux, pode tentar ao invés do `vim`, mas o `cat`, pois ele já vem instalado e funciona da mesma forma.

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/ls%20cd%20vim.png)

Uma observação importante é que se caso estiver usando Windows, na hora de copiar a chave, use o botão direito para copiar, ao invés do CTRL + C, pois o windows, costuma colar caractere invisível e isso pode dar problema na autenticação.

Bom, depois de todos esses passos feitos, agora é só entrar nesse link: 

https://github.com/settings/keys

- Clicar no botão verde “NEW SSH KEY”

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/ssh%20new%20new.png)

Agora é só dar um nome para a chave e pronto, a chave SSH foi configurada no github \o/.


# Criando um repositório:


### Vá no seu perfil e clique em "repositories"

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/repositories.png)

### Clique em "NEW"

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/new.png)

### Agora é só criar o repositório: 


![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/create%20repository.png)


- #### Um nome para o repositório deve ser criado obrigatoriamente.
- #### Escolha se quer um repositório público ou privado.
- #### A escolha do README é facultativa, mas é sempre bom criar, pois será o README que pode conter do que se trata aquele repositório, se precisar colocar os comandos para a pessoa rodar o projeto é nele que colocamos, além de todas as informações relevantes do projeto.
- #### O .gitignore também é facultativo, mas é sempre bom ter pois é  arquivo de texto que diz ao Git quais arquivos ou pastas ele deve ignorar em um projeto, como por exemplo um ambiente virtual que contenha uma senha. Um arquivo  .gitignore local geralmente é colocado no diretório raiz de um projeto. 


Repositório criado, agora é preciso colocar este repositório no seu computador, para que assim possamos colocar nosso trabalho e enviar ao github.
Esse processo de colocar no nosso computador é o que chamamos de clone. Então vamos clonar esse repositório.

#### Vá no repositório criado e clique no botão verde “CODE”

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/clone%20code.png)

Confira se está selecionado SSH e copie o nome do repositório clicando no ![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/copia.png)  

Volte no terminal, encontre um lugar para criar essa pasta e digite: 

- `git clone “URL copiada”`   e enter

Aparecerá a seguinte mensagem

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/clonado.png)

Se você for na pasta e digitar pelo terminal `ls`, poderá ver todos os arquivos, se preferir pode ir pelo caminho convencional do windows.

Agora é só colocar todos os arquivos, códigos nessa pasta e enviar para o github. 

Para isso podemos digitar: 

`git add .`   → Esse ponto no final é para indicar que todos os arquivos que estão na pasta vão ser enviados para o github, se quiser enviar um arquivo específico, coloque o nome dele ao invés do ponto. 

`git commit -m “mensagem”` → Na mensagem do commit é pra dizer o que significa a alteração, a adição, ou a nova funcionalidade do código, normalmente é uma mensagem simples, não é para descrever o código, a descrição do código fica para o README.

Se for sua primeira vez fazendo isso, o commit não será feito, é preciso falar para o github quem é você, então ele vai pedir o email (e-mail que foi usado para criar o github) e também o seu nome.

![alt text](https://github.com/liviaspereira/config_github_ssh/blob/main/Imagens/commit%20config.png)

Então é só digitar o que ele pede:

`git config –global user.email “seu@email”` enter

`git config –global user.name “seu nome”` enter

Lembrando que essas configurações só serão feitas uma única vez.

Agora finalmente podemos enviar tudo o que queremos para o github, para isso digite:

`git push`

Agora é só voltar no github atualizar o repositório e lá veremos nossos arquivos \o/











