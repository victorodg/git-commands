# hello-world
description-test

# Commands

## git config

- git config --global -e
    - abre o arquivo de configuração do Git

## Criar atalho

- Exemplos:
    - s = !git status
        - cria um atalho que fica na sessão [alias] do arquivo .gitconfig
    - c = !git add --all && git commit -m
        - cria um atalho que atualiza o que vai no commit e aplica o commit
    - l = !git log --pretty=format:’%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn,%C(green)%cr’
        - cria um atalho que customiza o comando log
        - %h: hash reduzido do commit
        - %d: branch e tag
        - %s: mensagem do commit
        - %cn: nome da pessoa que realizou o commit
        - %cr: data relativa do commit

## git init

- git init
    - cria um repositório no diretório atual

## git clone

- git clone https://github.com/itau-corp/itau-sv9-db-dbsv910.git
    - clona o branch “main”
- git remote rm origin
    - desvincula o clone do original

## git clone --branch

- cd .../main_branch/
- git clone --branch develop
    - clona o branch “develop”

## git remote

- git remote add origin [https://github.com/itau-corp/itau-sv9-db-dbsv910.git](https://github.com/itau-corp/itau-sv9-db-dbsv910.git) (testar git@github.com/...)
    - cria o remote “origin”
- remote é uma bookmark para um repositório diferente para o qual eu posso dar um pull ou push, esse repositório nem precisa ser uma versão do repositório “main”

## git branch

- git branch develop
    - cria o branch “develop” no repositório local
- git push -u <remote> develop
    - sobe a nova branch para o repositório remoto
- git branch
    - lista as branches
- git branch -r
    - lista o remote e o branch
- git branch -d develop
    - deleta uma branch

## git checkout

- git checkout feature/grant_nii
    - navega para a branch “feature/grant_nii”
- git checkout -b feature/grant_nii
    - cria a branch feature/grant_nii

## git status

- git status
    - fornece informações sobre a branche em que estiver no momento

## git pull

- git pull <remote>
    - obtém atualizações do repositório remoto
- git pull <remote> develop
    - obtém atualizações de um branch específico (develop) do repositório remoto

## git add

- git add <arquivo>
    - inclui as alterações de um arquivo em nosso próximo commit
- git add -A, git add --all ou git add .
    - adiciona todos os arquivos modificados em nosso próximo commit

## git commit

- git commit -m “mensagem explicando a mudança no código”
    - define um ponto de verificação para o qual você pode voltar mais tarde se necessário

## git push

- git push <remote> develop
    - envia e salva as alterações no repositório remoto, no branch “develop”
- git push -u origin develop
    - faz upload de um branch “develop” novo
    
## git reset
    
- git reset --hard <remote>/<branch>
    
- deixa o repositório local igual ao remoto

## git revert

- git log -- oneline
    - obtém o número do hash
- git revert ‘número do hash’
    - desfaz a alteração local ou remotamente

## git merge

- git merge main develop
    - mescla as atualizações no branch “develop” ao branch “main” (”develop” não sofrerá alterações)

## configurar git com vscode

- git config --global core.editor ‘code --wait’
- git config --global -e

---

# Markdown Sheet

## Headings

# H1
\#
## H2
\##
### H3
\###

## Text

**bold text**

\*\*bold text\*\*

*italicized text*

\*italicized text\*

## Quote

> blockquote

\> blockquote

## Ordered list

1. First item
2. Second item
3. Third item

## Unordered list

- First item
- Second item
- Third item

## Code

`code`
  
\`code\`

## Horizontal rule

---

\---

## Link

[title](https://www.example.com)

\[title\]\(https://www.example.com\)

## Image

![alt text](image.jpg)

\!\[alt text\]\(image.jpg\)

## Table

| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text | 

\| Syntax \| Description \|

\| \----------- \| \----------- \|

\| Header \| Title \|

\| Paragraph \| Text \| 

## Fenced code block

```
{
"firstName": "John",
"lastName": "Smith",
"age": 25
}
``` 

\`\`\`

\{

"firstName": "John",

"lastName": "Smith",
  
"age": 25
  
\}

\`\`\` 

## Footnote

Here's a sentence with a footnote. [^1]

[^1]: This is the footnote. 

Here's a sentence with a footnote. \[\^1\]

\[\^1\]: This is the footnote.

## Heading ID

### My Great Heading {#custom-id}
  
\#\#\# My Great Heading \{\#custom-id\}  

## Definition List

term
: definition 

term
\: definition 

## Strikethrough

~~The world is flat.~~

\~\~The world is flat.\~\~

## Task list

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media 

\- \[x\] Write the press release
\- \[ \] Update the website
\- \[ \] Contact the media 

## Emoji

That is so funny! :joy:

That is so funny! \:joy\:

See https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji

## Highlighting

I need to highlight these ==very important words==. 
 
I need to highlight these \=\=very important words\=\=.

## Subscript

H~2~O

H\~2\~O

## Superscript

X^2^

X\^2\^
