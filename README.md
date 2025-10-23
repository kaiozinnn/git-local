# 🧩 Aula Prática – Git Local + GitHub + GitFluence

## 🎯 Objetivos

- Aprender a utilizar o **Git** localmente para versionar projetos, criar commits, branches e manipular o histórico.
- Entender como integrar o repositório local ao **GitHub** e colaborar com outras pessoas usando **Pull Requests** e **GitFluence**.

---

## 🧱 1. Configuração Inicial

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
git config --global core.editor "code --wait"
git config --list
```

---

## 📂 2. Criar e Iniciar um Repositório

```bash
mkdir meu_projeto
cd meu_projeto
git init
```

---

## 🏷️ 3. Alterar a Branch Padrão para `main`

```bash
git branch -m master main
git config --global init.defaultBranch main
```

---

## 📄 4. Criar Arquivos e Verificar Status

```bash
echo "Meu primeiro arquivo" > readme.txt
git status
```

---

## 🧺 5. Adicionar Arquivos à Área de Staging

```bash
git add readme.txt
git add .
git status
```

---

## 💾 6. Fazer o Primeiro Commit

```bash
git commit -m "Primeiro commit - adiciona readme.txt"
```

---

## 🔍 7. Ver Histórico e Detalhes

```bash
git log
git log --oneline
git show
```

---

## ✏️ 8. Editar Arquivos e Registrar Mudanças

```bash
echo "Adicionando nova linha" >> readme.txt
git diff
git add readme.txt
git commit -m "Atualiza readme.txt com nova linha"
```

---

## ♻️ 9. Desfazer Mudanças

```bash
git restore readme.txt
git restore --staged readme.txt
```

---

## 🌿 10. Criar e Alternar Entre Branches

```bash
git branch
git branch nova_funcionalidade
git switch nova_funcionalidade
```

---

## 🧬 11. Fazer Commits em Outra Branch

```bash
echo "Nova feature" > feature.txt
git add feature.txt
git commit -m "Adiciona nova feature"
```

---

## 🔀 12. Voltar e Mesclar Mudanças

```bash
git switch main
git pull origin main
git merge nova_funcionalidade
```

---

## 🗑️ 13. Excluir Branches Locais

```bash
git branch -d nova_funcionalidade
```

---

## 🧹 14. Ignorar Arquivos com `.gitignore`

Conteúdo sugerido:

```
*.log
*.tmp
node_modules/
```

```bash
git add .gitignore
git commit -m "Adiciona arquivo .gitignore"
```

---

## 🧠 15. Visualizar Informações Úteis

```bash
git status
git log --oneline --graph --decorate
git diff
git show HEAD
```

---

## 💡 16. Exemplo de Fluxo Completo

```bash
git init
echo "Aula prática Git local" > readme.txt
git add .
git commit -m "Primeiro commit"
git branch dev
git switch dev
echo "Nova versão em desenvolvimento" >> readme.txt
git add .
git commit -m "Atualiza versão dev"
git switch main
git merge dev
git log --oneline --graph
```

---

## 🌐 17. Integração com GitHub

### 🔁 Fork e Clone

1. Faça fork do repositório original no GitHub:  
   `https://github.com/andersonrmgomes/git-local`
2. Clone o fork:

```bash
git clone https://github.com/SEU_USUARIO/git-local
cd git-local
git checkout -b documentacao-colaboracao
```

---

### 🤖 Uso do GitFluence

Acesse [GitFluence](https://www.gitfluence.com) e digite comandos como:

| Descrição | Comando |
|----------|---------|
| Criar e mudar para nova branch | `git checkout -b nome-da-branch` |
| Ver branches locais e remotos | `git branch -a` |
| Enviar branch remoto | `git push -u origin documentacao-colaboracao` |

---

### 📝 Editar e Subir Documentação

```bash
# Edite README.md ou outros arquivos
git add .
git commit -m "feat: adiciona documentação de integração com GitHub"
git push origin documentacao-colaboracao
```

---

### 📤 Abrir Pull Request

1. Acesse seu fork no GitHub.
2. Clique em **Compare & pull request**.
3. Envie o PR do seu branch para o `main` do repositório original.

---

### 👥 Adicionar Colaboradores ao Repositório Privado

1. Vá em **Settings > Access > Collaborators**.
2. Clique em **Add people**.
3. Pesquise o usuário e envie o convite.
4. O colaborador deve aceitar para ter acesso ao repositório.

---

## 🧩 Dica Final

Use o GitFluence para aprender comandos Git com base em frases simples.  
Exemplo: “delete a local branch” → `git branch -d nome-da-branch`

---

## 📘 Créditos

Material elaborado por *Anderson R. M. Gomes* 🧑‍🏫  
Atualizado com integração GitHub e GitFluence por Kaio Vinícius
