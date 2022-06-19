# Anotações das aulas Git/GitHub :woman_student:



### Definições



#### Sha1

##### SHA1 - Secure Hash Algorithim (Algotimo de hash Seguro)

É um conjunto de hash criptografadas projetadas pelo NSA. Embaralha o arquivo de forma específica. Essa encripitação gera um conjunto de caracteres de 40 digitos que é único.

É uma forma curta de representar um árquivo.

Ao modificar algo nesse arquivo, ele irá gerar outro código de 40 digitos. Se o arquivo for retornado para o estado anterior, será gerado a primeira encriptação novamente.



### Objetos Internos do Git

#### Blobs / Tree / Commit

##### São responsáveis pelo versionamento do código

**Blobs**

- Usa a função echo



**Tree -  (árvores)**

- Armazenam os Blobs.
- Contém metadados.
- As árvores podem apontar para outras árvores ou para os blobs.



**Commit**

- Aponta para a árvore.
- Aponta para o utimo Commit. 
- Aponta para um autor.
- Aponta para uma mensagem.
- Os Commits possuem SHA1.



**Git- Sistema distribuído e seguro**

**Chaves SSH e Tokens**



**Chave SSH** -  forma de estabelecer uma conexão segura entre duas máquinas.

Existem duas chaves, a pública e a privada.



Para gerar uma chave SSH use o seguinte comando no Git Bash:

​	**ssh-keygen -t ed25519 -C + seu email do GitHub**



Ao colocar o código no GitHub é necessário fazer uma autenticação, essa autentiação hoje é feita pela chave SSH.

O seguinte comando mostra a chave pública, que devemos colocar no GitHub em SSH Keys.

​	**cat id_ed25519.pub**



**Token de Acesso Pessoal**

Como gerar um token no GitHub.

-> Ir em Developer Settings

-> Personal Access Token 

-> Note: Colocar um nome

-> Colocar data de expiração

-> em Select Scopes  -  Repo

->**Generate Token**

Ao gerar um Token, copie ele e salve em um arquivo seguro no computador.





### **Iniciando o Git e criando um Commit**

**Git Init** (Iniciar um repositório)

**Gitt add** (Mover o arquivo e dar inicio ao versionamento)

**Git Commit** (Faz o Commit)

 Todos os comandos do Git levam a palavra Git na frente e depois o comando especifico, pois estamos chamando pelo terminal.



### **Tracked**

Dentro de tracked, dentro dos arquivos que são rastreáveis pelo, ele pode se subdivir em três estágios diferentes.



**Unmodified** - Ainda não foi modificado

**Modified** - Sofreu alguma alteração

**Staged** - Onde os arquivos estão se preparando para fazer parte de um Commit



Temos outro agrupamento.

**Untracked** - arquivos que o Git ainda não conhece.





Ambiente de desenvolvimento - representa tudo o que está na nossa máquina.

Servidor - O Git é um sistema distribuído. Existe a versão que está no GitHub, e tem a versão que está na nossa máquina.

As alterações que são feitas na nossa máquina não representam imediantamente na versão que estã no remoty respository.

O repositório remoto está guardado em um servidor.

Os arquivos vão ficar transitando entre o "working directory" e a "staging area".

Ao fazer o commit os arquivos que estavam na área de staging são movidos de **staged** para **unmodified**, ou seja, é criado um **snap shot**.

**Git status** - nos ajuda a monitorar os status dos arquivos. 



**Comandos Git**

**git config --lista** - Mostra todas as configurações que forma feitas, inclusive o e-mail e nome usados.

Obs: o ideal é que o e-mail e o nome sejam os mesmos no Git e no GitHub.



**git config --global User.email "+ email usado no GitHub**"

**git config --global User.name ''nome usado no GitHub"**



## **Conflito de merge**

Quando você envia um código para o GitHub, a versão que está lá corresponde exatamente a versão que está na sua máquina. Supondo que outra pessoa faça um **Git Clone** do seu arquivo, o arquivo que está no GitHub é o mesmo que está na sua máquina e na máquina da outra pessoa.

Supondo que vocês abram o arquivo e façam a edição dele, já não estão mais em sincronia. O código do GitHub é um, o código da sua máquina é um, e o código da outra pessoa é outro.

Se o código que está na sua máquina e o código que está na máquina da outra pessoa, contém uma edição na mesma linha, é justamenre quando acontecem edições na mesma linha que ocorrem problemas.

Supondo que a outra pessoa empurrou (push) o arquivo para o GitHub, ou seja, o código que está no GitHub é o código que está na máquina de outra pessoa, então seu código está desatualizado. O código que está agora no GitHub é a versão mais atual.

Quando você submeter o seu código no GitHub ele vai te dizer que primeiro você puxar aquela versão mais atual que está lá, fazer as alterações, juntar o que você trabalhou com o que a outra pessoa trabalhou, e depois empurrar, pois ai nesse caso, seria a versão mais recente.

Nesse momento acontece o **conflito de merge**, quando o GitHub tenta junbtar duas alterações, e existem duas alterações na mesma linha, o GitHub não faz nenhuma alteração nisso, você precisa fazer manualmente.

