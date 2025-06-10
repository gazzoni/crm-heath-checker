# Configuração da Integração com n8n

## Setup do Webhook

1. **Configure a variável de ambiente**:
   Crie um arquivo `.env.local` na raiz do projeto com:
   ```
   NEXT_PUBLIC_N8N_WEBHOOK_URL=https://your-n8n-instance.com/webhook/chat
   ```

2. **URLs de exemplo**:
   - n8n Cloud: `https://your-subdomain.app.n8n.cloud/webhook/chat`
   - n8n self-hosted: `https://your-domain.com/webhook/chat`
   - Desenvolvimento local: `http://localhost:5678/webhook/chat`

## Estrutura esperada do Webhook n8n

### Payload enviado para o n8n:
```json
{
  "message": "Mensagem do usuário",
  "timestamp": "2024-01-01T12:00:00.000Z",
  "sessionId": "session-1704110400000"
}
```

### Resposta esperada do n8n:
```json
{
  "response": "Resposta do agente IA"
}
```

**Ou alternativamente:**
```json
{
  "message": "Resposta do agente IA"
}
```

**Ou:**
```json
{
  "text": "Resposta do agente IA"
}
```

## Configuração no n8n

1. Crie um novo workflow no n8n
2. Adicione um nó **Webhook** como trigger
3. Configure o webhook para aceitar POST requests
4. Adicione seu agente IA (OpenAI, Anthropic, etc.)
5. Configure a resposta para retornar o JSON no formato esperado

## Exemplo de workflow n8n básico:

```
Webhook → [Processar mensagem] → Agente IA → [Formatar resposta] → Responder
```

## Tratamento de Erros

A interface já inclui tratamento de erros automático. Se o webhook falhar, será exibida uma mensagem de erro amigável para o usuário.

## Desenvolvimento

Para testar localmente, você pode usar ferramentas como ngrok para expor seu n8n local:
```bash
ngrok http 5678
```

E usar a URL fornecida pelo ngrok na variável de ambiente. 