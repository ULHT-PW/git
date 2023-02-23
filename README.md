# GIT

Uma pasta com os ficheiros do seu laboratório pode existir em três sítios: 
* no PC
* no GitHub 
* no PythonAnyWhere

Vamos aprender como transferir os conteúdos da pasta entre estes sítios. 

Para o fazer, auxiliamo-nos do sistema de controlo de versões Git. Um repositório Git é uma pasta ./git, que reside dentro da sua pasta. Este repositório rastreia todas as alterações feitas nos ficheiros da pasta, construindo um histórico ao longo do tempo. O Git permite manter o seu repositório local em sincronismo com o seu reopsitório remoto, à medida que faz mudanças em qualquer um deles.

<img src="https://user-images.githubusercontent.com/42048382/221050972-e514079d-a572-43d9-bd39-0b5566321e34.png" width="100px">

Se não estiver familiarizado com o Git, veja os seguintes videos:
* [criação de repo git e upload no GitHub](https://educast.fccn.pt/vod/clips/1x4q1ux6mv/streaming.html?locale=pt)
* [clone do GitHub, edição local, upload no GitHub](https://educast.fccn.pt/vod/clips/170nrt6pya/streaming.html?locale=pt)
* [slides](https://github.com/ULHT-PW/git/blob/main/Git%20e%20GitHub_simples.pdf)


## Criar um repositório Git
<img src="https://user-images.githubusercontent.com/42048382/221045249-00bfaf04-7898-4829-bd67-947ae4f349f3.png" width="70px">

Consideremos que tem o seu projeto numa pasta. Esta pasta está no seu PC ou no PythonAnyWhere. Ainda não tem um repositório Git associado que permita rastrar mudanças nos seus ficheiros. Vamos então criar um repositório Git:

1. Na consola (linha de comandos) defina, na máquina em que está, a sua identidade para o git:
    ```Bash
    $ git config --global user.name "username_usado_no_git"
    $ git config --global user.email "iniciais@meuemail.pt"
    ```

2. dentro da pasta do seu projeto, crie um repositório Git da seguinte forma:
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
        
