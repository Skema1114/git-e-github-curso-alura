# GitEGithubCursoAlura

## Neste projeto:

- Curso:

  - Git e Github: Controle e compartilhe seu código
  - https://cursos.alura.com.br/course/git-github-controle-de-versao

## Comandos utilizados

- git status (verificar o status do repositório)
- git add imdex.html / index add . (adicionar um ou vários arquivos para que o git começe a "escutá-lo" e que o mesmo fique pronto para receber uma mensagem de commit)
- git commit -m "Mensagem pequena e descritiva" ("encapsula" os arquivos que estão sendo "escutados"/estageados e rotula os mesmos com essa mensagem passada)
- git log (mostra diversas informações do histórico de commits efetuados no repositório)
- git config --local user.name "Nome" (altera o nome do usuário no repositório)
- git config user.name (visualiza o nome do usuario no repositório)
- git log --oneline (mostra o log só que de forma super resumida)
- git log -p (mostra o log só que de forma super completa)
- git log --pretty="format:%H" (indenta para que o log mostre apenas os hashs dos commits)
- git log --pretty="format:%h %s" (indenta o log de forma que o mesmo mostre apenas o hash resumido o as mensagens de commits)
- git log --pretty="format:%h %s %ae" (indenta o log de forma que o mesmo motre apenas o hash resumido, as mensagens de commits e o email do autor)

## Anotações

- `HEAD:` Estado atual do nosso código, ou seja, onde o Git os colocou;
- `Working tree:` Local onde os arquivos realmente estão sendo armazenados e editados;
- `index:` Local onde o Git armazena o que será commitado, ou seja, o local entre a working tree e o repositório Git em si;
- **OBS:** Para sair do `(END)` no windows (testado no `Poweshell`) basta pressionar a tecla `q`;
- **CONVENÇÃO/CONSENSO:** VOCÊ NUNCA DEVE COMMITAR UM CÓDIGO QUE NÃO FUNCION, O CÓDIGO TEM QUE ESTAR EM ESTADO FUNCIONAL PARA SER COMMITADO;
- **DICA DO CURSO:** Devemos gerar um commit sempre que a nossa base de código está em um estado do qual gostaríamos de nos lembrar. Nunca devemos ter commits de códigos que não funcionam, mas também não é interessante deixar para commitar apenas no final de uma feature. Essa pode ser uma discussão sem fim e cada empresa ou equipe pode seguir uma estratégia diferente. Estude sobre o assunto, entenda o que faz mais sentido para você e sua equipe e seja feliz;

## Entendendo

- Status commits
  <img src="assets\img\status-commits.png" width="auto">

## Links

- Comandos e parâmetros disponíveis do git log
  - https://devhints.io/git-log
- Formatando os logs com o prettie
  - https://devhints.io/git-log-format
