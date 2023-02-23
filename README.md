# GIT
Os ficheiros do seu laboratório poderão existir em três sítios: 
* no PC
* no GitHub 
* no PythonAnyWhere

Vamos aprender como transferir os conteúdos de e para cada uma destes sítios.

Se não estiver familiarizado com o Git, veja os [videos e slides sobre git](https://moodle.ensinolusofona.pt/course/view.php?id=9482#section-3). Eis o link direto para os {videos sobre git](https://educast.fccn.pt/vod/channels/1pc3vu3zkk?locale=pt) se tiver alguma dúvida.

## Criar novo repositório local
<img src="https://user-images.githubusercontent.com/42048382/221045249-00bfaf04-7898-4829-bd67-947ae4f349f3.png" width="70px">

Consideremos que tem o seu projeto no PythonAnyWhere/PC mas ainda não tem nem repositório local nem remoto no GitHub. Abra uma consola e crie, dentro da pasta que quer sincronizar seus conteúdos, um repositorio git:

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
     
## Carregar repositório local &rarr; novo repositório remoto no GitHub
<img src="https://user-images.githubusercontent.com/42048382/221045425-cdfb2233-5338-429d-9fdb-e5c10cc2c172.png" width="100px">

2. Na página do GitHub, na sua conta, crie um repositório com nome <numeroAluno-pw-labs>

3. carregue os conteúdos do repositório local para o repositório remoto no GitHub:
   ```Bash
    $ git remote add origin https://github.com/<username>/<repo_name.git>
    $ git push -u origin main
   ```   

### Sincronizar repositório local &rarr; repositorio remoto no GitHub já existente
<img src="https://user-images.githubusercontent.com/42048382/221045425-cdfb2233-5338-429d-9fdb-e5c10cc2c172.png" width="100px">
    
Se fizer alterações no seu repositório no PythonAnywhere/PC, pode sincronizar com o repo do GitHub da segunte forma:
   ```Bash
   $ git add .
    $ git commit -m "primeiro commit"
    $ git push
   ```
        
## "Clonar" repositório GitHub &rarr; máquina sem repositório
<img src="https://user-images.githubusercontent.com/42048382/221045530-175d4ee3-0c9c-4513-ab9d-cd2900987236.png" width="100px">

Basta fazer um clone do que tem no GitHub para a pasta que especificar. Na máquina onde quer ter os conteúdos do repositório GitHub, faça:

```Bash
   $ git clone https://github.com/<username>/<repo_name.git>
   ```   
   
## Sincronizar repositorio GitHub &rarr; máquina com repositório 
<img src="https://user-images.githubusercontent.com/42048382/221045571-36ea2212-dc4b-491e-bd4c-565969d8324c.png" width="100px">
    
```Bash
   $ git pull
   ```
        
