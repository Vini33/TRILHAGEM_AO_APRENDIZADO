# Oque e uma branch?

Imagine que voce esta em uma arvore e quer pegar uma manga que esta um pouco mais alta que voce
pra isso voce vai ter que ir subindo de galho em galho ate chegar na manga, agora vamos dizer que esse 
pe de manga e o seu repositorio, entao ele nunca muda o pe de manga nunca muda voce so ficou mudando
de galho em galho ate conseguir pegar a manga, a manga e como se fosse um teste uma funca que voce quer
implementar mas nao sabe se vai fica bom e caso voce se arrependar de pegar a manga(funcao), voce pode simplesmente
volta pro galho anterio que vai esta como era antes de chegar na manga(funcao),


e aqui que voce olha pensa e imagina eu quero implementar uma nova funcao, mas nao quero baguncar oque eu ja tenho feito
<img src="../imagens/branch/pe_de_manga_sem_galhos.png" width="500">

e ai que branch entra, voce pode criar um galho a partir do que voce ja tem feito sem mexer direto na base
basta voce criar uma nova branch

<img src="../imagens/branch/pe_de_manga_com_galho.png" width="500">

<img src="../imagens/branch/pe_de_manga_segundo_galho_manga_colhida.png" width="500">

apos conclui oque pensa voce pode decidir se implementar esse novo galho na main incesta ele na arvore bem dizer
se nao voce pode corta ele e jogar fora, remover a branch nao mexer na arvore principal agora adicionar uma nova branch
vai ser adicionado um novo galho na arvore principal

## codigo

 - Voce gostou e quer implementar essa nova branch na main(arvore principal)
   - `git switch main` | voce sair da branch e vai pra main(arvore principal)
   - `git merge galho-da-manga` | aqui voce uni as duas usando o `merge`

 - voce nao gostou da branch e quer jogar fora
   - `git switch main` | voce sair da branch e vai pra main(arvore principal)
   - `git branch -D galho-da-manga` | aqui voce deleta ela 

 - criando uma nova branch
  - `git switch -c outro-galho` | assim voce criar uma nova branch(galho) e ja entra logo nele
    - `switch` | trocar de branch
    - `-c` | de create (criar), ou seja, cria a branch nova
    - `outro-galho` | o nome que você escolheu para ela

 - vendo as branch que voce tem
   - `git branch` | mostra as lista de branch que voce tem
   - `*` | mostra em qual delas voce ta

 - mudar de branch 
   - `git switch galho-branch` | entra na branch escolhida(galhos)
   - `git switch main`  | vai direto na main(arvore principal)
   

    <img src="../imagens/branch/branches.png">