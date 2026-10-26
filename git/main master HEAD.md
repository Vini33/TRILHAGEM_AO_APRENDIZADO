# oque e um HEAD, main ou master?


`master` foi substituido por `main` mas voce ainda vai ver alguns repositorio com nomes `master`
mas e a mesma coisa de `main`, serve apenas pra apontar para o commit atual.

quando voce faz um commit e naquele momento que a `main` comecar a existir, e tipo como se fosse uma foto
tirada do seu repositorio, "e se eu fizer outro commit?" a `main` vai se torna aquele novo commit,
imagine que a `main` e um ima de geladeira e voce so tem esse ima, quando voce da um commit(tira uma foto)
voce vai precisar colar aquela foto nova na geladeira mas pra isso voce tem que tirar o ima da foto antiga
com isso a `main`(ima) vai passar a apontar aquela nova foto, "mas e o outro commit se perdeu?" nao, o outro commit
continua la, o registro dele continua, oque mudou foi que voce tirou o ima dele e colou na nova foto mas a foto antiga
continua na geladeira so que sem a main(ima) apontando pra ela

## fluxo

agora vamos intender o fluxo de como as coisas funciona um pouco

o `HEAD` aponta pra uma branch que e uma `main` ou pode ser um galho
e a `main` aponta para o ultimo commit(foto)

mas o `HEAD` e quem diz "olha eu estou nessa branch atual" pode ser ela um galho ou a `main` mesmo
"e se eu criar uma branch(galho) novo?" o `HEAD` vai mudar de branch ele vai apontar para aquela nova
branch, "e o main, oque acontece com ele?" ele continua la, apontando pro ultimo commit feito, criar uma nova branch
nao vai interferir na `main`, "e se eu fizer um commit em uma nova branch(galho)?", bom quando tem um novo commit dentro
de uma branch nova oque rola e que essa mesma branch(galho) e um ima que aponta pra  esse novo commit(foto)
"e como ele sabe qual commit e o anterior?" bom, resumidamente cada commit aponta pro commit anterior
e como uma cadeia em familia, voce e o filho, e voce tem um pai, 
e seu pai tem um pai, os commit tem essa hierarquia de pai e filho mas so o filho conhece o pai, o pai nao conhece o filho


"e se quiser volta na minhas fotos antigas?" bom voce tem 3 maneira de fazer isso, voce pode visitar ela sem mudar
a `main` de lugar, voce voltar nessa foto apagando todas as outras a frente dela ou pode voltar sem apagar as outras fotos

>[!IMPORTANT]
> so pra cargo de conciencia, voce pode criar uma branch(galho) sem entra nela
> `git branch galho ` | criar uma branch(galho), mas voce continuar na branch atual
> `git switch galho`  | aqui sim voce muda de branch, ou seja o `HEAD` vai mudar