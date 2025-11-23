# Exercício: Examine as Configurações do GitHub Copilot e os Recursos da Interface do Usuário

## Objetivo

Neste exercício, você irá explorar as configurações do GitHub Copilot e se familiarizar com a interface do usuário no Visual Studio Code.

## Pré-requisitos

- Visual Studio Code instalado
- GitHub Copilot instalado e ativado
- Conta do GitHub com acesso ao Copilot

## Parte 1: Explorando as Configurações

### Tarefa 1.1: Acessar as Configurações do Copilot

1. Abra o Visual Studio Code
2. Pressione `Ctrl+,` (Windows/Linux) ou `Cmd+,` (Mac) para abrir as Configurações
3. Na barra de pesquisa, digite "GitHub Copilot"
4. Observe todas as configurações disponíveis

**Resultado Esperado**: Você deve ver uma lista de configurações relacionadas ao GitHub Copilot.

### Tarefa 1.2: Explorar Configurações Principais

Identifique e anote as seguintes configurações:

- [ ] `github.copilot.enable` - Controle global do Copilot
- [ ] `editor.inlineSuggest.enabled` - Sugestões inline
- [ ] `github.copilot.editor.enableAutoCompletions` - Autocompletações

**Exercício**: 
1. Desabilite o Copilot usando a configuração `github.copilot.enable`
2. Observe o ícone na barra de status (deve mostrar que está desabilitado)
3. Reabilite o Copilot

### Tarefa 1.3: Configurar por Linguagem

1. Abra o arquivo `settings.json`:
   - Pressione `Ctrl+Shift+P` (Windows/Linux) ou `Cmd+Shift+P` (Mac)
   - Digite "Preferences: Open Settings (JSON)"
   - Pressione Enter

2. Adicione a seguinte configuração:

```json
{
  "github.copilot.enable": {
    "*": true,
    "plaintext": false,
    "markdown": true
  }
}
```

3. Salve o arquivo

**Resultado Esperado**: O Copilot agora está desabilitado para arquivos de texto simples, mas habilitado para Markdown.

## Parte 2: Explorando a Interface do Usuário

### Tarefa 2.1: Ícone da Barra de Status

1. Localize o ícone do GitHub Copilot na barra de status (canto inferior direito)
2. Clique no ícone
3. Observe as opções disponíveis

**Questões**:
- Quais opções aparecem quando você clica no ícone?
- O que indica cada estado do ícone (ativo, inativo, erro)?

### Tarefa 2.2: Sugestões Inline

1. Crie um novo arquivo chamado `exemplo.js`
2. Comece a digitar o seguinte código:

```javascript
// Função para calcular a soma de dois números
function somar
```

3. Aguarde uma sugestão do Copilot aparecer (texto em cinza)
4. Pratique a navegação:
   - Pressione `Alt+]` (ou `Option+]` no Mac) para ver a próxima sugestão
   - Pressione `Alt+[` (ou `Option+[` no Mac) para ver a sugestão anterior
   - Pressione `Tab` para aceitar uma sugestão
   - Pressione `Esc` para rejeitar

**Resultado Esperado**: Você deve conseguir navegar entre diferentes sugestões e aceitar/rejeitar conforme necessário.

### Tarefa 2.3: Painel de Sugestões Múltiplas

1. No arquivo `exemplo.js`, posicione o cursor em uma nova linha
2. Comece a escrever um comentário: `// Função para validar email`
3. Pressione `Ctrl+Enter`
4. Observe o painel que abre com múltiplas sugestões

**Exercício**:
- Navegue entre as diferentes sugestões
- Selecione a que considerar mais adequada
- Feche o painel

### Tarefa 2.4: GitHub Copilot Chat

1. Abra o GitHub Copilot Chat:
   - Clique no ícone de chat na barra lateral, OU
   - Pressione `Ctrl+Alt+I` (Windows/Linux) ou `Cmd+Shift+I` (Mac)

2. Faça as seguintes perguntas ao Copilot:

   a) "Como criar uma função assíncrona em JavaScript?"
   
   b) "Explique o conceito de promises em JavaScript"
   
   c) "Gere um exemplo de código para ler um arquivo JSON em Node.js"

3. Observe e analise as respostas

**Questões**:
- As respostas foram claras e úteis?
- O código sugerido está correto?
- Como você pode usar esse recurso no seu dia a dia?

### Tarefa 2.5: Inline Chat

1. No arquivo `exemplo.js`, escreva uma função simples:

```javascript
function multiplicar(a, b) {
  return a * b;
}
```

2. Selecione a função inteira
3. Pressione `Ctrl+I` (Windows/Linux) ou `Cmd+I` (Mac)
4. Digite: "Adicione validação de parâmetros e tratamento de erros"
5. Pressione Enter e observe as modificações sugeridas

**Resultado Esperado**: O Copilot deve sugerir uma versão melhorada da função com validações.

### Tarefa 2.6: Menu de Contexto

1. No arquivo `exemplo.js`, selecione a função `multiplicar`
2. Clique com o botão direito
3. Procure pelas opções do Copilot no menu

**Exercício**:
- Experimente a opção "Explain This" (Explicar Isto)
- Experimente a opção "Generate Tests" (Gerar Testes)
- Experimente a opção "Generate Docs" (Gerar Documentação)

## Parte 3: Comandos via Command Palette

### Tarefa 3.1: Explorar Comandos

1. Pressione `Ctrl+Shift+P` (Windows/Linux) ou `Cmd+Shift+P` (Mac)
2. Digite "GitHub Copilot"
3. Observe todos os comandos disponíveis

**Liste pelo menos 5 comandos que você encontrou**:
1. _______________________________
2. _______________________________
3. _______________________________
4. _______________________________
5. _______________________________

