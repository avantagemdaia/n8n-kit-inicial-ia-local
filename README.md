
# Kit Inicial de IA Local (Self-Hosted)

O **Kit Inicial de IA Local** é um modelo open-source com Docker Compose, projetado para configurar rapidamente um ambiente de IA e desenvolvimento low-code local.

![n8n.io - Screenshot](https://raw.githubusercontent.com/n8n-io/self-hosted-ai-starter-kit/main/assets/n8n-demo.gif)

Curado por [n8n.io](https://github.com/n8n-io), ele combina a plataforma n8n auto-hospedada com uma lista de ferramentas de IA compatíveis para facilitar a criação de fluxos de trabalho de IA localmente e com segurança.

> 🔎 [Leia o anúncio oficial](https://blog.n8n.io/self-hosted-ai/)

## 🔧 O que está incluído

✅ [**n8n auto-hospedado**](https://n8n.io/) – Plataforma low-code com mais de 400 integrações e componentes de IA avançados  
✅ [**Ollama**](https://ollama.com/) – Plataforma para rodar LLMs localmente  
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

### Executando com Docker Compose

#### Para usuários com GPU Nvidia

```bash
docker compose --profile gpu-nvidia up
```

> ⚠️ Nunca usou sua GPU Nvidia com Docker? Veja [as instruções da Ollama](https://github.com/ollama/ollama/blob/main/docs/docker.md)

#### Para usuários com GPU AMD (Linux)

```bash
docker compose --profile gpu-amd up
```

#### Para usuários de Mac (M1 ou superior)

Você pode rodar:
1. Somente via CPU (`docker compose up`)
2. Rodar **Ollama diretamente no Mac** e conectá-lo ao n8n no Docker.

Edite seu `.env`:
```
OLLAMA_HOST=host.docker.internal:11434
```

No n8n:
- Acesse http://localhost:5678/home/credentials
- Clique em “Local Ollama service” e atualize a URL base para:
```
http://host.docker.internal:11434/
```

#### Para outros casos (CPU)

```bash
docker compose --profile cpu up
```

## ⚡ Primeiros passos

1. Acesse http://localhost:5678/ para configurar o n8n.
2. Abra este fluxo: http://localhost:5678/workflow/srOnR8PAY3u4RSwb
3. Clique no botão **Chat**.
4. Aguarde o download do modelo Llama3.2 no Ollama (verifique o log do Docker).

## 🔗 Recursos disponíveis no n8n

- [AI Agent](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.agent/)
- [Classificador de texto](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.text-classifier/)
- [Extrator de informações](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.information-extractor/)

> 📝 Este kit é ideal para testes e projetos iniciais. Para produção, personalize conforme suas necessidades.

## 🔄 Atualizações

### Para Nvidia:
```bash
docker compose --profile gpu-nvidia pull
docker compose create && docker compose --profile gpu-nvidia up
```

### Para Mac:
```bash
docker compose pull
docker compose create && docker compose up
```

### Para CPU:
```bash
docker compose --profile cpu pull
docker compose create && docker compose --profile cpu up
```

## 📚 Leituras recomendadas

- [Agentes de IA na prática com n8n](https://blog.n8n.io/ai-agents/)
- [Tutorial de fluxo de IA](https://docs.n8n.io/advanced-ai/intro-tutorial/)
- [Langchain no n8n](https://docs.n8n.io/advanced-ai/langchain/langchain-n8n/)
- [Diferenças entre agentes e cadeias](https://docs.n8n.io/advanced-ai/examples/agent-chain-comparison/)
- [O que são bancos vetoriais?](https://docs.n8n.io/advanced-ai/examples/understand-vector-databases/)

## 🎥 Vídeo tutorial

- [Como instalar IA local com n8n](https://www.youtube.com/)

## 🛍️ Templates de IA

Veja ideias em: [Galeria oficial de workflows](https://n8n.io/workflows/categories/ai/)

## 📁 Trabalhando com arquivos locais

O kit cria uma pasta compartilhada (ex: `/data/shared`) que permite ao n8n acessar arquivos do disco.

Use os nodes:
- [Read/Write Files](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.filesreadwrite/)
- [Local File Trigger](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.localfiletrigger/)
- [Execute Command](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.executecommand/)

## 📜 Licença

Licenciado sob [MIT License](LICENSE)

## 💬 Suporte

Participe do [Fórum do n8n](https://community.n8n.io/)

- Compartilhe seus fluxos
- Tire dúvidas
- Sugira melhorias
