# BetCandidate

BetCandidate é uma aplicação web construída com [Next.js](https://nextjs.org/) que permite apostas on-chain nas eleições de Condado-PE, utilizando a carteira MetaMask para autenticação e transações na blockchain.

## Objetivo

O objetivo do projeto é criar uma plataforma descentralizada onde os usuários possam apostar em candidatos de uma eleição municipal, de forma transparente e segura, utilizando criptomoedas (POL) na blockchain.

## Como funciona

1. **Acesso à plataforma:**  
   O usuário acessa a aplicação web e visualiza informações sobre a disputa eleitoral.

2. **Autenticação com MetaMask:**  
   Para apostar, o usuário deve conectar sua carteira MetaMask clicando no botão "Conectar MetaMask".  
   - Se a MetaMask não estiver instalada, será exibida uma mensagem de erro.
   - Após a conexão, o endereço da carteira é salvo no navegador.

3. **Realização de apostas:**  
   Após autenticar-se, o usuário é redirecionado para a página de apostas (`/bet`).  
   - O usuário escolhe um candidato e informa o valor em POL que deseja apostar.
   - A transação é assinada e enviada pela MetaMask diretamente para o contrato inteligente na blockchain.

4. **Encerramento da disputa:**  
   Quando a disputa é encerrada, o vencedor é definido no contrato inteligente.

5. **Resgate do prêmio:**  
   Usuários que apostaram no candidato vencedor podem solicitar o resgate do prêmio, que é transferido automaticamente para sua carteira.

## Tecnologias utilizadas

- [Next.js](https://nextjs.org/) (React)
- [Web3.js](https://web3js.readthedocs.io/) para interação com a blockchain
- [MetaMask](https://metamask.io/) para autenticação e assinatura de transações
- Smart contract (endereço: `0xEE4962E497eA0B8b12F5794D0B77dfB56632d832`)

## Como rodar o projeto

1. Instale as dependências:
   ```bash
   npm install
   ```

2. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```

3. Abra [http://localhost:3000](http://localhost:3000) no navegador.

> **Observação:**  
> É necessário ter a extensão MetaMask instalada no navegador e estar conectado à rede correta para interagir com o contrato.

## Estrutura principal

- `src/app/page.js`: Página inicial e autenticação com MetaMask.
- `src/app/bet/page.js`: Página de apostas e resgate de prêmios.
- `src/services/Web3Service.js`: Funções para interação com o contrato inteligente.

