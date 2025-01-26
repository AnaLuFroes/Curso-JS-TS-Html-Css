
# Como subir um projeto para o repositório usando Git

Este guia descreve o processo para subir um projeto para um repositório remoto utilizando o Git.


## Pré-requisitos

Antes de começar, certifique-se de que você possui:

- Git instalado em sua máquina (https://git-scm.com/).
- Um repositório remoto criado (por exemplo, no GitHub, GitLab, Bitbucket, etc.).
- Acesso à linha de comando (terminal ou CMD).

## Passo a passo

### 1 - Inicializar um repositório local (opcional)
Se você ainda não inicializou o repositório no diretório (pasta) do projeto, navegue até seu diretório e use o comando:

```bash
git init
```
Isso cria um repositório Git no seu diretório local.

### 2 - Configurar o repositório remoto
Certifique-se de que o repositório remoto já foi criado na plataforma de sua escolha (github, gitlab, etc). Copie o URL HTTPS ou SSH fornecido pela plataforma. Para adicionar o repositório remoto, use o comando:

```bash
git remote add origin <URL_DO_REPOSITORIO>
```

Exemplo usando o link do repositório: 

```bash
git remote add origin https://github.com/usuario/nome-do-repositorio.git
```

### 3 - Adicionar arquivos ao controle de versão
Adicione todos os arquivos ao staging area com o comando:

```bash
git add .
```

Dica: O "." adiciona todos os arquivos do seu diretório (pasta). Para adicionar arquivos específicos, substitua o "." pelo nome do arquivo.

### 4 - Fazer um commit
Depois de adicionar os arquivos, você precisa criar um commit para salvar as alterações localmente. Use o comando:

```bash
git commit -m "Mensagem do commit"
```

Exemplo:

```bash
git commit -m "Adiciona estrutura inicial do projeto"
```

### 5 - Criar a branch "pai"
Crie a branch (ramificação) que deseja enviar para o repositório remoto:

```bash
git branch -M <nome_da_branch>
```

### 6 - Subir os arquivos para o repositório remoto
Para enviar os arquivos ao repositório remoto, utilize:

```bash
git push -u origin <nome_da_branch_escolhida_no_passo_anterior>
```

### 7 - Dica para alterações em projetos já existentes
Caso esteja subindo alterações futuras, basta repetir o passo 3 e 4 e após realizar eles salve as alterações com o seguinte comando:

```bash
git push
```

-------------------------------------------------------------------

## Comandos completos (resumo)

Se você está começando do zero, aqui está o conjunto completo de comandos para subir o projeto:

```bash
1 - git init
2 - git remote add origin <URL_DO_REPOSITORIO>
3 - git add .
4 - git commit -m "Mensagem descritiva do commit"
5 - git push -u origin main
```

## Cores
Verde - Novos Arquivos ou Pastas
Azul - Arquivos Modificados
Laranja - Arquivos prontos para serem enviados para o repositório remoto.
