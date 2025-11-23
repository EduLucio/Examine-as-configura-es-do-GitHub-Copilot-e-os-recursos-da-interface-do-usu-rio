# Referência Rápida: GitHub Copilot no VS Code

## 🚀 Atalhos de Teclado Essenciais

### Sugestões Inline
- **Aceitar sugestão**: `Tab`
- **Rejeitar sugestão**: `Esc`
- **Próxima sugestão**: `Alt+]` (Windows/Linux) / `Option+]` (Mac)
- **Sugestão anterior**: `Alt+[` (Windows/Linux) / `Option+[` (Mac)
- **Ver todas sugestões**: `Alt+\` (Windows/Linux) / `Option+\` (Mac)

### Chat e Interação
- **Painel de sugestões**: `Ctrl+Enter`
- **GitHub Copilot Chat**: `Ctrl+Alt+I` (Windows/Linux) / `Cmd+Shift+I` (Mac)
- **Inline Chat**: `Ctrl+I` (Windows/Linux) / `Cmd+I` (Mac)
- **Command Palette**: `Ctrl+Shift+P` (Windows/Linux) / `Cmd+Shift+P` (Mac)

## ⚙️ Configurações Principais

### settings.json

```json
{
  // Habilitar/Desabilitar Copilot por linguagem
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true,
    "javascript": true,
    "python": true,
    "java": true,
    "yaml": false
  },
  
  // Habilitar sugestões inline
  "editor.inlineSuggest.enabled": true,
  
  // Habilitar autocompletações
  "github.copilot.editor.enableAutoCompletions": true,
  
  // Sugestões rápidas
  "editor.quickSuggestions": {
    "other": true,
    "comments": true,
    "strings": true
  }
}
```

## 📋 Comandos Via Command Palette

Digite `Ctrl+Shift+P` / `Cmd+Shift+P` e depois:

- `GitHub Copilot: Enable` - Ativar
- `GitHub Copilot: Disable` - Desativar
- `GitHub Copilot: Open Chat` - Abrir chat
- `GitHub Copilot: Explain This` - Explicar código selecionado
- `GitHub Copilot: Fix This` - Corrigir código
- `GitHub Copilot: Generate Tests` - Gerar testes
- `GitHub Copilot: Generate Docs` - Gerar documentação
- `GitHub Copilot: Sign Out` - Sair

## 🎯 Estados do Ícone na Barra de Status

- **✓ (Verde com checkmark)**: Copilot ativo e funcionando
- **⊗ (Vermelho com X)**: Copilot desativado
- **⚠ (Amarelo com aviso)**: Problemas de autenticação ou conexão
- **... (Carregando)**: Processando sugestões

## 💡 Recursos da Interface

### 1. Sugestões Inline
- Aparecem como texto cinza enquanto você digita
- Navegue com `Alt+]` / `Alt+[`
- Aceite com `Tab`, rejeite com `Esc`

### 2. Painel de Sugestões (`Ctrl+Enter`)
- Mostra múltiplas sugestões
- Permite escolher a melhor opção
- Visualização completa do contexto

### 3. Copilot Chat
- Interface de conversação
- Faça perguntas sobre código
- Solicite explicações e refatorações
- Gere testes e documentação

### 4. Inline Chat (`Ctrl+I`)
- Chat contextual no editor
- Modifica código selecionado
- Gera código no cursor
- Perguntas sobre código atual

### 5. Menu de Contexto (Botão Direito)
- **Explain This**: Explica o código
- **Fix This**: Corrige problemas
- **Generate Tests**: Cria testes
- **Generate Docs**: Adiciona documentação

## 🔧 Configurações Avançadas

### Desabilitar para Arquivos Específicos

```json
{
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "scminput": false
  }
}
```

### Configuração por Workspace

Crie `.vscode/settings.json` no projeto:

```json
{
  "github.copilot.enable": {
    "*": true,
    "javascript": true,
    "typescript": true
  }
}
```

### Proxy Settings

```json
{
  "github.copilot.advanced": {
    "debug.overrideProxyUrl": "http://proxy.example.com:8080"
  }
}
```

## 📝 Exemplos de Uso

### 1. Gerar Função
```javascript
// Função para validar CPF
```
*Aguarde sugestão e pressione Tab*

### 2. Gerar Testes
1. Selecione a função
2. Botão direito → "Generate Tests"
3. Revise os testes gerados

### 3. Explicar Código
1. Selecione o código
2. Botão direito → "Explain This"
3. Leia a explicação no Chat

### 4. Refatorar com Inline Chat
1. Selecione o código
2. Pressione `Ctrl+I`
3. Digite: "Refatore para usar async/await"
4. Revise e aceite

## 🎓 Melhores Práticas

### ✅ Faça
- Revise sempre o código sugerido
- Use comentários descritivos para melhores sugestões
- Aproveite para aprender novos padrões
- Configure por linguagem conforme necessário
- Use o Chat para perguntas complexas

### ❌ Evite
- Aceitar código sem entender
- Usar em código de segurança crítica sem revisão
- Confiar cegamente em todas as sugestões
- Ignorar boas práticas do projeto
- Desabilitar completamente (use configuração por linguagem)

## 🔍 Solução de Problemas

### Copilot não sugere código
1. ✓ Verifique o ícone na barra de status
2. ✓ Confirme `editor.inlineSuggest.enabled`: true
3. ✓ Verifique autenticação GitHub
4. ✓ Reinicie VS Code

### Sugestões de baixa qualidade
1. ✓ Escreva comentários mais descritivos
2. ✓ Forneça mais contexto no código
3. ✓ Use nomes de variáveis/funções claros
4. ✓ Navegue entre sugestões (`Alt+]`)

### Erro de autenticação
1. `GitHub Copilot: Sign Out`
2. `GitHub Copilot: Sign In`
3. Complete autenticação no navegador

## 📊 Configurações Comuns por Tipo de Projeto

### Projeto JavaScript/TypeScript
```json
{
  "github.copilot.enable": {
    "*": true,
    "javascript": true,
    "typescript": true,
    "json": true
  }
}
```

### Projeto Python
```json
{
  "github.copilot.enable": {
    "*": true,
    "python": true,
    "jupyter": true
  }
}
```

### Projeto Web Full-Stack
```json
{
  "github.copilot.enable": {
    "*": true,
    "javascript": true,
    "typescript": true,
    "html": true,
    "css": true,
    "json": true
  }
}
```

## 🔗 Links Úteis

- [Documentação Oficial](https://docs.github.com/en/copilot)
- [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [Guia de Início Rápido](https://docs.github.com/en/copilot/quickstart)
- [Blog do GitHub](https://github.blog/tag/github-copilot/)

## 📞 Suporte

- **Problemas técnicos**: [GitHub Support](https://support.github.com/)
- **Feedback**: Dentro do VS Code via Command Palette
- **Comunidade**: [GitHub Community Discussions](https://github.com/orgs/community/discussions)

---

**Dica**: Mantenha esta referência aberta enquanto trabalha para consultas rápidas!
