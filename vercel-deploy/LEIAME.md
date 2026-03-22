# Premium Películas — Deploy Vercel

## Estrutura
```
premium-peliculas/
├── index.html       ← Site completo
├── vercel.json      ← Configuração do Vercel
└── api/
    └── analyze.js   ← Proxy seguro para a API de IA
```

## Como fazer o deploy

### Passo 1 — Acesse o Vercel
Vá em: https://vercel.com/new

### Passo 2 — Upload da pasta
Arraste a pasta `premium-peliculas` inteira para a área de deploy
OU conecte via GitHub (recomendado para atualizações futuras)

### Passo 3 — Configurar a API Key (OBRIGATÓRIO para o diagnóstico IA)
Após o deploy, acesse:
**Settings → Environment Variables**

Adicione:
- **Name:** `ANTHROPIC_API_KEY`
- **Value:** sua chave da API Anthropic (começa com `sk-ant-...`)
- **Environment:** Production, Preview, Development

Clique em **Save** e depois em **Redeploy**.

### Passo 4 — Domínio próprio (opcional)
Em **Settings → Domains**, adicione seu domínio.
Ex: `premiumpeliculas.com.br`

## Onde obter a API Key
1. Acesse: https://console.anthropic.com
2. Vá em **API Keys**
3. Clique em **Create Key**
4. Copie a chave e cole no Vercel

## Atualizar o site no futuro
Basta fazer novo deploy arrastando a pasta atualizada no Vercel.
