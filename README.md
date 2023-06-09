# Anotações: comandos básicos do Git




## Working Area

- Transformar a pasta local num repositório
``` bash
$ git init
```

- Remover o(s) arquivo(s) do repositório
``` bash
$ git rm nomeArquivo.ext
```

- Mostrar as alterações feitas no(s) arquivo(s) que estão na Working Area
``` bash
$ git diff
```

## Staging Area

- Adicionar o(s) arquivo(s) na Staging Area
``` bash
$ git add nomeArquivo.ext
```

- Retirar o arquivo da Staging Area
``` bash
$ git reset HEAD nomeArquivo.ext
```

- Fazer com que o(s) arquivo(s) volte(m) para o padrão que estava(m) na Staging Area.
``` bash
$ git checkout -- nomeArquivo.ext
```

- Mostrar as alterações feitas no(s) arquivo(s) que está(ão) na Staging Area
``` bash
$ git diff --staged 
```

## Commit

- Commit dos arquivos que estão na Staging Area para o respositório
``` bash
$ git commit -m "mensagem" 
```

- Editar o último commit
``` bash
$ git commit --amend -m "mensagem (edição")
```

- Exibir todos os commits realizados
``` bash
$ git log
```

- Exibir todos os commits realizados + os diffs
``` bash
$ git log -p
```

- Exibir uma quantidade específica de commits + os seus diffs
``` bash
$ git log -p -quantidade (ex: $ git log -p -2)
```

- Exibir os commits com seus comentários, sem maiores detalhes
``` bash
$ git log --pretty=oneline
```

- Abrir o visualizador de histórico de commits (GUI)
``` bash
$ gitk
```

## Branch

- Cria uma branch
``` bash
$ git branch nomeBranch
```

- Acessar a branch
``` bash
$ git checkout nomeBranch
```

- Apagar a branch
``` bash
$ git branch -d nomeBranch
```

- Adicionar as modificações da branch fonte na branch corrente (master ou outras)
``` bash
$ git merge branchFonteArquivos
```

- Listar as branchs existentes
``` bash
$ git branch
```

- Conflitos entre branchs 
Verificar a(s) linha(s) onde ocorre o conflito e resolvê-lo manualmente.

## Conexão com o GitHub

- Fazer link remoto
``` bash
$ git remote add origin enderecoRepositorioGit
```

- Gerar a keygen

	Deixar sem senha, caso contrário, será necessário informá-la a cada push/pull

	Entrar na pasta onde estão as chaves e abrir o .pub. É neste arquivo que encontra-se a chave.
	
	GitHub: acessar settings -> SSH and GPG Keys -> New SSH key -> colar a key no local apropriado

``` bash
$ ssh-keygen
```

- Clonar o repositório do GitHub (faz o download dos arquivos para uma pasta local)
	
	O link para clone está disponível em cada repositório no GitHub

``` bash
$ git clone enderecoRepositorioGit (nomeRepositorioLocal "opcional")
```
 	
- Push (envio) dos arquivos commitados para o GitHub

	Obs: verificar se estais no repositório correto antes de fazer o push

``` bash
$ git push origin master
```
	
- Pull (pega) dos arquivos commitados no GitHub

	Obs: verificar se estais no repositório correto antes de fazer o pull

``` bash
$ git pull origin master
```
	
## Contribuição em outros projetos no GitHub

- Fork
	
	Clone do repositório que você quer contribuir.

	1. No GitHub, acessar o repositório que deseja colaborar e clicar em FORK.

	2. No repositório "forkado", procurar o link para clonar.

	3. Git Bash da sua máquina:

	``` bash
	$ git clone enderecoRepositorioGit (nomeRepositorioLocal "opcional")
	```

	4. O repositório será clonado para o seu computador e já podem ser realizadas as contribuições.

	5. Realizar os ADD e os COMMITS necessários.

	6. Realizar o GIT PUSH ORIGIN MASTER para subir as alterações para o seu respositório no GitHub.



- Pull Request

	Envio das suas contribuições para serem analisadas pelo autor do projeto.

	1. No seu perfil do GitHub, no repositório "forkado", clicar em Pull Request e confirmar.

	2. No perfil do projeto destino da colaboração: clicar em Pull Request e, se aceito, realizar o MERGE PULL REQUEST.


## Outros

- Limpar a tela

``` bash
$ clear
```
