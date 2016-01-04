# git-code-education

## Instruções para o primeiro push

Um "push" é um comando utilizado para enviar os seus arquivos git para um repositório central, neste exemplo utilizando o Github 
que é um serviço online de versionamento de projetos. 
Primeiro precisamos criar este repositório para em seguida "linká-lo" à sua instalação do git de forma que, quando você der um "push" 
no seu código ele já saberá qual o endereço do seu repositório remoto. Veja o passo-a-passo:

>1. Crie uma conta no Github acessando o endereço https://github.com;

>2. Agora você deve criar um repositório dentro do Github clicando na opção "New repository", adicionando um nome e uma descrição
para o mesmo, e em seguida escolhendo se será um respositório público(gratuito, todos podem ver e contribuir com o seu projeto) ou
privado(pago, para uso interno da sua equipe de desenvolvimento). Você pode também criar um arquivo "README" detalhando o seu 
projeto(opcional). Clique em "Create repository" e o seu repositório estará criado. O endereço do seu repositório segue o 
padrão: https://github.com/nome-de-usuário-da-conta-github/nome-do-repositório.git;

>3. Para que não seja necessário digitar a senha do github toda vez que for executado um "push" no seu projeto e para garantir a 
autenticidade na transações do Github, podemos criar um par de chaves pública/privada com essa finalidade. Acesse o seu terminal e 
digite comando "ssh-keygen", em seguida dê "Enter" 3 vezes e pronto. Procure em seu computador, a pasta oculta ".ssh", com o comando 
"cd ~/.ssh/", nela você encontrará o arquivo "id_rsa" e "id_rsa.pub" que são as chaves privada e pública respectivamente. A primeira 
você não deve compartilhar com ninguém, já a segunda será inserida na sua conta do Github clicando na opção "Settings">menu 
"SSH keys", clique em "Add SSH keys", dê um nome para sua chave, no campo "key" cole o conteúdo do arquivo id_rsa.pub bastando 
apenas abri-lo no bloco de notas, confirme sua senha do Github e temos um respositório configurado!

>4. Para "linkar" a sua instalação local do Git com o seu repositório no Github precisamos executar o comando:
"git remote add origin https://github.com/nome-de-usuário-da-conta-github/nome-do-repositório.git", onde "remote" indica que é um endereço
remoto, "add" adicionar, "origin" é por convenção um nome ou apelido dado ao seu repositório remoto, até para facilitar o comando do
"push", por exemplo, para que não seja necessário digitar o endereço completo do seu repositório a todo momento;

>5. Realizaremos um "commit" de exemplo e aí sim finalmente o "push" enviando os arquivos para o seu repositório:

>* git commit -m "meu primeiro commit"

>* git push origin master

>Será informado na sua tela que um novo "branch" de nome "master" foi criado no seu repositório do Github. Fim!
