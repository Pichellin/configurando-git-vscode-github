# 🚀 Guia Completo: Git + VSCode + GitHub

Este guia é um material completo e didático para iniciantes que desejam configurar, subir, clonar e sincronizar projetos entre o Visual Studio Code e o GitHub. Ideal para alunos e profissionais em início de jornada com Git e controle de versão.

---

## 📌 Índice

1. [Configuração Inicial do Git](#-1-configuração-inicial-do-git)
2. [Criando um Repositório no GitHub](#-2-criando-um-repositório-no-github)
3. [Subindo um Projeto Local para o GitHub](#-3-subindo-um-projeto-local-para-o-github)
4. [Resolvendo Problemas de Autenticação](#-4-resolvendo-problemas-de-autenticação)
5. [Atualizando um Repositório (Push)](#-5-atualizando-um-repositório-push)
6. [Clonando um Repositório Existente (Clone)](#-6-clonando-um-repositório-existente-clone)
7. [Sincronizando Atualizações (Pull)](#-7-sincronizando-atualizações-pull)
8. [Dicas Finais e Boas Práticas](#-8-dicas-finais-e-boas-práticas)

---

## 🛠️ 1. Configuração Inicial do Git

Abra o terminal do VSCode e configure o Git com seu nome de usuário e e-mail:

```bash
git config --global user.name "SeuUsuario"
git config --global user.email "SeuUsuario@hotmail.com"
git config --global credential.helper store
```

> 💡 Use seu e-mail cadastrado no GitHub. O helper `store` salva as credenciais localmente.

---

## 🧱 2. Criando um Repositório no GitHub

1. Acesse [https://github.com](https://github.com).
2. Clique em **"New repository"**.
3. Informe o nome e a descrição do projeto.
4. **Não selecione** a opção “Initialize this repository with a README”.
5. Clique em **"Create repository"**.

---

## ⬆️ 3. Subindo um Projeto Local para o GitHub

No terminal do VSCode:

```bash
git init
git add .
git commit -m "Primeiro commit do projeto"
git branch -M main
git remote add origin https://github.com/SeuUsuario/SeuRepositorio.git
git push -u origin main
```

> Substitua `SeuUsuario` e `SeuRepositorio` pelos seus dados reais.

---

## ⚠️ 4. Resolvendo Problemas de Autenticação

Se ocorrer erro como:

```bash
fatal: unable to access 'https://github.com/usuario/repositorio/': The requested URL returned error: 403
```

### Solução:

1. Acesse o **Gerenciador de Credenciais** do sistema operacional.
2. Remova qualquer entrada relacionada ao `github.com`.
3. Repita o comando `git push`.

> 🔐 Também necessário após trocar a senha no GitHub.

---

## 🔁 5. Atualizando um Repositório (Push)

Após modificar arquivos locais, use:

```bash
git add .
git commit -m "Atualização no projeto"
git push
```

> Não precisa repetir os comandos de `init`, `branch` ou `remote`.

---

## 📥 6. Clonando um Repositório Existente (Clone)

Para baixar um projeto do GitHub para sua máquina:

```bash
git clone https://github.com/SeuUsuario/SeuRepositorio.git
```

Depois de clonar:

```bash
cd SeuRepositorio
```

---

## 🔄 7. Sincronizando Atualizações (Pull)

Se o repositório já foi clonado e deseja trazer atualizações do GitHub:

```bash
git pull
```

> Ideal para manter o projeto atualizado caso outras pessoas também trabalhem nele.

---

## 💡 8. Dicas Finais e Boas Práticas

- Commits devem ter mensagens claras e diretas.
- Sempre **puxe (`git pull`) antes de subir (`git push`)** em projetos colaborativos.
- Use branches para testar alterações sem afetar o projeto principal.
- Nunca salve arquivos sensíveis (senhas, tokens) no repositório.
- Utilize `.gitignore` para evitar que pastas desnecessárias sejam versionadas (ex: `node_modules`, `venv`, etc.).

---

## 📦 Empacotamento para GitHub

Se estiver usando o GitHub via navegador, você pode compactar o projeto em `.zip` e subir manualmente.

---

## ✅ Git, VSCode e GitHub integrados com sucesso!
