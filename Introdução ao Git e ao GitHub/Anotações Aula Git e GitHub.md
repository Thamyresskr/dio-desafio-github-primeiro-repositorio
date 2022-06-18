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



Ao colocar o código no GitHub é necessário fazer uma autenticação, essa autentiação hoje é feita pelachave SSH.

 