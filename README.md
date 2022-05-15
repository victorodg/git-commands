# Vocabulário

## Git

Git é um sistema distribuído open source de controle de versão.

O sistema ajuda a acompanhar as atualizações feitas no código.

Não há códigos sobrescritos, uma vez que o Git salva múltiplas cópias no repositório.

## Repositório

É um diretório onde os arquivos ficam armazenados, podendo ficar em um depósito do GitHub ou em seu computador.

## Remote

É o repositório remoto, armazenado nos servidores do GitHub.

Tipicamente o *remote* padrão se chama *origin*.

## Branch

Um *branch* é uma versão do repositório que difere do projeto principal.

## Commit

Os *commits* são alterações salvas. Cada vez que um *branch* é alterado, deve ser feito um *commit* para manter a alteração.

## Pull request

É o ato de propor as mudanças que você acabou de fazer para outros desenvolvedores trabalhando no mesmo projeto.

---

# Comandos

## git config

```
git config --global -e
```

- abre o arquivo de configuração do Git

## Criar atalho

- Exemplos:

```
s = !git status
```

- cria um atalho que fica na sessão [alias] do arquivo .gitconfig
    
```
c = !git add --all && git commit -m
```

- cria um atalho que atualiza o que vai no commit e aplica o commit
    
```
l = !git log --pretty=format:’%C(blue)%h%C(red)%d %C(white)%s - %C(cyan)%cn,%C(green)%cr’
```

- cria um atalho que customiza o comando log
- %h: hash reduzido do commit
- %d: branch e tag
- %s: mensagem do commit
- %cn: nome da pessoa que realizou o commit
- %cr: data relativa do commit

## git init

```
git init
```

- cria um repositório no diretório atual

## git clone

```
git clone https://github.com/<usuario>/<repositorio>.git
```

- clona o branch *main* do repositório <repositorio>

```
git remote rm <remote>
```

- desvincula o clone do repositório remoto original

## git clone --branch

```
cd .../<diretorio_do_repositorio>/
    
git clone --branch <branch>
```
    
- clona o *branch* `<branch>`

## git remote

```
git remote add origin https://github.com/<usuario>/<repositorio>.git
```
    
- conecta seu repositório local a um repositório remoto

## git branch

```
git branch <branch>
```

- cria o *branch* `<branch>` no repositório local

```
git push -u <remote> <branch>
```

- sobe a *branch* `<branch>` para o repositório remoto

```
git branch
```
    
- lista as *branches* locais

```
git branch -a
```

- lista as *branches* remotas

```
git branch -r
```

- lista o *remote* e o *branch*

```
git branch -d <branch>
```

- deleta a *branch* `<branch>` do repositório local

```
git push origin --delete <branch>
```

- deleta a *branch* `<branch>` do repositório remoto

## git checkout

```
git checkout <branch>
```
    
- navega para a *branch* `<branch>`

```
git checkout -b <branch>
```
    
- cria a *branch* <branch>` e navega para ela

## git status

```
git status
```
    
- fornece informações sobre a *branch* em que estiver no momento

## git pull

```
git pull <remote>
```
    
- obtém atualizações do repositório remoto

```
git pull <remote> <branch>
```
    
- obtém atualizações de uma *branch* específica do repositório remoto

## git add

```
git add <arquivo>
```
 
- inclui as alterações de um arquivo em nosso próximo *commit*

```
git add --all ou git add .
```
    
- adiciona todos os arquivos modificados em nosso próximo *commit*

## git commit

```
git commit -m “mensagem explicando a mudança no código”
```

- define um ponto de verificação para o qual você pode voltar mais tarde se necessário

## git push

```
git push <remote> <branch>
```
    
- envia e salva as alterações no repositório remoto, na *branch* `<branch>`

```
git push -u <remote> <branch>
```

- faz upload de um *branch* novo
    
## git reset
    
```
git reset --hard <remote>/<branch>
```
    
- deixa o repositório local igual ao remoto, como se estivesse refazendo o `git clone`

## git revert

```
git log --oneline
```

- obtém o número do hash

```
git revert <número_do_hash>
```

- desfaz a alteração local ou remotamente

## git merge

```
git merge <branch_receptor> <branch_doador>
```
  
- mescla as atualizações no *branch* `<branch_doador>` ao branch `<branch_receptor>` (`<branch_doador>` não sofrerá alterações)

## configurar git com vscode

```
git config --global core.editor ‘code --wait’
git config --global -e
```

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
    
\- First item

\- Second item
    
\- Third item

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

See https://www.markdownguide.org/extended-syntax/#copying-and-pasting-emoji

## Subscript

H<sub>2</sub>O

H\<sub\>2\</sub\>O

## Superscript

X<sup>2</sup>

X\<sup\>2\</sup\>
