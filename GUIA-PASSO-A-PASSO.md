# 🎓 Guia Completo: Como Resolver os Exercícios

**Bem-vindo!** Este guia vai te ensinar **passo a passo** como fazer os exercícios do curso.

---

## 📋 Índice

1. [Primeira Vez: Setup Inicial](#primeira-vez-setup-inicial)
2. [Resolver um Exercício (Passo a Passo)](#resolver-um-exercício)
3. [Abrir Pull Request](#abrir-pull-request)
4. [Entender o Feedback do Bot](#entender-o-feedback)
5. [Corrigir e Reenviar](#corrigir-e-reenviar)
6. [Dúvidas Comuns](#dúvidas-comuns)

---

## 🆕 Primeira Vez: Setup Inicial

**Você só precisa fazer isso UMA VEZ!**

### Passo 1: Instalar o Git

#### Windows
1. Baixe: https://git-scm.com/download/win
2. Instale com as opções padrão
3. Abra o **Git Bash** (vai aparecer no Menu Iniciar)

#### Mac
```bash
# No Terminal
xcode-select --install
```

#### Linux (Ubuntu/Debian)
```bash
sudo apt install git
```

**Testar se funcionou:**
```bash
git --version
# Deve mostrar: git version 2.x.x
```

---

### Passo 2: Configurar o Git

Abra o terminal e rode:

```bash
# Seu nome (vai aparecer nos commits)
git config --global user.name "Seu Nome Completo"

# Seu email (o mesmo do GitHub)
git config --global user.email "seu@email.com"
```

**Verificar:**
```bash
git config --list
```

---

### Passo 3: Criar Conta no GitHub (se não tiver)

1. Acesse: https://github.com/signup
2. Crie sua conta
3. Confirme o email
4. Configure autenticação de dois fatores (recomendado)

---

### Passo 4: Fork do Repositório

1. Acesse: https://github.com/petrosbarreto/desenvolvimento-web-2026-exercicios
2. Clique no botão **Fork** (canto superior direito)
3. Clique em **Create fork**

**O que aconteceu?**
Você criou uma **cópia** do repositório na sua conta!

---

### Passo 5: Clonar o Repositório

Agora você vai **baixar** o repositório para seu computador.

1. No seu fork (na sua conta), clique no botão verde **Code**
2. Copie a URL (algo como: `https://github.com/SEU-USUARIO/desenvolvimento-web-2026-exercicios.git`)

No terminal:

```bash
# Vá para a pasta onde quer guardar (ex: Documentos)
cd ~/Documents  # Mac/Linux
cd C:\Users\SeuNome\Documents  # Windows

# Clone o repositório
git clone https://github.com/SEU-USUARIO/desenvolvimento-web-2026-exercicios.git

# Entre na pasta
cd desenvolvimento-web-2026-exercicios
```

**Pronto!** Agora você tem o repositório no seu computador! 🎉

---

## 🎯 Resolver um Exercício

Vamos resolver a **Aula 01** como exemplo.

### Passo 1: Abrir a Pasta no Editor

**Visual Studio Code (recomendado):**

```bash
# Instalar VS Code: https://code.visualstudio.com/

# Abrir o projeto
code .
```

**Ou use qualquer editor:**
- Sublime Text
- Atom
- Notepad++
- Até Bloco de Notas serve!

---

### Passo 2: Ler o README do Exercício

1. Abra o arquivo: `exercicios/aula01/README.md`
2. **Leia tudo com atenção!**
   - O que é pedido?
   - Quais são os requisitos?
   - Tem template inicial?

**Dica:** O README é seu melhor amigo! Tudo que você precisa está lá.

---

### Passo 3: Criar os Arquivos

Dentro de `exercicios/aula01/`, crie os arquivos pedidos:

```
exercicios/aula01/
├── index.html    ← Você vai criar
├── style.css     ← Você vai criar
├── script.js     ← Você vai criar (se pedido)
└── README.md     ← Já existe (instruções)
```

**No VS Code:**
- Clique direito na pasta `aula01`
- **New File**
- Digite o nome: `index.html`

---

### Passo 4: Começar pelo Template

A maioria dos exercícios tem um **template inicial** no README.

**Copie o template** e cole no seu arquivo!

**Exemplo (`index.html`):**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meu Exercício - Aula 01</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Olá, Mundo!</h1>
  
  <!-- TODO: Adicione seu código aqui -->
  
  <script src="script.js"></script>
</body>
</html>
```

---

### Passo 5: Desenvolver Incrementalmente

**NÃO tente fazer tudo de uma vez!**

Faça um pedacinho por vez:

1. **Estrutura HTML**
   - Crie as tags básicas
   - Teste no navegador (abra o `index.html`)

2. **Estilo CSS**
   - Adicione cores
   - Ajuste espaçamentos
   - Teste no navegador

3. **JavaScript** (se houver)
   - Comece pelo básico
   - Use `console.log()` para debugar
   - Teste no navegador

**A cada mudança:**
- Salve o arquivo (`Ctrl+S`)
- Dê refresh no navegador (`F5`)

---

### Passo 6: Testar MUITO

**Abra o DevTools (F12):**

- **Console:** Ver erros JavaScript
- **Elements:** Ver HTML e CSS aplicado
- **Network:** Ver requisições (para APIs)

**Checklist antes de enviar:**
- [ ] Funciona no Chrome/Firefox?
- [ ] Não tem erros no Console?
- [ ] Está responsivo? (teste redimensionando)
- [ ] Código está limpo e organizado?

---

### Passo 7: Salvar Progresso (Commit)

Quando terminar (ou quiser salvar progresso):

```bash
# Ver o que mudou
git status

# Adicionar TODOS os arquivos
git add .

# OU adicionar arquivo específico
git add exercicios/aula01/index.html

# Criar um commit (snapshot do seu trabalho)
git commit -m "feat(aula01): adicionar página de apresentação"
```

**Mensagens de commit boas:**
```bash
git commit -m "feat(aula01): adicionar estrutura HTML"
git commit -m "style(aula01): estilizar header e footer"
git commit -m "fix(aula01): corrigir erro no JavaScript"
```

---

## 📤 Abrir Pull Request

Quando o exercício estiver **pronto**:

### Passo 1: Enviar para o GitHub (Push)

```bash
git push origin main
```

**Se der erro "Permission denied":**

Você precisa autenticar. Escolha uma opção:

**Opção A: Personal Access Token (recomendado)**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Generate new token
3. Marque: `repo`, `workflow`
4. Copie o token (GUARDE BEM!)
5. Use o token como senha quando o Git pedir

**Opção B: SSH (avançado)**
- Siga: https://docs.github.com/pt/authentication/connecting-to-github-with-ssh

---

### Passo 2: Criar o Pull Request

1. Vá no **seu fork** no GitHub
2. Vai aparecer um banner amarelo: **Compare & pull request**
3. Clique nele!

**OU:**

1. Clique na aba **Pull requests**
2. **New pull request**
3. **base repository:** `petrosbarreto/desenvolvimento-web-2026-exercicios`
4. **base:** `main`
5. **head repository:** `SEU-USUARIO/desenvolvimento-web-2026-exercicios`
6. **compare:** `main`
7. **Create pull request**

---

### Passo 3: Preencher o PR

**Título (IMPORTANTE!):**
```
[Aula 01] Seu Nome Completo
```

**Exemplo:**
```
[Aula 01] João Silva Santos
```

**Descrição:**

```markdown
## ✅ O que foi feito

- Criei página de apresentação pessoal
- Adicionei foto e links
- Responsivo para mobile

## 🎨 Destaque

Usei gradient no header e animações CSS!

## ❓ Dúvidas

Não tive dúvidas, mas não sei se o código está 100% correto.
```

**Clique em: Create pull request**

---

## 🤖 Entender o Feedback do Bot

Em ~30 segundos, o bot vai comentar no seu PR!

### Exemplo de Comentário

```
## 🤖 Validação Automática - Aula 01

### 📊 Resultado: 85/100 ⭐⭐

**Detalhamento:**
- 📁 Estrutura: 28/30
- 📝 HTML: 25/30
- 🎨 CSS: 20/20
- ✨ Criatividade: 12/20

### ✅ O que está bom:
- HTML válido
- CSS externo linkado
- Tags semânticas usadas

### ❌ Problemas encontrados:
- Falta atributo `alt` em imagens
- Falta `<meta description>`

### 💡 Como melhorar:
- Adicione alt em todas as imagens
- Adicione meta description no <head>

🎉 Seu exercício está aprovado! (>70)
```

---

### Entendendo a Nota

| Nota | Nível | O que significa |
|------|-------|-----------------|
| 90-100 | ⭐⭐⭐ Excelente | Perfeito! Parabéns! |
| 70-89 | ⭐⭐ Bom | Aprovado, mas pode melhorar |
| 50-69 | ⭐ Regular | Precisa melhorar |
| 0-49 | ❌ Insuficiente | Refazer |

**Nota mínima para aprovar: 70/100**

---

## 🔧 Corrigir e Reenviar

Se tirou menos de 70 ou quer melhorar:

### Passo 1: Corrigir Localmente

Faça as correções no seu computador (nos arquivos).

---

### Passo 2: Commit das Correções

```bash
git add .
git commit -m "fix(aula01): adicionar alt nas imagens"
git push origin main
```

---

### Passo 3: Bot Valida Automaticamente!

**Não precisa abrir novo PR!**

O bot vai automaticamente validar novamente e comentar de novo com a nova nota! 🎉

---

## ❓ Dúvidas Comuns

### P: Posso usar bibliotecas (jQuery, Bootstrap)?

**R:** Depende do exercício. Se não mencionar, prefira **JavaScript puro**.

---

### P: Meu código não funciona. E agora?

**R:** Checklist:
1. **Console (F12):** Tem erros?
2. **Arquivo certo?** `script.js` está no lugar certo?
3. **Linkado?** `<script src="script.js">` está no HTML?
4. **Sintaxe:** Tem `;` faltando? `}` fechando?
5. **Google:** Pesquise o erro exato

**Ainda travado?** Abra uma Issue!

---

### P: Como abrir uma Issue?

1. Vá no repositório: https://github.com/petrosbarreto/desenvolvimento-web-2026-exercicios/issues
2. **New issue**
3. Escolha: **🆘 Dúvida sobre Exercício**
4. Preencha o template
5. **Submit**

**Professor ou colegas vão te ajudar!** 💪

---

### P: Posso colaborar com colegas?

**R:** Sim, PODEM discutir e ajudar uns aos outros!

❌ **NÃO PODE:** Copiar código inteiro
✅ **PODE:** Trocar ideias, explicar conceitos

**O código final deve ser SEU!**

---

### P: Esqueci de fazer commit. E agora?

```bash
# Ver status
git status

# Adicionar arquivos
git add .

# Commit
git commit -m "feat(aulaXX): descrição"

# Push
git push origin main
```

**Sempre pode fazer mais commits!**

---

### P: Como ver o ranking?

**Leaderboard:** https://petrosbarreto.github.io/desenvolvimento-web-2026-exercicios/leaderboard.html

Atualiza automaticamente a cada 5 minutos! 🏆

---

### P: Posso fazer exercícios fora de ordem?

**R:** Tecnicamente sim, mas **NÃO recomendo**.

Os exercícios são progressivos:
- Aula 01 → Básico
- Aula 20 → Avançado (precisa ter feito 01-19)

**Sugestão:** Faça na ordem! 📚

---

## 🎉 Resumo em 1 Minuto

```bash
# 1. Primeira vez: Fork + Clone
git clone https://github.com/SEU-USUARIO/desenvolvimento-web-2026-exercicios.git
cd desenvolvimento-web-2026-exercicios

# 2. Resolver exercício (ex: aula01)
cd exercicios/aula01/
# Criar index.html, style.css, etc
# Testar no navegador

# 3. Commit
git add .
git commit -m "feat(aula01): minha solução"
git push origin main

# 4. Abrir PR no GitHub
# Título: [Aula 01] Seu Nome

# 5. Aguardar bot (~30s)
# 6. Ver nota, corrigir se necessário
# 7. Repetir para outras aulas!
```

---

## 📞 Precisa de Ajuda?

- **Dúvida sobre exercício:** [Abrir Issue](https://github.com/petrosbarreto/desenvolvimento-web-2026-exercicios/issues/new/choose)
- **Bug no sistema:** [Reportar Bug](https://github.com/petrosbarreto/desenvolvimento-web-2026-exercicios/issues/new/choose)
- **Sugestão:** [Sugerir Melhoria](https://github.com/petrosbarreto/desenvolvimento-web-2026-exercicios/issues/new/choose)
- **Discord da turma:** [Entrar](https://discord.gg/...)

---

## 🏆 Dicas de Ouro

1. **Commit frequentemente** - Não espere terminar tudo
2. **Teste no navegador** - A cada mudança, dê F5
3. **Use DevTools (F12)** - Seu melhor amigo
4. **Google é seu aliado** - Pesquise erros
5. **Peça ajuda cedo** - Não fique travado por horas
6. **Veja PRs de colegas** - Aprenda com outros códigos
7. **Capriche no README** - Explique seu código
8. **Adicione criatividade** - Bônus para soluções únicas!

---

**Bons estudos e bom código! 🚀**

_Qualquer dúvida, abra uma Issue!_
