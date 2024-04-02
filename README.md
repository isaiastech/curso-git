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
