# Chat Interface

Uma interface de chat moderna e responsiva construída com Next.js, React e TypeScript, integrada com agentes IA via webhook do n8n.

## 🚀 Características

- ✨ Interface moderna e responsiva
- 📱 Otimizada para mobile e desktop
- 🎯 Efeito de streaming em tempo real
- 🔗 Integração com n8n via webhook
- 🎨 Design limpo com Tailwind CSS
- 📳 Feedback tátil (vibração no mobile)
- 🔄 Seções de conversa organizadas

## 🛠️ Tecnologias

- **Next.js 15** - Framework React
- **TypeScript** - Tipagem estática
- **Tailwind CSS** - Estilização
- **Lucide React** - Ícones
- **n8n** - Automação e agentes IA

## 📋 Pré-requisitos

- Node.js 18+ 
- pnpm, npm ou yarn
- Instância do n8n (local ou cloud)

## 🚀 Instalação

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/chat-interface.git
   cd chat-interface
   ```

2. **Instale as dependências:**
   ```bash
   pnpm install
   # ou
   npm install
   ```

3. **Configure as variáveis de ambiente:**
   ```bash
   cp .env.example .env.local
   ```
   
   Edite o arquivo `.env.local`:
   ```env
   NEXT_PUBLIC_N8N_WEBHOOK_URL=https://your-n8n-instance.com/webhook/chat
   ```

4. **Execute o projeto:**
   ```bash
   pnpm dev
   # ou
   npm run dev
   ```

5. **Acesse:** [http://localhost:3000](http://localhost:3000)

## 🔧 Configuração do n8n

Para configurar a integração com n8n, consulte o arquivo [README-n8n-setup.md](./README-n8n-setup.md) que contém instruções detalhadas sobre:

- Configuração do webhook
- Estrutura do workflow
- Formato dos dados
- Exemplos práticos

## 📱 Uso

1. Digite sua mensagem no campo de texto
2. Pressione Enter (desktop) ou Cmd+Enter (mobile/desktop) para enviar
3. Aguarde a resposta do agente IA com efeito de streaming
4. Use os botões para funcionalidades extras (Add, DeepSearch, Think)

## 🎨 Customização

### Cores e Tema
Edite as classes do Tailwind CSS no arquivo `chat-interface.tsx` para personalizar cores e estilos.

### Velocidade do Streaming
Ajuste as constantes no arquivo:
```typescript
const WORD_DELAY = 40 // ms por palavra
const CHUNK_SIZE = 2 // Número de palavras por vez
```

## 📂 Estrutura do Projeto

```
├── app/                 # Páginas e layouts do Next.js
├── components/          # Componentes reutilizáveis
├── hooks/              # Custom hooks
├── lib/                # Utilitários e configurações
├── public/             # Arquivos estáticos
├── styles/             # Estilos globais
├── chat-interface.tsx  # Componente principal do chat
└── README-n8n-setup.md # Instruções do n8n
```

## 🤝 Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para detalhes.

## 👨‍💻 Autor

**Guilherme Gazzoni**

---

⭐ Deixe uma star se este projeto te ajudou! 