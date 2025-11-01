#bandit #overthewire #linux #ctf

## **Level 0**

### **Comandos a serem utilizados**

[[secao01-Linux Cheat Sheet V1.0.pdf]]
### **Enunciado e Resolução**
O primeiro nível tem como objetivo apenas acessar o SSH, utilizando o usuário e porta informados no site. O host vai solicitar a senha para o login com o usuário. A senha está sendo informada no enunciado também.

Para acessar o SSH estou utilizando o Kali Linux que está diretamente no terminal do meu Windows, por meio do WSL2.

![[level0-overthewire.png]]
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit0
Senha: bandit0

## **Level 1**

### **Enunciado e Resolução**
O nível apenas solicita que realizemos a leitura do arquivo "readme" no diretório home(assim que realizamos login já estamos nesse diretório). A partir dai basta dar um `ls` para listar os arquivos e pastas desse diretório(opcional) e utilizar um comando de leitura de arquivos, onde eu utilizei o `cat` para que eu conseguisse ler a senha 
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit1
Senha: ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
## **Level 2**

### **Enunciado e Resolução**
A senha para o próximo nível está em um arquivo chamado "-". Como o nome do arquivo é o mesmo caractere que o bash utiliza para indicar parâmetros no CLI, acaba acontecendo um erro ao realizar o comando `cat -`, pois o terminal vai estar aguardando a introdução de um parâmetro. Nesse caso torna-se obrigatório especificar que o "-" é um diretório, por meio do sinal "<"(menor) ou por meio do "./"(ponto e barra), então o comando fica assim:
`cat ./-`
`cat < -`
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit2
Senha: 263JGJPfgU6LtdEvgfWU1XP5yac29mFx
## **Level 3**

### **Enunciado e Resolução**
A senha para o próximo nível está armazenada em um arquivo chamado `--spaces in this filename--`localizado no diretório inicial. Como o arquivo possui espaços no seu nome, se a gente não especificar que esses espaços fazem parte do nome do arquivo, isso vai gerar um problema no comando, pois o CLI vai entender que o nome do arquivo acaba em `--spaces`, e portanto torna-se necessário a utilização da "\\"(contra barra) para especificar que o espaço é um caractere do nome do arquivo:
`cat ./--spaces\ in\ this\ filename--`
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit3
Senha: MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
## **Level 4**

### **Enunciado e Resolução**
A senha para o próximo nível está armazenada em um arquivo oculto no diretório **inhere**. Para achar a senha é necessário descobrir o nome do arquivo dentro do diretório, para isso listamos tudo que o diretório possui, inclusive arquivos escondidos por meio do `ls -a`. 

![[level4-overthewire.png]]

Agora basta acessar o arquivo utilizando o `cat ./...Hiding-From-You`. E para evitar sempre de escrever o nome dos arquivos e diretórios, é possível utilizar a tecla "tab", que vai realizar um autocomplete nos nomes dos diretórios e arquivos.
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit4
Senha: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
## **Level 5**

### **Enunciado e Resolução**
A senha para o próximo nível está armazenada no único arquivo legível por humanos no diretório **inhere**. Quando falamos de um arquivo legível por humanos, estamos falando sobre um arquivo escrito no formato ASCII, portanto é necessário entender o tipo de arquivo por meio do comando `file`. Acessando o diretório(`cd ./inhere`) e utilizando o comando "file" em todos os arquivos ao mesmo tempo, obtemos aquele que possui o formato ASCII:
`file ./*`
Em diversos sistemas o "\*"(asterisco) é um "coringa" ou "wildcard", que significa qualquer valor. Então quando rodamos um comando e substituímos no nome de um arquivo ou parte do nome por um "\*", significa que comando vai se aplicar a todos que derem match(nesse caso foi qualquer coisa dentro do diretório)
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit5
Senha: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
## **Level 6**

### **Enunciado e Resolução**
A senha para o próximo nível está armazenada em um arquivo em algum lugar dentro do diretório **inhere** e possui todas as seguintes propriedades: ele é legível por humanos, possui 1033 bytes de tamanho e não é executável.
Para encontrarmos o arquivo possuindo a senha, precisamos acessar o "inhere", e procurar um arquivo dentro de cada um dos diretórios presentes. Para procurar por arquivos, vou utilizar o comando `find` e vou especificar primeiro, que eu quero arquivos por meio do parâmetro `-type`:
`find . -type f` 
![[level5.1-overthewire.png]]
Nesse comando, o "." significa que eu quero procurar nesse diretório em específico(inhere), mas eu posso especificar o diretório utilizando o path, ou posso procurar na "home" do usuário por meio do "~".
### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit6
Senha: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
## **Level 7**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit7
Senha: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
## **Level 8**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit8
Senha: 
## **Level 9**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit9
Senha: 
## **Level 10**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit10
Senha: 
## **Level 11**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit11
Senha: 
## **Level 12**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit12
Senha: 
## **Level 13**

### **Enunciado e Resolução**

### **Credenciais**
Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit13
Senha: 
## **Level 14**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit14
Senha: 

## **Level 15**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit15
Senha: 

## **Level 16**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit16
Senha: 

## **Level 17**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit17
Senha: 

## **Level 18**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit18
Senha: 

## **Level 19**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit19
Senha: 

## **Level 20**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit20 
Senha: 

## **Level 21**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit21 
Senha: 

## **Level 22**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit22 
Senha: 

## **Level 23**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit23 
Senha: 

## **Level 24**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit24 
Senha: 

## **Level 25**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit25 
Senha: 

## **Level 26**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit26 
Senha: 

## **Level 27**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit27
Senha: 

## **Level 28**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit28
Senha: 

## **Level 29**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit29 
Senha: 

## **Level 30**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit30 
Senha: 

## **Level 31**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit31
Senha: 

## **Level 32**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit32 
Senha: 

## **Level 33**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit33
Senha: 

## **Level 34**

### **Enunciado e Resolução**

### **Credenciais**

Hostname: bandit.labs.overthewire.org -p 2220
Usuário: bandit34
Senha: