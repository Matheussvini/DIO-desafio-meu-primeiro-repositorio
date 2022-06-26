#### Aprendizados Git / GitHub

- lista de diretórios (pastas) de onde vc ta
  	dir - Windows / ls - Linux
  	dir -a - mostra arquivos ocultos

- entrar na pasta / voltar 1 pasta

  ​	cd / cd ..

- limpar tela
  	cls - windows / clear (ctrl + l) - linux

- função autocompletar 
  	tab - windows / linux

- criar pasta 
  	mkdir - windows / linux

- enviar uma informação para saída 
  	echo - windows / linux

- deletar arquivos de uma pasta
  	del - windows

- deletar repositório (pasta + arquivos)
  	rmdir "nome da pasta" /S /Q

- mover arquivos para uma pasta

  ​	mv nome_do_arquivo.extensão ./nome_da_pasta/



#### Formatação Typora

- link clicável

  ​	\[nome a ser exibido](URL do link)



#### Trabalhando com o GitBash

1. Inicializar um repositório git dentro de uma pasta (.git)

   ​	git init

2. Configuração inicial:

   1. Atrelar autor ao commit
      1. git config --global user.email \"matheussvini@outlook.com"
      2. git config --global user.name Matheussvini

3. Commitar o arquivo

   ​	git add * ou git add nome_do_arquivo nome_da_pasta/ ou git add .

   ​	git commit -m "escreva aqui uma mensagem sobre o commit"

4. Verificar como está o repositório de trabalho

   ​	git status

5. Criar arquivo como página de rosto do repositório

   ​	echo > README.md

6. Listar email e usuário do autor do repositório

   ​	git config --list

7. Enviar repositório local para o repositório remoto

   1. criar repositório no GitHub e copiar URL do repositório

   2. Adicionar origem para onde estão sendo enviado os arquivos

      ​		git remote add origin URL_do_repositório

      ​		origin é o apelido do URL para fazer menção

   3. Exibe lista de repositórios remoto que se tem cadastrado

      ​		git remote -v

   4. Empurrar (enviar) código do repositório local para o repositório remoto

      ​		git push origin master

      ​		fazer autenticação



#### Conflitos no GitHub - Merge

- Acontece normalmente quando você tem um arquivo em um repositório no GitHub, que alguém já modificou e lançou a alteração no GitHub, aí você modifica a versão inicial e tenta enviar para o GitHub e dá conflito. O GH vai pedir que você puxe a tentativa de junção das 2 modificações e decida manualmente o que será modificado.

- Puxar versão de junção das 2 versões que estão dando conflito

  ​		git pull origin master

- Abre o arquivo baixado no Typera, copia e conteúdo e cola em um editor de textos para ver o texto sem formatação.

- Entendendo as marcações:

  ​	<<<<<<<<< HEAD

  ​	conteúdo que você modificou

  ​	=========

​			conteúdo que alguém modificou e lançou no GH

​			>>>>>>>> e1bvhbwwgw4w3faejfwuewifa

- Agora é só apagar os comentários e decidir no conflito que modificações permanecem ou não.

- Deixar na pasta a versão final após resolução do conflito e commitar.

  ​		git add *

  ​		git commit -m "resolve conflitos"

- Empurrar para o repositório remoto

​				git push origin master



#### Como baixar/clonar repositório remoto para trabalhar no seu repositório local

1. Copia URL de clone do repositório remoto
2. Abre o GitBash na pasta em que deseja salvar seu clone
3. git clone URL_do_repositório