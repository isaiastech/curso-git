# Comandos fundamentais

# Criar arquivo
echo "# curso-git-1" >> README.md

#inicializar repositório
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/isaiastech/curso-git-1.git
git push -u origin main

git remote add origin https://github.com/isaiastech/curso-git-1.git
git branch -M main
git push -u origin main

# Adicionando Arquivos
git add .\css\style.css

# Adicionando Arquivos
 git add .  "usa o ponto no final".

## Salvando alterações

git commit a.txt -m "estou enviando o arquivo de texto" ->salva um arquivo especifico
git commit -a -m "Enviando a funcionalidade X" ->salva todas as alterações

## Enviando código para o repositório
git push

## Recebendo alterações
git pull

##Clonando repositórios
git clone https://github.com/isaiastech/curso-git-1.git .  "Passa a url com um ponto no final"

# Removendo arquivos

git rm teste.txt
git commit -a -m "deletando arquivo desnecessário"
git push

# Vendo log dos commits
git log

# Renomeando Arquivos
git mv css/banner.css css/banner_inicial.css → renomeando arquivo

git mv css/banner.css css/banner_inicial.css → movendo para pasta

# Desfazer alterações
git checkout css/style.css

# Ignorando arquivos do projeto
criar um arquivo chamado .gitignore
dentro dele coloca os arquivo que não serão colocados no repositório do github

ex:       node_modules/*  → ignora todos os arquivos da pasta
	exemplo.txt    → ignora um arquivo específico.

# Com o comando git reset podemos resetar as mudanças feitas
● Geralmente é utilizado com a flag --hard
● Todas as alterações commitadas e também as pendentes serão
 excluídas;

<!-- Fim da 1ª Secão -->


# Branches

# Criando e utilizando branches

git branch -->mostra o numero de branch no projeto
git branch <nome do branch> cria um novo branch

# Mudando de branch
● Podemos deletar um branch com a flag -d ou --delete
● Não é comum deletar um branch, normalmente guardamos o histórico
do trabalho;
● Geralmente se usa o delete quando o branch foi criado errado;

git branch --delete <nome da branch>
git branch --d <nome da branch>

# Mudando de branch

● Podemos mudar para outro branch utilizando o comando git checkout
-b <nome>
● Este comando também é utilizado para dispensar mudanças de um
arquivo;
● Alterando o branch podemos levar alterações que não foram
commitadas junto, tome cuidado!

# Unindo branches

● O código de dois branches distintos pode ser unido pelo comando git
merge <nome do branch>
● Outro comando para a lista dos mais utilizados;
● Normalmente é por meio dele que recebemos as atualizações de outros
devs;
● obs= commit o arquivo no branch atual volta para master ai faz o merge

git merge <nome do branch>

# Stash

● Podemos salvar as modificações atuais para prosseguir com uma
● outra abordagem de solução e não perder o código
● O comando para esta ação é o git stash
● Após o comando o branch será resetado para a sua versão de acordo
● com o repo;

git stash

# recuperando Stash

● Podemos verificar as stashs criadas pelo comando git stash list
● E também podemos recuperar a stash com o comando git stash
● <nome>
● Desta maneira podemos continuar de onde paramos com os arquivos
adicionados a stash

git stash list

# Removendo a stash
● Para limpar totalmente as stash de um branch podemos utilizar o
  comando git stash clear
● Caso seja necessário deletar uma stash específica podemos utilizar git
  stash drop <nome>
 
 git stash clear <apaga tudo>
 git stash drop <nome da stash> apaga uma em especifico

 # Utilizando tags

 ● Podemos criar tags nos branches por meio do comando git tag -a
   <nome> -m “<msg>”
● A tag é diferente do stash, serve como um checkpoint de um branch;
● É utilizada para demarcar estágios do desenvolvimento de algum
recurso;
● sempre fazer o commit antes

git tag <ver o nome da tag>
git tag <nome da versão v1.0> -a -m "primeira versão"

# Verificando e alterando tags
● Podemos verificar uma tag com o comando git show <nome>
● Podemos trocar de tags com o comando git checkout <nome>
● Desta maneira podemos retroceder ou avançar em checkpoints de um
branch;

# Enviando e compartilhando tags
● As tags podem ser enviadas para o repositório de código, sendo
compartilhada entre os devs;
● O comando é git push origin <nome da tag>
● Ou se você quiser enviar mais tags git push origin --tags

# Conclusão da seção

# Compartilhamento e atualização
# Encontrando branches
● Branches novos são criados a todo tempo e o seu git pode não estar
mapeando eles;
● Com o comando git fetch você é atualizado de todos os branchs e tags
que ainda não estão reconhecidos por você;
● Este comando é útil para utilizar o branch de algum outro dev do time,
por exemplo;

git fetch <passando a flag -a>
