# Sobre o git :desktop_computer:

* Sistema de versionamento de código distribuído

​	Criador: Linus Torvalds 

​	Comandos Básicos 

​	- Mudar Pastas 

​	\- Listas as pastas 

​	- Criar pastas/arquivos

​	\- Deletar pastas/arquivos 



*Cmd*

​	**Windows**              

* cd (cd ..) (navegar)   

* dir (listar pastas arquivos)      

* cls (limpar tela)

* mkdir (criar pasta)    

* echo ... (imprime no terminar um texto)

* echo texto ">" (redirecionador de fluxo) 

* del *nome (deleta arquivos apenas)

* rmdir /s /q  (remover diretórios (pastas)

* pwd (lista o caminho) 

* mv "nome do arquivo".md ./"nome da pasta" (comando mover)     

* (letra) + tab (completa o termo) 



**Unix (Linux/Apple)**

* cd (navegar)

* (listar pastas/arquivos)
*  clear (limpar tela)
*  mkdir (criar pasta)
*  rm -rf (remover diretórios)



#### Como o GIT funciona por baixo dos panos

**SHA1**

* Secure Hash Algorithm (Algoritmo de Hash Seguro), é um conjunto de funções hash criptográficas projetada pela NSA (Agência de Segurança Nacional dos EUA);

* A encriptação gera conjunto de caracteres indentificador de 40 dígitos;

$ openssl sha1



**Objetos fundamentais**

* BLOBS

Metadados do git

Blob             tamanho 42

\0

Ola mundo 



* echo 'conteudo' | git hash-object --stdin

* (gera um código sha) 

* echo -e 'blob 9\0conteudo' | openssl sha1

* (>) (gera o mesmo código sha) 

 (essa função espera receber um arquivo)

 

**TREES (árvores)**

* Armazenam os BLOBS

TREE               <tamanho>

\0

blob   sa4d8s    texto.txt

 

**COMMITS**

* É o objeto que vai juntar tudo

SHA1 487d4s...

Commit           <tamanho>

tree                    s4a5sq1

parente             a98acq1 (último commit)

autor                  perkles

mensagem       "inicia..."

timestamp



* Sistema distribuído

* Segurança



#### Chaves SSH e Tokens 

* Chave SSH: conexão segura e encriptada entre duas máquinas

**Git Bash:**

 ssh-keygen -t ed25519 -C [alexander.pastana@gmail.com](mailto:alexander.pastana@gmail.com)

* A chava pública vem sempre seguida de ".pub"

* Depois de acessar o local onde as chaves estão alocadas no Pc:

cat id_ed25519.pub

Será exibida a chave ssh pública.

SSH agent

eval $(ssh-agent -s)

Agent pid 647 (número do projeto)

* Passa a chave privada ao agent, não a pública. O agent ficará encarregado de usar a chave privada para descriptografar alguma criptografia que chegar com essa chave:

ssh-add (colocar caminho da chave, caso não esteja na pasta) id_ed25519

* Token de acesso pessoal 



#### COMANDOS COM O GIT

**Iniciar o Git**

Cria de fato um repositório git dentro da pasta/diretório em questão;

Tracked & Untracked

* Iniciar o versionamento

* Criar um commit

​	\- git init (iniciar repositório)

​	\- git add (mover arquivos e dar início ao versionamento, conhecer os primeiros comandos)

​	\- git commit (criar commit)

* Quando lidamos com terminal, sempre colocaremos o nome do programa na frente, por isso os comandos do GIT começam com "git".

$ git init (inicia o git dentro da pasta, para que o mesmo possa versionar e gerenciar o código).

* Flag -a mostra conteúdos ocultos;

$ ls -a

* Configurações Iniciais para criar arquivo pela primeira vez:

• Adicionar email

$ git config --global user.email "[email@mail.com](mailto:email@mail.com)" 

• Adicionar nome do autor

$ git config --global [user.name](http://user.name) "nome"

• Adicionando um arquivo 

\- Markdown: forma humanizada de escrever HTML sem precisar entender HTML de fato.

 **Ex:**

 \# Título tamanho 1

 \## Título tamanho 2

 \### Título tamanho 3 

 \#### Título tamanho 4

**Criando commit:**

Dentro da pasta com o arquivo Markdown:

* Adicionando ao repositório git criado

​	 \- Adicionando alterações gerais:

$ git add * 

$ git add .

​	 \- Adicionando arquivo à uma pasta já existente e commitada:

$ git add nome do arquivo.md pasta/



* Do stage para o commit:

$ git commit -m "commit inicial" (mensagem do commit)

* (em seguida, traz informações sobre o commit, trazendo os primeiros caracteres do sha1 dentro de "master", a string da mensagem, informações do arquivo, e o nome do aquivo .md)

  

* status do diretório

$ git status 



* Adicionando repositório remoto

$ git remote add origin 'aqui vem o link'

 * origin é o apelido geralmente dado (substitui url do github)

 

* Enviar commit para repositório remoto

$ git push origin master 

 

* Alterar nome da branch principal (master)

$ git branch -M "main" 



* Criando uma nova branch 

$ git checkout -b "nova branch"



* Alternando entre branchs

$ git checkout master (ou main)



* Juntar branch anternativa com a principal

​    *Primeiramente entrar na branch principal;

$ git merge novo-arquivo



* Baixa as alterações feitas no github

$ git pull 



#### Resolvendo Conflitos 

**Merge conflicts**

* Quando alguém clona seu repositório, arquivo etc, e o devolve com alterações, então você precisará pegar esse último commit alterado (o git juntará essas duas versões, a da sua máquina e a que foi alterada), resolver manualmente o que deverá ficar no commit e depois enviá-lo. (pull).

$ git pull origin master 



**Clonando repositórios**

*Baixa repositório já existente (clona) 

$ git clone https://...  .git

$ git remote -v 

(mostra origem do repositório, link)
