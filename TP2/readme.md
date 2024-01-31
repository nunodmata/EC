# Usa o SageMath em protótipos de esquemas clássicos de chave pública.


1. Construir uma classe Python que implemente um **KEM - ElGamal**. A classe deve
    1. Inicializar cada instância recebendo  o parâmetro de segurança (tamanho em bits da ordem do grupo cíclico) e gere as chaves pública e privada.
    2. Conter funções para encapsulamento e revelação da chave gerada.
    3. Construir,  a partir deste KEM e usando a transformação de **Fujisaki-Okamoto**, um PKE que seja IND-CCA seguro.
    
2. Construir uma classe Python que implemente o  [EdCDSA](https://www.dropbox.com/sh/2v55nnx1veosvhq/AACuh5CNZtuDVcU9FuW7m4eOa?dl=0) a partir do “standard” [FIPS186-5](https://csrc.nist.gov/pubs/fips/186-5/ipd).
    1. A implementação deve conter funções para assinar digitalmente e verificar a assinatura.
    2. A implementação da classe deve usar  uma das “Twisted Edwards Curves” definidas no standard e escolhida  na iniciação da classe: a curva  “edwards25519” ou “edwards448”.
    3. Por aplicação da transformação de Fiat-Shamir construa um protocolo de autenticação de desafio-resposta.
