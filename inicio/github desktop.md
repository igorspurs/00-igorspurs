
## INTRODUÇÃO

Com o Github Desktop, acredito que posso gerenciar os arquivos de forma hierarquizada mais facilmente, além de ter eles upados na nuvem, além da vantagem do fato de que posso criar backups, além de continuar dentro do ambiente do github...

## CONTROLE

Instalei:
1. Github
2. Git

## VANTAGENS

De acordo com o chatpt, são vantagens do Github Desktop:

1.Gerenciamento Local
- Permite clonar repositórios para o seu computador e trabalhar nos arquivos localmente, o que é mais rápido e eficiente para projetos maiores.
- Não depende de conexão constante com a internet.

2. Interface Amigável para Git
- Simplifica tarefas como commit, push, pull e merge com botões e interface gráfica.
- Ideal para quem não tem experiência com linha de comando.

3. Trabalho com Vários Arquivos
Possibilita edição, movimentação e exclusão em massa de arquivos diretamente no sistema local.
Com integrações locais (ex.: VS Code), você pode editar código sem usar a interface web.

Vantagens do Github no navegador

1. Acesso de Qualquer Lugar
- Basta um navegador para acessar e gerenciar repositórios sem a necessidade de instalar ferramentas.

2. Criação e Edição Rápida de Arquivos
- Permite criar, editar e excluir arquivos diretamente na interface, sem necessidade de sincronização.

3. Recursos Administrativos
- Configuração de permissões, integração com ações de CI/CD, e gerenciamento de repositórios privados.

4. Simplicidade
- Ideal para tarefas rápidas, como ajustes em arquivos pequenos ou configurações do repositório.


### Quando usar cada um?

    GitHub Desktop:
        Para projetos maiores que demandam alterações frequentes.
        Quando é necessário trabalhar offline ou realizar mudanças em massa.
        Se você preferir uma interface gráfica para evitar o terminal.

    GitHub Web:
        Para ajustes rápidos ou gerenciamento de configurações do repositório.
        Quando você não tem o repositório localmente ou não quer instalar softwares.
        Melhor para revisão de Pull Requests e colaboração.


## Como fiz? 

No terminal 


1. Add repositorio:

sudo wget -qO - https://packagecloud.io/shiftkey/desktop/gpgkey | sudo apt-key add -

sudo sh -c 'echo "deb https://packagecloud.io/shiftkey/desktop/any/ any main" > /etc/apt/sources.list.d/github-desktop.list'

alternativa, baixar a chave manualmente: get -qO - https://packagecloud.io/shiftkey/desktop/gpgkey | sudo tee /etc/apt/trusted.gpg.d/shiftkey-desktop.gpg

add o repositorio: echo "deb https://packagecloud.io/shiftkey/desktop/any/ any main" | sudo tee /etc/apt/sources.list.d/github-desktop.list


2. sudo apt update

3. sudo apt install github-desktop

4. Fazer Login no GitHub

Ao abrir o programa pela primeira vez:

Clique em Sign in to GitHub.com.

Entre com suas credenciais do GitHub.

Comece a usar o programa para gerenciar seus repositórios.


## Erro do Git não saber quem voce é

author identity unknown - não compila as alterações

para corrigir, no terminal

1. config email

git config --global user.email "seu-email@example.com"

2. config nome
   
git config --global user.name "Seu Nome"

3. Testar a configuração e ver se deu certo

git config --list

Deve aparecer algo assim:

user.name=Seu Nome

user.email=seu-email@example.com


## Terminal: alguns comandos uteis

1. Configuração do Git    Definir nome e email (autoria dos commits):

git config --global user.name "Seu Nome"

git config --global user.email "seu-email@example.com"

Configurações globais usadas em todos os seus repositórios.

Verificar configurações atuais:

git config --list

Mostra todas as configurações definidas no Git.


2. Inicializar um Repositório

Criar um repositório Git em uma pasta existente:

git init

Inicializa o controle de versão na pasta atual.

3. Adicionar e Confirmar Alterações

Adicionar arquivos para o próximo commit:

git add <arquivo>

Adiciona um arquivo específico. Para adicionar todos os arquivos alterados:

git add .

Confirmar alterações (commit):

git commit -m "Descrição das alterações"

Cria um commit com uma mensagem descritiva.

4. Enviar e Receber Alterações

Enviar alterações para o repositório remoto (push):

git push

Baixar alterações do repositório remoto (pull):

git pull

Atualiza o repositório local com as mudanças remotas.

Clonar um repositório existente:

git clone <URL>

Copia um repositório remoto para o seu computador.

5. Trabalhar com Branches

Criar uma nova branch:

git branch <nome-da-branch>

Alternar para uma branch específica:

git checkout <nome-da-branch>

Criar e alternar para uma branch ao mesmo tempo:

git checkout -b <nome-da-branch>

Exibir todas as branches:

git branch


6. Histórico de Commits

Visualizar o histórico de commits:

git log

Mostra detalhes dos commits anteriores. Para um formato mais compacto:

git log --oneline


7. Status e Comparação

Verificar o status do repositório:

git status

Mostra arquivos alterados, adicionados ou prontos para commit.

Verificar as diferenças entre as mudanças locais e o último commit:

git diff


8. Reverter ou Corrigir Alterações

Desfazer alterações não confirmadas em um arquivo:

git checkout -- <arquivo>

Remover um arquivo do estágio (desfazer git add):

git reset <arquivo>

Desfazer o último commit (sem perder as alterações)

git reset --soft HEAD~1

9. Resolver Conflitos de Merge

Após resolver conflitos, adicionar os arquivos resolvidos:

git add <arquivo>

Finalizar o merge após resolver os conflitos:

git commit

10. Trabalhar com Repositórios Remotos

Adicionar um repositório remoto:

git remote add origin <URL>

Verificar os repositórios remotos configurados:

git remote -v

Remover um repositório remoto:

git remote remove <nome>











