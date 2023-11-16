# Autenticando utilizando Token

1. Gerando um token
    - Na página do Github, ao lado direito, click na foto do perfil
    - Selecione "Setings" no menu suspenso que irá aparecer
    - Após clicar e abrir as configurações, vá até o final da página e click em "Developer settings"
    - Click em "Personal access tokens" e selecione "Tokens (classic)"
    - Click na caixa de seleção do lado direito "Generate new token".
    - Selecione no menu suspenso a opção "Generate new token (classic)"
    - Insira a senha do github
    - Na página direcionada, preencha as informações e configure o que for necessário
    - Após configurar o que for necessário, no fim da página, click em "Generate token"
    - copie o token que foi gerado

2. Fazendo autenticação
    - Após criar um repositório ou em um já criado, click no botão "<> Code", selecione a opção "HTTPS" no cabeçalho e copie o link que está na barra de endereço logo abaixo do cabeçalho.
    - Abra o git bash here na pasta do seu computador que deseja clonar o projeto
    - utilize o codigo abaixo, seguido da url copiada
        git clone
    - Irá solicitar o nome de usuário, insira o mesmo
    - Agora ira solicitar a senha, nesse momento, cole o token que foi criado e copiado.
    - Sucesso, agora os arquivos foram clonados

3. Salvando o token permanente ou temporariamente
    - Para temporáriamente, utilize o codigo
        git config --global credential.helper cache
    - Para salvar sendo que apenas você utiliza o computador, use
        git config --global credential.helper store
    - Repita a etapa 2 e para os proxímos o git não irá pedir mais as credenciais

4. Verificando as informações
    - Para ver qual local está salvo as informações
        git config --global --show-origin credential.helper
    - Para abrir e verificar o que está escrito no arquivo
        cat .gitconfig
    - Para verificar qual o token que foi salvo
        cat .git-credentials
