
# Kit Inicial de IA Local (Self-Hosted)

💻 **Este repositório foi adaptado para rodar no Windows 11 usando Docker Desktop.**
⚠️ A funcionalidade de rodar modelos de linguagem localmente com Ollama foi removida nesta versão para garantir compatibilidade total com Windows.
👨‍💻 Usuários de macOS podem seguir as mesmas instruções com Docker Desktop instalado.



O **Kit Inicial de IA Local** é um modelo open-source com Docker Compose, projetado para configurar rapidamente um ambiente de IA e desenvolvimento low-code local.

![n8n.io - Screenshot](https://raw.githubusercontent.com/n8n-io/self-hosted-ai-starter-kit/main/assets/n8n-demo.gif)

Curado por [n8n.io](https://github.com/n8n-io), ele combina a plataforma n8n auto-hospedada com uma lista de ferramentas de IA compatíveis para facilitar a criação de fluxos de trabalho de IA localmente e com segurança.

> 🔎 [Leia o anúncio oficial](https://blog.n8n.io/self-hosted-ai/)

## 🔧 O que está incluído

✅ [**n8n auto-hospedado**](https://n8n.io/) – Plataforma low-code com mais de 400 integrações e componentes de IA avançados  
✅ [**Qdrant**](https://qdrant.tech/) – Banco vetorial open-source de alta performance  
✅ [**PostgreSQL**](https://www.postgresql.org/) – Armazena dados com segurança em escala

## 💡 O que você pode construir

⭐️ **Agentes de IA** para agendamentos  
⭐️ **Resumo de PDFs da empresa** com privacidade  
⭐️ **Bots inteligentes para Slack**  
⭐️ **Análise de documentos financeiros** de forma local e econômica

## 🚀 Instalação

### Clonar o repositório

```bash
git clone https://github.com/n8n-io/n8n-kit-inicial-ia-local.git
cd n8n-kit-inicial-ia-local
cp .env.example .env  # Atualize as senhas e chaves
```


### Executando com Docker Desktop (Windows 11 ou macOS)

Este projeto foi adaptado para rodar com Docker Desktop no Windows 11.

```bash
docker compose up
```

💡 No macOS, também é possível rodar normalmente com Docker. Certifique-se de que o Docker está instalado corretamente.


