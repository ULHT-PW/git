# GIT

Considere o seu laboratório de PW uma pasta com ficheiros. Esta pode estar em três sítios: 
* no PC
* no GitHub 
* no PythonAnyWhere

**Objetivo**:  aprender como transferir os conteúdos da pasta entre estes sítios. 

Para o fazer, auxiliamo-nos do sistema de controlo de versões **Git**. Um repositório Git é uma pasta ./git, que reside dentro da sua pasta. Este repositório rastreia todas as alterações feitas nos ficheiros da pasta, construindo um histórico ao longo do tempo. O Git permite manter o seu repositório local em sincronismo com o seu reopsitório remoto, à medida que faz mudanças em qualquer um deles.

<img src="https://user-images.githubusercontent.com/42048382/221050972-e514079d-a572-43d9-bd39-0b5566321e34.png" width="100px">

**Vídeos e slides**: 
* [criação de repo git e upload no GitHub](https://educast.fccn.pt/vod/clips/1x4q1ux6mv/streaming.html?locale=pt)
* [clone do GitHub, edição local, upload no GitHub](https://educast.fccn.pt/vod/clips/170nrt6pya/streaming.html?locale=pt)
* [slides](https://github.com/ULHT-PW/git/blob/main/Git%20e%20GitHub_simples.pdf)


# Quero criar um repositório Git com o lab que fiz no meu PC
<img src="https://user-images.githubusercontent.com/42048382/221045249-00bfaf04-7898-4829-bd67-947ae4f349f3.png" width="70px">

Consideremos que tem o seu projeto numa pasta. Ainda não tem um repositório Git associado que permita rastrear mudanças nos seus ficheiros. Vamos então criar um repositório Git:

1. Se nunca o fez na maquina em que está, na consola (linha de comandos) **defina a sua identidade para o git**:
    ```Bash
    $ git config --global user.name "username_usado_no_git"
    $ git config --global user.email "iniciais@meuemail.pt"
    ```
    
Por exemplo:

    ```Bash
    $ git config --global user.name "luciostuder"
    $ git config --global user.email "lucio.studer@gmail.com"
    ```

2. dentro da pasta do seu projeto, **crie um repositório Git**:
    ```Bash
    $ git init
    ```

3. guarde o seu projeto no **repositório Git**:
    ```Bash
    $ git add .
    $ git commit -m "primeiro commit"
    $ git branch -M main
    ```


# Quero guardar o meu novo projeto no GitHub
<img src="https://user-images.githubusercontent.com/42048382/221045425-cdfb2233-5338-429d-9fdb-e5c10cc2c172.png" width="100px">

Se já fez os passos anteriores, pode sincronizar pela primeira vez o repositório local &rarr; repositório remoto GitHub:

1. na página do GitHub, crie um repositório remoto <repo_name>

2. **sincronize os conteúdos** no repositório remoto GitHub:
   ```Bash
    $ git remote add origin https://github.com/<username>/<repo_name.git>
    $ git push -u origin main
   ```   

# Quero guardar no GitHub as mudanças que fiz ao projeto no PC
<img src="https://user-images.githubusercontent.com/42048382/221045425-cdfb2233-5338-429d-9fdb-e5c10cc2c172.png" width="100px">
    
Se fizer alterações em ficheiros da sua pasta, pode: 
    1. indicar para "seguir o rastro" de todos ficheiros existentes e novos (git add .) 
    2. fazer uma "fotografia dos ficheiros rastreados" da pasta (git commit -m "adicionei estilos CSS"), com mensagem informativa do que foi alterado  
    3. sincronizar as mudanças com o repo GitHub (git push)
    
Eis a sequencia de comandos:
   ```Bash
    $ git add .
    $ git commit -m "adicionei estilos CSS"
    $ git push
   ```
        
# Esqueci-me do PC com o projeto em casa, mas está sincronizado no GitHub
<img src="https://user-images.githubusercontent.com/42048382/221045530-175d4ee3-0c9c-4513-ab9d-cd2900987236.png" width="100px">

Basta fazer um "clone" do repositorio remoto GitHub &rarr; seu PC:

```Bash
   $ git clone https://github.com/<username>/<repo_name.git>
   ```   
   
# Quero atualizar no PC de casa as alterações que fiz e carreguei no GitHub 
<img src="https://user-images.githubusercontent.com/42048382/221045571-36ea2212-dc4b-491e-bd4c-565969d8324c.png" width="100px">

Sincronize o repositorio GitHub &rarr; seu PC com repositório desatualizado:
```Bash
   $ git pull
   ```
        
