# Informações

quando abre o *git bash here* a janela apresenta o nome de usuário,  
seguido com o nome do computador e logo após o endereço do diretorio

## Atalhos e códigos

- git config => visualizar informações e variáveis
- Ctrl + "+" => maximiza as letras
- Ctrl + "-" => minimiza as letras
- Ctrl + L => limpa o que está escrito no terminal
- cat => seguido por um nome de arquivo, irá abrir o mesmo
- cd => sai do diretorio que estava e vai para a raiz
- ls => lista todos os arquivos no local que está

## Primeiras configurações do Git

Como inserir o nome e email para todos os repositorios que criar

- Utilize o comando
    git config --global user.name "NomeDoUsuario"
    git config --global user.name email@email.com

- Verificando variaveis
    git config user.name
    git config user.email

Como alterar o nome da Branch padrão do Git

- Utilize o comando
    git config --global init.defaultBranch NeWBranch
- Verificando o nome da Branch
    git config init.defaultBranch

Como verificar as variaveis

- Verificar o caminho e valor de todas variaveis
    git config --list --show-origin
- Verifica o caminho e valor das variaveis globais
    git config --global --list --show-origin
- Verifica apenas os valores das variaveis
    git config --global --list

 obs.:para ver detalhado as variavies de informações de cada uma  
 basta trocar o "--global" pelas outras informações que tem no  
 *config file location* do *git config*
