# Salvando login github no pc

se toda vez que voce fica fazendo pull pro seu repositorio github e precisa colocar nome e senha
voce pode ta simplesmente salvando seu login no seu pc.

Aqui vai o passo a passo de uma das opcoes

> [!NOTE]
> Como eu gostei da 3 opcao, ainda nao estudei as outras pra poder seguir enfrente, mas quando
> precisar vou da uma olhada

## opcao 1: GitHub CLI
estudar ainda

## opcao 2: Credential helper com token
estudar ainda


## opcao 3: SSH

### Salvamento definitivo SSH

`ssh-keygen -t ed25519 -C "seu@email.com"` | voce vai gerar um par de chaves publica e privada

aperte enter nas perguntas

agora mostre a chave publica
`cat ~/.ssh/id_ed25519.pub` | mostra a chave publica

copie toda a linha pra colar no github.

ja com github aberto click no seu perfil > settings > SSH and GPG Keys
clica em New SSH keys, e cole a chave publica la dentro e agora salve

Teste a conecxao

`ssh -T git@github.com` 

se ele fizer alguma pergunta responda com sim(yes)
ele deve retorna um Hi com seu nome na plataforma, isso que dizer que esta tudo ok

## duvidas

se voce tem duvida sobre algumas coisas vista como porque usei '~/'
 - ~
   - nos terminal o ~ representa a sua pasta pessoal sem ela eu teria que escrever
     home/seu_usuario/.ssh/id_ed25519.pub, entao o ~ e usado apenas pra simplificar
     evitar que eu precise escrever todo o caminho da pasta

 - ed25519
   - é o algoritimo de criptografia e o mais recomendado hoje em dia entrega uma segurança robusta com muito mais
    eficiência (chaves menores e processamento mais rápido)

 - -C
   - E apenas um comentario pra voce identificar pra que serve cada chave tipo, voce tem mais de 2 chaves
    pra uma pro github e outra pro gitlab, pra saber qual e qual voce pode edentificar ela usando
    -C "github" e -C "gitlab" como e um comentario pode colocar qualquer texto dentro

`ed25519` | e a tecnologia que criptografa mais moderna e recomendada

