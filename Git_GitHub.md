Sistema open-source para controle de versão. Com ele podemos criar todo histórico de alterações no código do nosso projeto e facilmente voltar para qualquer ponto para saber como o código estava naquela data.

- `Git init`
    
    É o primeiro comando usado em um novo projeto que ainda não é um repositório Git. Pode ser usado para converter um repositório Git existente e não versionado. Também pode iniciar um repositório vazio.
    
- `Git add`
    
    Adiciona arquivos traqueados, para que o git visualize-os
    
    - `git add <file-name>` - adiciona um arquivo em específico
    - `git add -A OR git add. OR add*`  - adiciona todos os arquivos
- `Git commit`
    
    Podemos chamar de um checkpoint no processo de desenvolvimento. Comumente utilizado para salvar as alterações, adicionando um texto a ela, e permitindo que outros membros vejam o que foi mudado.
    
    - `git commit -a` - Irá comitar todas as mudanças do diretório que se encontra, uma vez que o comando for rodado, será solicitada uma mensagem de commit.
    - `git commit -am "<commit-message>"` - Adicionará a mensagem sem ser solicitado pelo prompt.
- `Git push`
    
    Para tornar todas as mudanças comitadas disponíveis para o seu time, teremos que mandar ela para a origem remota.
    
    - `git push <remote> <branch-name>` - mandará as mudanças comitadas para o repositório remoto
    
- `Git clone`
    
    Usado para clonar um repositório remoto para sua máquina. Pode-se usar `git remote rm origin` para desassociar o repositório atual do da origem.
    
- `Git branch`
    
    Um dos comandos mais importantes, permite que os times trabalhem no mesmo código base paralelamente. Podemos criar um "branch" separado para cada feature, sem se preocupar com conflitos.
    
    - `git branch <branch-name>` - criar um branch no sistema local;
    - `git push -u <remote> <branch-name>` - fazer um push (enviar ao repositório remoto);
    - `git branch OR git branch --list` - ver todos os branchs
    - `git branch -d <branch-name>` - deletar branch
- `Git checkout`
    
    Trocar para o branch desejado.
    
    - `git checkout <branch-name>`
    - `git checkout -b <branch-name>` - cria e automaticamente troca para o branch selecionado
- `Git pull`
    
    Permite buscar (fetch) todas as alterações feitas no repositório remoto e automaticamente mescla (merge) elas no repositório local.
    
    - `git pull <remote>`
- `Git Diff`
    
    É o comando que se utiliza para visualizar as diferenças entre o meu branch atual e outro branch.
    
    - `git diff` - mostrará qualquer mudança não comitada no seu repositório local;
    - `git diff branch1..branch2` - mostrar as diferenças entre dois branches;
    - `git diff branch1 branch2 ./path/to/file.txt` - mostra a comparação de um arquivo nos diferentes branches.
- `Git Stash`
    
    Armazena temporariamente o seu trabalho, para que você possa mudar de branch, trabalhar nele e voltar para ele mais tarde.
    
    - `git stash save <stash-message>` - isso irá armazenar suas mudanças com a mensagem que inseriu. Só irá armazenar as mudanças feitas nos arquivos traqueados;
    - `git stash save -u` - para armazenar os não traqueados também;
    - `git stash list` - para visualizar todo o código armazenado;
    - `git stash apply` - irá automaticamente restaurar e aplicar o último armazenamento na pilha;
    - `git stash apply stash@{1}` - restaura e aplica um stash específico.
- `Git status`
    
    Mostra informações cruciais do seu repositório local.
    
    - `Git status` - Pode mostrar o seu branch atual, se o seu branch está atualizado, se existe alguma coisa no branch que precise ser comitado, empurrado ou puxado, se temos arquivos staged ou not staged e se temos arquivos criados, modificados ou deletados.
- `Git log`
    
    Histórico de commits do repositório.
    
    - `git log` - mostra todo o histórico de commits. Se for muito grande, mostrará apenas uma pequena parte. Pode-se apertar `space` para rolar ou `:q` para fechar;
    - `git log -n 3` - últimos 3 commits;
    - `git log --oneline` - mostrar commits em uma única linha;
    - `git log --author"<author-username>"` - mostrar o histórico de commit de um determinado autor.
- `Git merge`
    
    Uma vez que você terminou de desenvolver dentro do seu branch e já testou as funcionalidades, você pode fundir (merge) com o branch pai. Pode ser um branch de desenvolvimento ou o master branch. Precisa-se estar no branch específico que você quer fundir (merge) com o seu branch feature.
    
    - `git checkout develop` - seleciona o branch;
    - `git pull` - fazer a atualização do seu repositório local, pois alguém pode ter realizado mudanças antes de você terminar a feature;
    - `git merge feature1` - se não tivermos conflitos, podemos fundir (merge) a feature1 no branch develop.
- `Git fetch`
    
    Realiza o download de objetos e refs de outro repositório sem afetar o seu código local. Primeiramente visualiza-se o que está de diferente e depois realiza-se o merge. O `git pull` faz basicamente primeiro um `git fetch` seguido de um `git merge origin/master`.
    

- pode também fazer o `ls -a` e se tiver uma pasta **".git"** significará que não é uma pasta comum, e sim um repositório local
- `git remote -v` retorna o repositório remoto linkado à pasta
- Criptografia por traz do GIT:
40 caracteres gerados automaticamente sendo possível ver através do comando(já dentro do arquivo):
`openssl sha1`
