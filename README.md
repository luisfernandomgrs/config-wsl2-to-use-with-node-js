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
