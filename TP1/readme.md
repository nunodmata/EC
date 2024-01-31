# Use a package Criptography para 

1. Criar um comunicação privada assíncrona entre um agente Emitter e um agente Receiver que cubra os seguintes aspectos:
    1. Autenticação do criptograma e dos metadados (associated data). Usar uma cifra simétrica  num modo HMAC  que seja seguro contra ataques aos “nounces” .
    2. Os “nounces” são gerados por um gerador pseudo aleatório (PRG) construído por um função de hash em modo XOF.
    3. O par de chaves cipher_key, mac_key , para cifra e autenticação, é acordado entre agentes usando o protocolo ECDH com autenticação dos agentes usando assinaturas ECDSA.


2. Use o package Cryptography para criar uma cifra com autenticação de meta-dados a partir de um PRG
    1. Criar um gerador pseudo-aleatório do tipo XOF (“extened output function”) usando o SHAKE256, para gerar uma sequência de palavras de 64 bits. 
        1. O gerador deve poder gerar até um limite de $,2^n,$ palavras ($n$ é  um parâmetro) armazenados em long integers do Python.
        2. A “seed” do gerador funciona como cipher_key e é gerado por um KDF a partir de uma “password” .
        3. A autenticação do criptograma e dos dados associados é feita usando o próprio SHAKE256.
    b. Defina os algoritmos de cifrar e decifrar : para cifrar/decifrar uma mensagem com blocos de 64 bits, os “outputs” do gerador são usados como máscaras XOR dos blocos da mensagem. 
    Essencialmente a cifra básica é uma implementação do  “One Time Pad”.


3. Use o “package” Cryptography para
    1. Implementar uma AEAD com “Tweakable Block Ciphers” conforme está descrito na última secção do texto +Capítulo 1: Primitivas Criptográficas Básicas.  A cifra por blocos primitiva, usada para gerar a “tweakable block cipher”, é o AES-256 ou o ChaCha20.
    2. Use esta cifra para construir um canal privado de informação assíncrona com acordo de chaves feito com “X448 key exchange” e “Ed448 Signing&Verification” para autenticação  dos agentes. Deve incluir uma fase de confirmação da chave acordada.
