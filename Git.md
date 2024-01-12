## Comandos básicos do Git

Para usar o Git, os desenvolvedores usam comandos específicos para copiar, criar, alterar e combinar código. Esses comandos podem ser executados diretamente na linha de comando ou usando um aplicativo como GitHub Desktop. Aqui estão alguns comandos comuns para usar o Git:

- `git init` inicializa um novo repositório Git e começa a acompanhar um diretório existente. Ele adiciona uma subpasta oculta dentro do diretório existente que contém a estrutura de dados interna necessária para o controle de versão.

- `git clone` cria uma cópia local de um projeto que já existe remotamente. O clone inclui todos os arquivos, histórico e branches do projeto.

- `git add` prepara uma alteração. O Git controla as alterações na base de código de um desenvolvedor, mas é necessário testar e tirar um instantâneo das alterações para incluí-las no histórico do projeto. Este comando executa o teste, a primeira parte do processo de duas etapas. Todas as mudanças que são testadas irão tornar-se parte do próximo instantâneo e parte do histórico do projeto. O teste e o commit separados dão aos desenvolvedores total controle sobre o histórico do seu projeto sem alterar como eles codificam e funcionam.

- `git commit` salva o instantâneo no histórico do projeto e conclui o processo de controle de alterações. Em suma, um commit funciona como tirar uma foto. Qualquer item que tenha sido preparado com git add passará a fazer parte do instantâneo com git commit.

- `git status` mostra o status das alterações como não controladas, modificadas ou preparadas.

- `git branch` mostra os branches que estão sendo trabalhados localmente.

- `git merge` mescla as linhas de desenvolvimento. De modo geral, esse comando é usado para combinar alterações feitas em dois branches distintos. Por exemplo, um desenvolvedor faria merge quando quisesse combinar alterações de um branch de recurso no branch principal para implantação.

- `git pull` atualiza a linha de desenvolvimento local com atualizações do equivalente remoto. Os desenvolvedores usam este comando se um colega fez commits em um branch remoto, e eles gostaria de refletir essas alterações no seu ambiente local.

- `git push` atualiza o repositório remoto com todos os commits feitos localmente em um branch.

- `git log` exibe o histórico de todos os commits do repositório

Para obter mais informações, confira o guia de referência completo de comandos do Git.

### Contribuir para um repositório existente
```
# baixe um repositório no GitHub para sua máquina
git clone https://github.com/owner/repo.git

# crie uma nova branch para armazenar novas alterações
git branch my-branch

# mudar para a nova branch
git checkout my-branch

# adicionar arquivos
git add file.ext

# salvar alterações
git commit -a -m "my updates"

# enviar as alterações para o github
git push --set-upstream origin my-branch
```

### Inicie um novo repositório e publique-o no GitHub
Primeiro, você deverá criar um novo repositório no GitHub para guardar seu código.
```
# inicialize com funções específicas do git
git init my-repo

# adicione o novo arquivo ao git
git add README.md

# salve a criação do novo arquivo
git commit -m "add README to initial commit"

# forneça o caminho para o repositório que você criou no github
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git

# enviar as alterações para o github
git push --set-upstream origin main
```

### Contribuir para uma branch existente no GitHub
Nesse exemplo você já tem um projeto chamado repo no local e uma nova branch foi criada no GitHub remoto.
```
# atualizar todas as ramificações de rastreamento remoto e a ramificação atualmente em check-out
git pull

# mude para o branch existente chamado `feature-a`
git checkout feature-a

# adicione o novo arquivo ao git
git add file1.md

# salve a criação do novo arquivo
git commit -m "edit file1"

# enviar as alterações para o github
git push
```
