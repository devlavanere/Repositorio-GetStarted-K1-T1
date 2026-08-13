#  Guia de Sobrevivência Git: Comandos Úteis e Salvadores de Vidas

Este repositório contém uma lista de comandos do Git, indo desde o fluxo básico de versionamento até truques avançados que salvam o dia a dia de qualquer desenvolvedor.

##  O Feijão com Arroz (Essenciais)

Estes são os comandos que você vai digitar praticamente todos os dias:

* `git init`: Inicializa um novo repositório Git em uma pasta local.
* `git status`: Mostra o estado atual do repositório (arquivos modificados, adicionados ou não rastreados).
* `git add .`: Adiciona todas as modificações atuais na "área de preparação" (staging area) para o próximo commit.
* `git commit -m "Sua mensagem aqui"`: Tira um "retrato" (snapshot) das alterações preparadas e salva no histórico.
* `git push`: Envia os seus commits locais para o repositório remoto (ex: GitHub).
* `git pull`: Puxa as atualizações do repositório remoto e mescla com a sua versão local.

##  Navegando entre Branches

Branches (ramificações) são essenciais para criar novas funcionalidades sem quebrar o código principal.

* `git branch`: Lista todas as branches locais. A branch atual ficará marcada com um asterisco (`*`).
* `git switch -c <nome-da-branch>`: Cria uma nova branch e já muda para ela imediatamente (forma mais moderna que o antigo `git checkout -b`).
* `git switch <nome-da-branch>`: Muda para uma branch já existente.
* `git merge <nome-da-branch>`: Junta as alterações de outra branch na branch que você está no momento.

##  Investigando o Passado

Comandos incríveis para entender o que aconteceu no código:

* `git log --oneline --graph`: O jeito mais legal de ver o histórico! Mostra a árvore de commits e branches de forma resumida e visual direto no terminal.
* `git diff`: Mostra exatamente quais linhas de código foram alteradas, adicionadas ou removidas antes de você fazer o commit.
* `git blame <nome-do-arquivo>`: Mostra quem modificou cada linha de um arquivo e em qual commit (excelente para descobrir quem introduziu um bug).

##  Salvadores da Pátria (Desfazendo coisas)

Todo mundo erra. Estes comandos ajudam a consertar:

* `git stash`: Você começou a codificar, o código está pela metade, mas você precisa mudar de branch urgentemente. O `stash` guarda suas alterações temporariamente em uma "gaveta" sem precisar fazer um commit incompleto.
* `git stash pop`: Traz de volta as alterações que você guardou na "gaveta" com o comando acima.
* `git restore <nome-do-arquivo>`: Desfaz as alterações locais de um arquivo que ainda não foi comitado, voltando ele para o estado original.
* `git reset --soft HEAD~1`: Desfaz o último commit, mas **mantém** as alterações nos arquivos (ótimo se você esqueceu de adicionar um arquivo no commit anterior ou errou a mensagem).
* `git cherry-pick <hash-do-commit>`: Puxa um commit específico de outra branch e aplica na sua branch atual.