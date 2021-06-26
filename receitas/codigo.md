Para fazer o versionamento de código e enviá-lo para um servidor os seguintes passos e requisitos devem ser atendidos.



- Ter uma conta no servidor para armazenar os códigos. Pode ser o Github, Atlassian, GitLab etc.
- Criar o projeto no servidor onde será armazenado os arquivos.
- Instalar o git na máquina de desenvolvimento.
- Configurar o usuário com o comando

```
git config --global user.name "Seu nome"
```

- Não precisa ser o mesmo nome utilizado no servidor. Como por exemplo no Github.
- Configurar o email com o comando

```
git config --global user.email "Seu email"
```

- Não precisa ser o mesmo email utilizado no Github.
- A flag --global indica que esta configuração será utilizada para todos os projetos.
- No windows o git armazena estes dados num arquivo oculto chamado .gitconfig que fica salvo na pasta do usuário.
- Utilize o programa chamado **Git GUI** que é instalado ao instalar o Git. No menu help tem a opção Show SSH key.  Ao acessar essa tela, se não tiver uma chave, você poderá gerar uma.  Após ter a chave, use o botão Copy para copiar esta chave.
- Se  estiver utilizando o Github, acesse a conta, no menu superior direito  clique no avatar e depois em Configurações ou Settings, depende do  idioma.
- Do lado esquerdo acesse *SSH and GPG keys.* 
- Clique no botão New SSH Key. No campo key cole a chave que você copiou do GIt  GUI. No campo Title você pode dar o nome que você quiser. Salve.
- Agora o seu computador de desenvolvimento já consegue se comunicar com o servidor via url to tipo ssh.



Em uma pasta com um projeto configurado usando o comando *git init.* Você pode adicionar a url do projeto com o comando



```
git remote add <alias> <url>
```



irá criar o vínculo do seu projeto com o servidor. *Alias* é qualquer nome que você quiser dar. O costume é utilizar a palavra *origin* que remete a origem do projeto. Em url você coloca a url que você copiou do github.



Se você fez o clone do projeto com o comando *git clone* você não vai precisar executar esta etapa de adicionar a url com o comando *git remote add.*



Quando você for fazer um *push* ou um *pull* ou qualquer outro comando que interaja com o servidor, ele vai pedir uma  senha, essa senha, se você utilizou a conexão ssh, não é a senha do  github. É a senha que você digitou para gerar a chave SSH no Git GUI.  Essa é a senha pública para abrir a senha privada armazenada no  servidor, que permite que seu computador se autentique no servidor e  possa estabelecer a conexão.



Espero que não tenha causado mais confusão. Mas explicar passos técnicos sem imagens nem sempre é fácil.



EDIT:



Lembrando que as configurações iniciais para configurar nome, email e criação da  chave você só faz uma vez. A chave que você cria é a mesma para todos os projetos, ela é uma chave por servidor. Você pode usar a mesma chave em vários servidores diferentes. Ela é uma forma de estabelecer controle e segurança dos usuários.



------------

git remote remove origin

git remote add origin git@github.com:juniomsilva/livro-receitas.git

git push -u origin master