### Tarefa 3.2: Testar Comandos Específicos

Execute os seguintes comandos e anote o resultado:

- [ ] `GitHub Copilot: Generate Tests` - Gera testes para código selecionado
- [ ] `GitHub Copilot: Explain This` - Explica código selecionado
- [ ] `GitHub Copilot: Fix This` - Corrige problemas no código

## Parte 4: Personalização Avançada

### Tarefa 4.1: Criar Configuração Personalizada

1. Abra o arquivo `settings.json` do VS Code
2. Adicione a seguinte configuração personalizada:

```json
{
  "github.copilot.enable": {
    "*": true,
    "yaml": false,
    "plaintext": false,
    "scminput": false
  },
  "editor.inlineSuggest.enabled": true,
  "editor.quickSuggestions": {
    "other": true,
    "comments": true,
    "strings": true
  }
}
```

3. Salve o arquivo
4. Teste a configuração criando arquivos de diferentes tipos

### Tarefa 4.2: Configuração por Workspace

1. Crie uma nova pasta para um projeto de teste
2. Abra a pasta no VS Code
3. Crie o arquivo `.vscode/settings.json` na raiz do projeto
4. Adicione configurações específicas do Copilot para este projeto:

```json
{
  "github.copilot.enable": {
    "*": true,
    "javascript": true,
    "typescript": true
  }
}
```

**Resultado Esperado**: O Copilot agora tem configurações específicas para este workspace.

## Parte 5: Prática com Casos Reais

### Tarefa 5.1: Gerar uma Classe

Use o Copilot para gerar uma classe completa:

1. Crie um arquivo `usuario.js`
2. Escreva o seguinte comentário:

```javascript
// Classe Usuario com propriedades nome, email, idade e métodos para validação
```

3. Deixe o Copilot sugerir a implementação completa
4. Revise e ajuste conforme necessário

### Tarefa 5.2: Gerar Testes Unitários

1. Selecione a classe que você criou
2. Use o comando `GitHub Copilot: Generate Tests`
3. Observe os testes gerados
4. Analise se os testes cobrem os casos principais

### Tarefa 5.3: Refatorar Código

1. Escreva uma função com código repetitivo:

```javascript
function calcularDesconto(preco, tipo) {
  if (tipo === 'bronze') {
    return preco * 0.95;
  } else if (tipo === 'prata') {
    return preco * 0.90;
  } else if (tipo === 'ouro') {
    return preco * 0.85;
  } else {
    return preco;
  }
}
```

2. Selecione a função
3. Use o Inline Chat (`Ctrl+I`) e peça: "Refatore esta função para usar um objeto de configuração"
4. Analise a sugestão de refatoração

## Parte 6: Atalhos de Teclado

### Tarefa 6.1: Memorizar Atalhos Principais

Pratique os seguintes atalhos até se sentir confortável:

| Ação | Atalho (Windows/Linux) | Atalho (Mac) | Praticado ✓ |
|------|------------------------|--------------|-------------|
| Aceitar sugestão | `Tab` | `Tab` | [ ] |
| Rejeitar sugestão | `Esc` | `Esc` | [ ] |
| Próxima sugestão | `Alt+]` | `Option+]` | [ ] |
| Sugestão anterior | `Alt+[` | `Option+[` | [ ] |
| Painel de sugestões | `Ctrl+Enter` | `Ctrl+Enter` | [ ] |
| Copilot Chat | `Ctrl+Alt+I` | `Cmd+Shift+I` | [ ] |
| Inline Chat | `Ctrl+I` | `Cmd+I` | [ ] |

## Parte 7: Reflexão e Aprendizado

### Questões de Reflexão

1. **Quais configurações do GitHub Copilot você considera mais úteis?**
   
   _Sua resposta:_

2. **Qual recurso da interface do usuário você achou mais produtivo?**
   
   _Sua resposta:_

3. **Como você pode integrar o Copilot no seu fluxo de trabalho diário?**
   
   _Sua resposta:_

4. **Quais precauções você deve tomar ao usar sugestões do Copilot?**
   
   _Sua resposta:_

5. **Em que situações você preferiria desabilitar o Copilot?**
   
   _Sua resposta:_

## Checklist de Conclusão

Certifique-se de ter completado todas as tarefas:

- [ ] Explorei as configurações do GitHub Copilot
- [ ] Identifiquei as principais opções de configuração
- [ ] Configurei o Copilot para diferentes linguagens
- [ ] Explorei o ícone da barra de status
- [ ] Pratiquei com sugestões inline
- [ ] Usei o painel de sugestões múltiplas
- [ ] Experimentei o GitHub Copilot Chat
- [ ] Usei o Inline Chat
- [ ] Explorei o menu de contexto
- [ ] Testei comandos via Command Palette
- [ ] Criei configurações personalizadas
- [ ] Configurei settings por workspace
- [ ] Pratiquei com casos reais
- [ ] Memorizei os atalhos principais
- [ ] Respondi às questões de reflexão

## Próximos Passos

Após completar este exercício, você deve:

1. Continuar praticando o uso do Copilot em seus projetos reais
2. Experimentar diferentes configurações para encontrar o que funciona melhor para você
3. Explorar recursos avançados do Copilot conforme se sentir mais confortável
4. Compartilhar suas descobertas e melhores práticas com sua equipe

## Recursos Adicionais

- [Guia Completo do Copilot](./GUIA_COPILOT.md)
- [Documentação Oficial](https://docs.github.com/en/copilot)
- [Melhores Práticas](https://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)

---

**Parabéns por completar este exercício!** Você agora tem uma compreensão sólida das configurações e da interface do GitHub Copilot no Visual Studio Code.
