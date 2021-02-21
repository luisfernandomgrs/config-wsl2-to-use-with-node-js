<h1>Configurações do ambiente - Node.js</h1>

<h2>Preparando ambiente WSL2/Ubuntu, VS Code para Nodejs e sub-pacotes</h2>
</br>
<p>Olá pessoal, o objetivo deste artigo é ajudar a preparar o ambiente windows usando o WSL e o VS Code para um projeto com Node.JS</br>
<code>Este projeto é baseado no que foi publicado pela Rocketseat para o NLW #04 de Março de 2021.</code>
Dito isso, vamos seguir.</p>

<h3>Vou levar em consideração que você já tenha o WSL2 instalado e configurado e que também já tenha o VS Code, instalado no seu Windows</h3>

<h2>Preparando o ambiente</h2>

Vamos ao conteúdo principal desse guia: configuração do seu ambiente para o NLW. Teremos três etapas principais na seção "**Instalação"**:

- Node + NPM;
- Yarn;
- Visual Studio Code e configurações.

# Node e NPM

O primeiro passo é instalar o Node.js, que vem acompanhado do NPM.

## Linux (Ubuntu/Debian)

Para o Linux iremos utilizar o **[NodeSource](https://github.com/nodesource/distributions/blob/master/README.md)**, basta seguir esses passos:

- Verifique se você possui o **[curl](https://curl.haxx.se/)** instalado rodando no terminal o comando:

```bash
curl --version
```

Caso ele retorne a versão, pode pular para o próximo passo. Caso não, basta rodar o comando:

```bash
sudo apt install curl
```

- Com o **curl** instalado, execute o comando de instalação da versão LTS mais recente disponível:
    - Ubuntu

    ```bash
    curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
    sudo apt-get install -y nodejs
    ```

Feche o terminal e abra novamente para as alterações fazerem efeito.

- Por fim, execute os seguintes comandos no terminal:

```bash
node -v
npm -v
```

Caso retorne as versões do Node e npm, sua instalação foi um sucesso.



# Yarn 1

## Linux (Ubuntu/Debian)

Para instalar o Yarn 1 no Linux vamos começar configurando o repositório do **Yarn** executando:

```bash
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```

Instale utilizando o seguinte comando:

```bash
 sudo apt update && sudo apt install --no-install-recommends yarn
```

Adicione ao arquivo `~/.bashrc` (ou `~/.zshrc` caso você utilize o shell zsh) a seguinte linha: 

```bash
export PATH="$PATH:`yarn global bin`"
```
<p>Vou colocar como fiz este processo, levando em consideração que uso o zsh, ok.</p>
<code>
    vi ~/.zshrc

    # adicionei a instrução export acima, logo abaixo da instrução export do ZSH... ficando assim:
    export ZSH="/home/luisfernando/.oh-my-zsh"
    export PATH="$PATH:`yarn global bin`"
    
    # para sair, tecle ESC, logo após tecle ":x" sem aspas... Sua alteração será salva e o arquivo fechado.    
</code>

Se desejar, não precisa fechar o terminal... Pode exexutar o comando abaixo se estiver usando o ZSH:
<code>
    source ~/.zshrc
</code>

Feche e abra o terminal novamente, em seguida rode o comando:

```bash
 yarn --version
```

Caso retorne a versão do Yarn (acima de 1.0, abaixo de 2.0), a instalação ocorreu com sucesso.

# Personalização

Ainda tomando como base o processo de configuração da Rocketseat, segue algumas dicas de configuração do Visual Studio Code.

Pra essa sessão, vou optar por deixar o link do material publicado pela Rocketseat, já que meu objetivo era apenas garantir deixar um material de apoio para configuração do node.js usando WSL e VS Code caso o material original seja removido.

Então segue o link abaixo para a personalização do seu ambiente de Desenvolvimento.

<code>https://www.notion.so/1c09af201b4b49c5bf1678842a96d9ab</code>

Um abraço, :)
