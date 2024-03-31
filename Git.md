## Comandos básicos do Git

Para usar o Git, os desenvolvedores usam comandos específicos para copiar, criar, alterar e combinar código. Esses comandos podem ser executados diretamente na linha de comando ou usando um aplicativo como GitHub Desktop. Aqui estão alguns comandos comuns para usar o Git:

- `git init` inicializa um novo repositório Git e começa a acompanhar um diretório existente. Ele adiciona uma subpasta oculta dentro do diretório existente que contém a estrutura de dados interna necessária para o controle de versão.

- `git add` prepara uma alteração. O Git controla as alterações na base de código de um desenvolvedor, mas é necessário testar e tirar um instantâneo das alterações para incluí-las no histórico do projeto. Este comando executa o teste, a primeira parte do processo de duas etapas. Todas as mudanças que são testadas irão tornar-se parte do próximo instantâneo e parte do histórico do projeto. O teste e o commit separados dão aos desenvolvedores total controle sobre o histórico do seu projeto sem alterar como eles codificam e funcionam.

- `git clone` cria uma cópia local de um projeto que já existe remotamente. O clone inclui todos os arquivos, histórico e branches do projeto.

- `git fetch` atualiza os objetos e referências do repositório.

- `git pull` atualiza a linha de desenvolvimento local com atualizações do equivalente remoto. Os desenvolvedores usam este comando se um colega fez commits em um branch remoto, e eles gostaria de refletir essas alterações no seu ambiente local.

- `git log` exibe o histórico de todos os commits do repositório.

- `git checkout` posiciona na branch em que o trabalho será realizado.

- `git status` mostra o status das alterações como não controladas, modificadas ou preparadas.

- `git branch` mostra os branches que estão sendo trabalhados localmente.

- `git merge` mescla as linhas de desenvolvimento. De modo geral, esse comando é usado para combinar alterações feitas em dois branches distintos. Por exemplo, um desenvolvedor faria merge quando quisesse combinar alterações de um branch de recurso no branch principal para implantação.

- `git commit` salva o instantâneo no histórico do projeto e conclui o processo de controle de alterações. Em suma, um commit funciona como tirar uma foto. Qualquer item que tenha sido preparado com git add passará a fazer parte do instantâneo com git commit.

- `git push` atualiza o repositório remoto com todos os commits feitos localmente em um branch.

### Exemplo de um novo repositório
```
# inicializa as funções específicas do git
git init

# verificar as mudanças no projeto
git status

# adicione o novo arquivo ao git
git add arquivo.html

# adiciona mais de um arquivo ao git
git add .

# salve a criação do novo arquivo
git commit -m "comentários da alteração"

# salvar a criação de vários arquivos
git commit -a -m "comentários das alterações"

# forneça o caminho para o repositório que você criou no github
git remote add origin https://github.com/owner/repository.git

# nomear o branch principal
git branch -M main

# enviar as alterações para o github
git push -u origin main
```

### Exemplo de uma nova branch em um repositório existente
```
# clona um repositório remoto para o local
git clone https://github.com/owner/repository.git

# crie uma nova branch para armazenar novas alterações
git branch my-branch

# mudar para a nova branch
git checkout my-branch

# cria e muda para a nova branch
git checkout -b my-branch

# verificar as mudanças no projeto
git status

# salvar a criação de vários arquivos
git commit -a -m "comentários das alterações"

# enviar a nova branch e as alterações para o github
git push --set-upstream origin my-branch
```

### Exemplo de uma branch existente em um repositório existente
```
# atualizar a branch local
git pull

# atuliza todas as referências de branch
git fetch

# mude para a branch existente
git checkout branch-exist

# verificar todas as branch do repositório
git branch -a

# salve a criação do novo arquivo
git commit -a -m "comentários das alterações"

# enviar as alterações para o github
git push
```

### Exemplo de merge entre branch de um repositório
```
# mude para a branch principal
git checkout main

# verificar todas as branch do repositório
git branch -a

# verificar todos os commits do repositório
git log

# une o código da branch main ao código da my-branch
git merge my-branch

# enviar as alterações para o github
git push
```

### Exemplos diversos de arquivo e branch
```
# excluir arquivos que não serão versionados
git clean -f

# restaurar arquivo alterado
git checkout .\arquivo.html

# comparar duas branch
git diff origin/release/1.0.0..origin/feature/new
```

### Git global setup
```
git config --global user.name "User Name"
git config --global user.email "username@email.com"
```

### Create a new repository
```
git clone https://gitlab.com/company/envoirement/project/frontend.git
cd frontend
git switch --create main
touch README.md
git add README.md
git commit -m "add README"
git push --set-upstream origin main
```

### Push an existing folder
```
cd existing_folder
git init --initial-branch=main
git remote add origin https://gitlab.com/company/envoirement/project/frontend.git
git add .
git commit -m "Initial commit"
git push --set-upstream origin main
```

### Push an existing Git repository
```
cd existing_repo
git remote rename origin old-origin
git remote add origin https://gitlab.com/company/envoirement/project/frontend.git
git push --set-upstream origin --all
git push --set-upstream origin --tags
```
