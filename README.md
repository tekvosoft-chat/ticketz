# Whatz.Tekvosoft 🚀

[![Status](https://img.shields.io/badge/status-active-brightgreen)](https://whatz.tekvosoft.com)
[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/tekvosoft-chat/whatz.tekvosoft)
[![License](https://img.shields.io/badge/license-AGPL-lightgrey)](LICENSE)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Chat%20Now-brightgreen)](https://wa.me/5519995378302)

---

## About the Project

**Whatz.Tekvosoft** é uma plataforma de comunicação completa, integrando **CRM** e **Helpdesk**, usando **WhatsApp** como principal canal de interação com clientes.

Este projeto é uma versão que estou estendendo do **Ticketz**, derivado de um projeto **Open Source** e adaptado para oferecer **instalação e uso simplificados**, com foco em qualidade, facilidade de instalação e uso. ## 

OBRIGADO CLAUDEMIR!!!

---

## Original Authorship

Este projeto teve origem em um projeto Open Source do desenvolvedor **Cassio Santos** (licença MIT), e passou por diversas melhorias por outros autores.  

A primeira versão SaaS do Whaticket foi criada pelo desenvolvedor **Wender Teixeira**, incluindo uma versão Single usando a biblioteca **Baileys** para acesso ao WhatsApp.  

Devido à dificuldade de identificar todos os autores das melhorias, assumimos que todas as alterações seguem a mesma licença original.  

---

## Relicensing

As alterações deste projeto são disponibilizadas **gratuitamente**, sendo relicenciadas sob **AGPL**, garantindo que todos os usuários possam acessar o código-fonte.  

- É importante manter o link para o repositório na tela "About Ticketz".  
- Alterações próprias podem ser usadas livremente, mas qualquer uso comercial de partes adicionadas neste projeto exige fornecimento do código ou licença específica.

---

## Objective

O objetivo deste projeto é **melhorar e manter atualizações abertas** sobre o Whaticket SaaS, priorizando **qualidade do aplicativo, facilidade de instalação e uso**.  

Sempre que possível, ajustes serão reaplicados a projetos originais, **creditando os autores originais**.

---

## 🚀 Very Quick Start on a Public Server

**Pré-requisitos:**
- Ubuntu 20+ limpo
- Portas 80 e 443 abertas
- Domínio apontando para o servidor

Execute no servidor (substitua `seudominio.com.br` e `seuemail@gmail.com`):

```bash
curl -sSL https://raw.githubusercontent.com/tekvosoft-chat/ticketz-docker-acme/main/setup.sh | sudo bash -s seudominio.com.br seuemail@gmail.com
Login inicial: e-mail informado

Senha padrão: 123456 (alterar no primeiro acesso)

Em poucos minutos, a plataforma estará no ar.

🔄 Upgrade
Para atualizar o sistema:

bash
Copiar código
curl -sSL https://raw.githubusercontent.com/tekvosoft-chat/ticketz-docker-acme/refs/heads/main/update.sh | sudo bash
O servidor ficará offline brevemente e voltará com a versão mais recente.

📋 Inspect Logs
Todos os elementos rodam em containers Docker:

bash
Copiar código
cd ~/ticketz-docker-acme
docker compose logs -t        # relatório completo
docker compose logs -t -f     # seguir logs em tempo real
🛠 Running from Source Using Docker
Instale Docker CE e Git (veja guia oficial)

Clone o repositório:

bash
Copiar código
git clone https://github.com/allgood/ticketz.git
cd ticketz
💻 Running Locally
Configuração padrão: localhost.
Para rodar em rede local, altere .env-backend-local e .env-frontend-local com o IP desejado (ex: 192.168.0.10).

bash
Copiar código
docker compose -f docker-compose-local.yaml up -d
Inicializa bancos e tabelas

Login: admin@ticketz.host

Senha: 123456

Para parar:

bash
Copiar código
docker compose -f docker-compose-local.yaml down
🌐 Running on the Internet
Configure DNS para backend e frontend, e um e-mail para registro de certificado:

text
Copiar código
backend: api.ticketz.exemplo.com
frontend: ticketz.exemplo.com
email: ticketz@example.com
Edite .env-backend-acme e .env-frontend-acme com essas informações.

bash
Copiar código
sudo docker compose -f docker-compose-acme.yaml up -d
Login: e-mail do .env-backend-acme

Senha: 123456

O sistema reinicia automaticamente em cada reboot.

Para encerrar:

bash
Copiar código
sudo docker compose -f docker-compose-acme.yaml down
📞 Contato e Suporte
Email: david.h.queiroz@gmail.com

WhatsApp: 19 99537-8302

Site: whatz.tekvosoft.com

⚠️ Aviso Importante
Este projeto não possui afiliação com a Meta, WhatsApp ou suas empresas.
O uso do código é de responsabilidade total do usuário.
