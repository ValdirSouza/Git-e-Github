# ***Introdução ao Git e ao GitHub***

**Sobre o Git**

O Git é um sistema de controle de versão distribuído amplamente utilizado para rastrear e <br>
gerenciar alterações em projetos de software. Ele possibilita a colaboração entre várias pessoas <br>
no desenvolvimento de código, gerenciando ramificações, mesmo quando as alterações ocorrem <br>
em locais diferentes ou na mesma linha, independentemente do momento em que são realizadas. <br>
No entanto, é importante observar que o Git não atua como um interpretador/compilador de código. <br>
Sua principal função é controlar e versionar o código, enquanto a detecção de erros e a compilação <br>
são geralmente tratadas por outras ferramentas e ambientes de desenvolvimento.

O Git foi desenvolvido principalmente para a linha de comando (CLI), e pode ser utilizado tanto por <br>
meio da linha de comando quanto por interfaces gráficas, proporcionando flexibilidade aos usuários. <br>
Existem diversas ferramentas gráficas, como o GitKraken, Sourcetree e GitHub Desktop, que facilitam a <br>
interação com o Git, tornando o processo mais acessível para aqueles que preferem ou necessitam de <br>
uma interface visual. Portanto, embora o Git possa ser utilizado via CLI, ele também tem opções de <br>
interface gráfica para tornar a interação mais amigável e acessível a diversos perfis de usuários.



Github não é uma ivenção do linux, ele nasceu do contestamento de vários desenvolvedores
github foi desenvolvido pela microsoft e é usado para armazenar o codigo

git e github são tecnologias diferentes

Linux criado 2005 pelo Linus Torvalds

1 - controle de versão
2 - armazenamento em nuvem
3 - trabalho em equipe
4 - melhorar seu código
5 - Reconhecimento


git ele é um software desenvolvido para interface cli, não tem interface grafica
para interagir com ele precisa de outros programas para interface grafica e hoje
já existe programas que fazem isso tornando mais simples

usando terminal
 - Mudar de pastas
 - Listar as pastas
 - Crias pastas/arquivos
 - Deletar pastas/arquivos

windows terminal derivado do shell
unix terminal derivado do bash

windows		Unix
 - cd		-cd			=> navega entre os diretorios, o uso da '/' faz voltar no inicio do disco C, '..' volta uma anterior
 - dir		-ls			=> lista os diretorios
 - mkdir	-mkdir			=> cria diretorio
 - del / rmdir	- rm -rf		=> del deleta arquivo, rmdir deleta diretl
 - cls		- control+L ou cls	=> limpa a visualização do terminal
 - echo		- echo			=> printa no terminal o que foi digitado após esse comando
 - echo > teste.txt			=> o terminal cria o arquivo com extenção que foi determinada no escrita e inclui o texto dentro do arquivo
o tecla 'TAB' é um atalho para completar a escrita do nome da tabela
que esteja no local acessado

-SHA1 (Secure Hash Algorithm)
  conjunto de funções hash criptográficas projetadas pela NSA(Agenc de Segur Nacional dos EUA)
  A encriptação gera um conjunto de characteres indentificador de 40 dígitos
-Objetos Fundamentais
  Blobs, Trees, commits => responsáveis por versionamento de código no git
 a função 'echo' pega um string e retornar o output da string
	  'hash-object' é uma função que recebe arquivo
	  '--stdin' usa em conjunto com a anterior para dizer para a anterior que era irá receber um texto em vez de um arquivo
 *Blob - os arquivos ficam gravados nesse objeto e dentro dele tem metadados, aqui fica a informações de tipo de objeto, o tamanho, uma \0 e o conteudo de fato do arquivo
 *Tree - Armazena os Blobs e aponta para diferentes blobs. Ela também contêm metadados. É responsável por armazenar toda a estrutura dos arquivos.
	Elas podem se apontar entre si. Possui incriptação também (sha1)
 *Commit - É o objeto que junta tudo, ele aponta para uma Tree, aponta para o último parente dele e o autor também.
	pode conter mensagem, tendo informações dos arquivos que compem eles
	possui também um timestamp de quando foi criando o arquivo

Sistema distribuído Seguro - 

## Iniciando o Git
 - git init		*inicializa o git (repositorio) dentro da pasta a qual estiver trabalhando o terminal
	Tracked (arquivos que o git tem ciência dele)
	  -Unmodified são arquivos que não foram modificados ainda
	  -Modified são os arquivos que já foram modificados
	  -Staged são os arquivos guardados para um proximo momento

	Untracked (arquivos que estão criados, mas o git não sabe da existência dele)
	  -Staged é o passo que move ele de Untracked para o passo de aguarda o que irá acontecer com o arquivo

	Quando adiciona arquivo ele vai para Staged
	Quando edita passa de Unmodified e vai para Modified
	"Stage" o arquivo vai para Staged
	Quando efetua o Commit(estende shot fica salvo aqui) e o arquivo para a ser Unmodified
	Caso remover o arquivo ele volta a ser Untracked, não existe no Git mais

   Os arquivos transitão entre as areas de 
	Working Directory	Untracked
		>> git add
	Staging Area		Unmodified - Modified
		>> git commit -m (moveu tora a área de stage para o repositorio
	Local Repository	Staged(repositorio local para o remoto)

 - git status		=> Retorna os status dos arquivos
 - Comando Mover
	mv nome_do_arquivo.ext ./novo_destino/
		- mv  => move o arquivo que vier logo apos
		- ./  => da pasta local onde se encontra para outro local
 - git add text.txt	=> move os arquivos e auterações para a área de Stage
 - git add *		=> movo todos os arquivos e auterações para a área de Stage
 - git commit -m	=> cria o snep shot no repositorio, cria a imagem das alterações que foram feitas
	caso queira comentar o que está sendo executado, coloque o texto entre "" após o 'm'

 - git config --list	=> lista as configurações setadas no Git
 - git config --global --unset user.name => comando para apagar atributo da configuração
						para apagar outro atributo basta trocar o nome no final

 - git remote add origin https://github...	=>comando usado para apontar um repositório local para um remoto

 - git push origin master	=> envia as informações do repositorio local para o repositorio remoto
				no feedback do codigo ele informa dados do objetos e o local que foi enviado

## Flask
 - ls -a => mostra arquivos ocultos
 - git pull origin master	=> puxa o conteudo que esta no repositorio remoto

clonando o arquivo pelo desktop no terminal
  No repositorio remoto clica em 'Code' e copie o url
  no git digite o seguinte comando e o url que foi copiado:
    - git clone https://github...
