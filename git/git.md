<h1 align="center">
    <img alt="git Image" title="git Image" src="./img/git.png" />
</h1>

### Oque é o Git:
Sistema de controle de versão distribuido e Open-source

### Tipos de Controle de Versão:
- **Sistemas Locais**

Disponivel somente na minha maquina,dificil de trabalhar com colaboradores,se o disco rigido for corrompido você perde tudo.

- **Sistemas Centralizados**

Ele fica em um unico servidor, Controle sobre as atividades dos colaboradores,se o servidor cair por uma hora durante essa hora ninguém pode trabalhar,se o disco rigido do banco de dados for corrompido você perde tudo

- **Sistemas Distribuidos**

Git, Mercurial, Bazaar

Duplicar( Clonar )localmente o repositório completo


## Configurações iniciais:
Estas configuração você Fara apenas uma vez por computador e o efeito se mantera mesmo apos atualizações, mas você podera mudalas a qualquer momento rodando esses comandos novamente.

 - **Listar Configurações**
 ```jsx
    git config --list
 ```
 - **Adicionar usuário github**
 ``` jsx 
    git config --global user.name "usuariodogithub"
 ```
 Se for preciso  colocar um nome diferente para um projeto específico é so colocar o comando sem a opção   - -global

- **Adicionar Email github**
```jsx
    git config --global user.email email_github_user@gmail.com
```
 o mesmo do github para não ocasionar problemas.

- **Setar editor**
```jsx
    git config --global core.editor "code -w"
```
code -w  é o visual studio code

## Iniciando um Repositório
 - **Acessa a pasta do projeto no terminal**
 ```jsx
    cd git-aula
 ```
 - **Inicializar um Repositorio dentro do nosso projeto**
 ```jsx
    git init
 ```
 - **Resposta Esperada**
 ```jsx
     Initialized empty Git repository
 ```

## Git Status
exibe as condições do diretório de trabalho e da área de staging.
```jsx
    git status
```

## Git add
Qual arquivo ou arquivos eu estou inserindo, preparando os arquivos para serem commitados

- **Adicionar Todos**
```jsx
    git add .
```

- **Adicionar um arquivo especifico**
```jsx
    git add index.js
```

- **Adicionar todos os arquivos com exteção .js**
```jsx
    git add *.js
```

## git commit
Colocando no repositorio local

- **Coommit**
```jsx
    git commit -m "initial commit"
```

## Git log
Com este comando é possivel saber todos os commites feitos no nosso projeto

 ```jsx
    git log
 ```
- **Comando git log resumido em uma linha**
 ```jsx
    git log --oneline
 ```

 ## Git Workflow
 Fluxo de trabalho do git

- **woking diretory /Working Tree**
Onde está todos os nossos arquivos modificados
##### Mandando para a stage area 
```jsx
    git add .
```
- **Stage Area/Index/stage tree**
Preparando os arquivos para serem commitados.
##### Commit
```jsx
    git commit -m "initial commit"
```
pronto os os nossos arquivos foram commitados e movidos para o local repository

##### obs: Caso eu queira remover um arquivo que está no stage area é so usar o comando 
```jsx 
    git rm --cache nome_do_arquivo.js
```
- **Local Repository**
Repósitório local, Sempre que for criado uma versão nova a versão mais nova fica no working diretory e todas as outras versões já criadas ficam  na linha do tempo  no local repository

##### PARA SABER MELHOR EM QUAL ETAPA ESTAMOS É SO USAR O COMANDO 

```jsx 
    git status
```

## Head - Apontador 
Mostra a branch atual 
##### Se ele aponta para Master/Main
Significa que estamos na nossa branch principal ou seja na nossa linha do tempo pricipal o ultimo commit 


## git remove
Remover um arquivo do working diretory 

```jsx
git rm nome_do_arquivo.js
```

## Trazendo de volta do staged
```jsx
git restore --staged nome_do_arquivo.js //tirando um arquivo especifico do staged area
```

```jsx
git restore --staged . //tirando todos os arquivos do staged area
```
