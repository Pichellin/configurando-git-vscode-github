# 🚀 Configurando Git com VSCode e GitHub

Este guia fornece instruções objetivas para configurar e utilizar o Git com o Visual Studio Code e GitHub. Ideal para iniciantes que desejam criar, sincronizar e atualizar repositórios locais com seus perfis no GitHub.

---

## 🛠️ 1. Configuração Inicial do Git

Configure o Git com seu nome de usuário e e-mail:

```bash
git config --global user.name "SeuUsuario"
git config --global user.email "SeuUsuario@seuProvedor.com"
git config --global credential.helper store
```

> 💡 `credential.helper store` permite que suas credenciais fiquem salvas localmente.

---

## 🧱 2. Criando um Repositório no GitHub

1. Acesse [github.com](https://github.com).
2. Clique em **"New repository"**.
3. Defina um nome para o repositório (ex: `meu-projeto`).
4. Escolha se será público ou privado.
5. **Não** marque a opção “Initialize with a README”.
6. Clique em **"Create repository"**.

---

## 💻 3. Subindo seu Projeto pelo VSCode (Primeira Vez)

No terminal do VSCode, execute:

```bash
git init
git add .
git commit -m "Meu primeiro commit"
git branch -M main
git remote add origin https://github.com/SeuUsuario/SeuDiretorio.git
git push -u origin main
```

> Substitua `SeuUsuario` e `SeuDiretorio` pelo seu nome de usuário e nome do repositório.

---

## ⚠️ 4. Erros de Autenticação com Git/GitHub

Caso receba um erro semelhante a:

```bash
fatal: unable to access 'https://github.com/nomeUsuario/diretorio/': The requested URL returned error: 403
```

### Solução:
1. Acesse o **Gerenciador de Credenciais** do seu sistema operacional.
2. Remova qualquer entrada relacionada a `github.com`.
3. Tente novamente os comandos de `git push`.

> 🔁 Este mesmo procedimento se aplica quando você altera sua senha no GitHub.

---

## ⬆️ 5. Fazendo Upload de Atualizações no Projeto

Sempre que quiser atualizar o repositório, use os comandos abaixo:

```bash
git add .
git commit -m "Atualização no projeto"
git push
```

> Não é necessário repetir `git init`, `branch` ou `remote`, pois já foram configurados.

---

## ⬆️ 6. Upgrade ou Novo Repositório (Repetindo o Processo)

Para um novo repositório, repita:

```bash
git init
git add .
git commit -m "Repositório do perfil, SeuUsuario"
git branch -M main
git remote add origin https://github.com/SeuUsuario/NovoRepositorio.git
git push -u origin main
```

---

## 📦 Arquivo ZIP para Upload

Recomenda-se compactar todos os arquivos (ex: README, scripts, pastas de exemplo) em `.zip` antes de subir no GitHub se for fazer isso via navegador.

---

## ✅ Pronto! Git + VSCode + GitHub 100% funcional.
