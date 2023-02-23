# git

# 1. Repo GitHub 
Os ficheiros do seu laboratório poderão existir em três sítios: no PythonAnyWhere, no GitHub ou no PC. Vamos aprender como transferir para cada uma destas entidades.

Se não estiver familiarizado com o Git, veja os [videos e slides sobre git](https://moodle.ensinolusofona.pt/course/view.php?id=9482#section-3). Eis o link direto para os {videos sobre git](https://educast.fccn.pt/vod/channels/1pc3vu3zkk?locale=pt) se tiver alguma dúvida.

### Criar novo repositório local e sincronizá-lo com um novo repositório remoto no GitHub

Consideremos que tem o seu projeto no PythonAnyWhere/PC e ainda não tem repositório. Passos para colocar os ficheiros no GitHub: 

1. Na sua conta de PythonAnyWhere/PC, abra uma consola (bash console) e crie, dentro da pasta `web`, um repositorio git e sincronize-o com o GitHub, da segunte forma. Para tal siga os seguitnes passos:

    1. defina a sua identidade para o git:
   ```Bash
    $ git config --global user.name "username_usado_no_git"
    $ git config --global user.email "iniciais@meuemail.pt"
   ```
    
    2. dentro da sua pasta `web` crie um repositório git com os conteúdos da pasta `:
   ```Bash
    $ git init
    $ git add .
    $ git commit -m "primeiro commit"
    $ git branch -M main
   ```
        
2. Na sua conta de GitHub, crie um repositório com nome <numeroAluno-pw-labs>

3. carregue os conteúdos da sua pasta `web` do PythonAnywhere para o seu repositório remoto no GitHub:
   ```Bash
    $ git remote add origin https://github.com/<username>/<repo_name.git>
    $ git push -u origin masater
   ```   

### sincronizar repositório local --> repositorio remoto no GitHub
Se fizer alterações no seu repositório no PythonAnywhere/PC, pode sincronizar com o repo do GitHub da segunte forma:
   ```Bash
   $ git add .
    $ git commit -m "primeiro commit"
    $ git push
   ```
        
### descarregar conteúdo do repositorio remoto no GitHub para máquina local sem repositório (PC/PythonAnywhere)
Basta fazer um clone do que tem no GitHub para a pasta que especificar:

```Bash
   $ git clone https://github.com/<username>/<repo_name.git>
   ```     
               
### atualizar repositorio local com conteúdos do repositório no GitHub 

```Bash
   $ git pull
   ```
        
