# git

# 1. Repo GitHub 
Os ficheiros do seu laboratório poderão existir em três sítios: 
* no PythonAnyWhere, 
* no GitHub 
* no PC. 

Vamos aprender como transferir os conteúdos para cada uma destes sítios.

Nota: Se não estiver familiarizado com o Git, veja os [videos e slides sobre git](https://moodle.ensinolusofona.pt/course/view.php?id=9482#section-3). Eis o link direto para os {videos sobre git](https://educast.fccn.pt/vod/channels/1pc3vu3zkk?locale=pt) se tiver alguma dúvida.

### Criar novo repositório local e sincronizá-lo com um novo repositório remoto no GitHub

Consideremos que tem o seu projeto no PythonAnyWhere/PC mas ainda não tem nem repositório local nem remoto no GitHub. Passos para colocar os ficheiros no GitHub: 

1. Na sua conta de PythonAnyWhere/PC, abra uma consola (bash console) e crie, dentro da pasta `web`, um repositorio git e sincronize-o com o GitHub, da seguinte forma:

    1. defina, na máquina em que está, a sua identidade para o git:
   ```Bash
    $ git config --global user.name "username_usado_no_git"
    $ git config --global user.email "iniciais@meuemail.pt"
   ```
    
    2. dentro da pasta `web` crie um repositório git com os conteúdos da pasta:
   ```Bash
    $ git init
    $ git add .
    $ git commit -m "primeiro commit"
    $ git branch -M main
   ```
        
2. Na página do GitHub, na sua conta, crie um repositório com nome <numeroAluno-pw-labs>

3. carregue os conteúdos do repositório local para o repositório remoto no GitHub:
   ```Bash
    $ git remote add origin https://github.com/<username>/<repo_name.git>
    $ git push -u origin masater
   ```   

### Sincronizar repositório local --> repositorio remoto no GitHub
Se fizer alterações no seu repositório no PythonAnywhere/PC, pode sincronizar com o repo do GitHub da segunte forma:
   ```Bash
   $ git add .
    $ git commit -m "primeiro commit"
    $ git push
   ```
        
### Descarregar repositório GitHub --> máquina sem repositório
Basta fazer um clone do que tem no GitHub para a pasta que especificar. PAra tal, na máquina onde quer ter os conteúdos do repositório GitHub, faça:

```Bash
   $ git clone https://github.com/<username>/<repo_name.git>
   ```     
               
### Sincronizar repositorio local --> repositório no GitHub 

```Bash
   $ git pull
   ```
        
