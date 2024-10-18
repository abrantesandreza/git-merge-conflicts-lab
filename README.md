# git-merge-conflicts-lab

Este repositório foi criado como parte de um laboratório prático de Git para treinar a resolução de conflitos de merge. Os estudantes devem modificar o mesmo arquivo em branches diferentes e realizar merges, enfrentando e resolvendo conflitos manuais. O objetivo é aprimorar o entendimento de fluxos de trabalho colaborativos no Git, incluindo o uso de branches e a prática de resolução de conflitos.

## Instruções
1. Criar uma branch com seu nome (por exemplo, joao-modificacoes).
2. Modificar pelo menos dois dos seguintes itens na sua branch:
     - Adicionar seu nome
     - Adicionar seu cargo na equipe
3. Após fazer as modificações, realizar um commit e tentar fazer o merge com a branch main. Isso deverá gerar conflitos, que precisam ser resolvidos manualmente.

## Passo a Passo: Fazendo Merge com a branch main

1. Atualize o repositório local com as mudanças da branch main
 - Antes de começar o merge, é importante que você tenha a versão mais recente da branch main no seu repositório local.

       git checkout main
       git pull origin main

 - Isso garante que você está trabalhando com a versão mais atualizada da branch main.

2. Vá para a sua branch de trabalho

 - Depois de atualizar a branch main, troque para a sua branch de trabalho, onde você fez as modificações.

       git checkout sua-branch

3. Atualize sua branch de trabalho com as mudanças da branch main

- Agora, você precisa incorporar as últimas mudanças da branch main na sua branch de trabalho para poder fazer o merge corretamente.

      git merge main

- Aqui é onde o Git tentará combinar as mudanças. Se não houver conflitos, as mudanças serão mescladas diretamente. No entanto, como vários alunos estarão modificando as mesmas linhas, conflitos provavelmente ocorrerão.

4. Resolva os conflitos de merge

- Se houver conflitos, o Git mostrará uma mensagem indicando quais arquivos precisam de atenção. Abra os arquivos indicados no seu editor de texto (por exemplo, VSCode) para resolver os conflitos.

- O Git marcará os conflitos assim:

      <<<<<<< HEAD
      (Este é o conteúdo da branch `sua-branch`)
      =======
      (Este é o conteúdo da branch `main`)
      >>>>>>> main

- Você deve escolher qual parte manter (ou combinar as duas, dependendo da situação) e remover os marcadores <<<<<<<, =======, e >>>>>>>.

- Exemplo:

      <<<<<<< HEAD
      João Silva - Desenvolvedor Frontend
      =======
      Joana Silva - Desenvolvedora Frontend
      >>>>>>> main

- Pode resolver o conflito assim:

      Joana Silva - Desenvolvedora Frontend

5. Adicione os arquivos corrigidos

  - Depois de resolver os conflitos, adicione os arquivos corrigidos para preparar o commit do merge.

        git add .

6. Finalize o merge com um commit

  - Agora que os conflitos foram resolvidos, finalize o merge com um commit.

        git commit

  - O Git abrirá um editor de texto para que você possa adicionar uma mensagem de commit descrevendo que você resolveu os conflitos.

7. Envie sua branch para o repositório remoto

  - Finalmente, faça o push da sua branch para o GitHub.

        git push origin sua-branch

  - Substitua sua-branch pelo nome da sua branch.

8. Abra um Pull Request

No GitHub, vá até a página do repositório e abra um Pull Request para que sua branch seja revisada e mesclada com a branch main.




















