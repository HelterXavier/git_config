
# 📘 Git e GitHub — Anotações

## ✅ O que é Git?

O **Git** é um sistema de controle de versão que permite rastrear as alterações feitas em seus arquivos ao longo do tempo. Com o Git, é possível:

- Reverter arquivos para versões anteriores (como uma **máquina do tempo** 🕒).
- Trabalhar em cópias isoladas de arquivos e mesclar alterações à versão principal depois de testadas e aprovadas.

> **Exemplo**: Se estiver trabalhando em uma página de destino de um site e decidir alterar a barra de navegação, você pode criar uma cópia do arquivo, editar essa barra e depois mesclar as alterações à versão principal.

### 📄 Estados dos arquivos

- **Untracked** → Arquivo novo que ainda não está sendo monitorado pelo Git.
- **Tracked** → Arquivo que já está sendo monitorado.
- **Modified** → Arquivo rastreado que sofreu modificações.
- **Staged** → Arquivo modificado que está pronto para ser enviado para o repositório (commitado).

## ⚙️ Como instalar o Git

Acesse: [https://git-scm.com/downloads](https://git-scm.com/downloads)

## 🔧 Como configurar

```bash
# Verificar versão
git --version

# Configurar usuário global
git config --global user.name "SEU_NOME_DE_USUARIO"
git config --global user.email "SEU_E-MAIL"
```

## 🚀 Inicializar um repositório Git

```bash
git init                         # Inicializa o repositório
git add .                        # Adiciona todos os arquivos
git add caminho/arquivo.txt      # Adiciona arquivo específico
git status                       # Verifica status atual
git commit -m "My first commit"  # Cria commit
git push                         # Envia para repositório remoto
```

## 🔁 Outros comandos úteis

```bash
git merge                        # Mescla branches
git checkout nome-da-branch      # Muda para outra branch
git mv nome_atual novo_nome      # Renomeia/move arquivos
git log --oneline                # Histórico resumido de commits
git commit --amend -m "Nova msg" # Corrige último commit
git reset --hard HEAD            # Volta ao último commit
git checkout -- arquivo.txt      # Desfaz alterações no arquivo
git revert <hash>                # Reverte um commit criando outro
git reset HEAD~1                 # Desfaz o último commit
```

## 🌿 Branches no Git

Branches permitem trabalhar em cópias isoladas do código sem afetar a base principal.

- `master` → Principal
- `git branch` → Lista branches
- `git branch nome-da-branch` → Cria nova branch
- `git checkout nome-da-branch` → Muda para branch
- `git branch -d nome-da-branch` → Deleta branch
- `git rebase` → Reorganiza histórico de commits
- `git fetch` → Baixa commits sem merge
- `git pull` → Fetch + merge/rebase
- `git init --bare` → Cria repositório remoto
- `git clone url` → Clona repositório remoto

## ✍️ Padrões de Commit

### Estrutura da mensagem

```
feat: <descrição>
:emoji: <tipo>(escopo): <descrição>
```

> **Nota**: Emoji e escopo são opcionais, mas recomendados.

### Tipos comuns

| Tipo     | Descrição |
|----------|-----------|
| `feat`   | Novo recurso (MINOR) |
| `fix`    | Correção de bug (PATCH) |
| `docs`   | Mudanças na documentação |
| `style`  | Estilo/código (sem alteração de lógica) |
| `refactor` | Refatoração sem mudar funcionalidade |
| `test`   | Adição/modificação de testes |
| `build`  | Alterações em build/dependências |
| `chore`  | Tarefas administrativas/configurações |

## 🧩 Emojis de Commits

| Tipo                     | Emoji |
|--------------------------|-------|
| Commit inicial           | 🎉 `:tada:` |
| Tag de versão            | 🔖 `:bookmark:` |
| Novo recurso             | ✨ `:sparkles:` |
| Lista de ideias/tasks    | 🔜 `:soon:` |
| Bugfix                   | 🐛 `:bug:` |
| Documentação             | 📚 `:books:` |
| Testes                   | 🧪 `:test_tube:` |
| Adicionando teste        | ✅ `:white_check_mark:` |
| Teste de aprovação       | ✔️ `:heavy_check_mark:` |
| Acessibilidade           | ♿ `:wheelchair:` |
| Texto                    | 📝 `:pencil:` |
| Package.json             | 📦 `:package:` |
| Em progresso             | 🚧 `:construction:` |
| Arquivos de configuração | 🔧 `:wrench:` |
| Remover dependência      | ➖ `:heavy_minus_sign:` |
| Adicionar dependência    | ➕ `:heavy_plus_sign:` |
| Reverter mudanças        | 💥 `:boom:` |
| Alterações após review   | 👌 `:ok_hand:` |
| Refatoração              | ♻️ `:recycle:` |
| Mover/Renomear arquivos  | 🚚 `:truck:` |
