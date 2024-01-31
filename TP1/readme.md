# Use a package Criptography para 

1. Criar um comunicação privada assíncrona entre um agente Emitter e um agente Receiver que cubra os seguintes aspectos:
    1. Autenticação do criptograma e dos metadados (associated data). Usar uma cifra simétrica  num modo HMAC  que seja seguro contra ataques aos “nounces” .
    2. Os “nounces” são gerados por um gerador pseudo aleatório (PRG) construído por um função de hash em modo XOF.
    3. O par de chaves $$\mathtt{cipher\_key}, \mathtt{mac\_key}$$ , para cifra e autenticação, é acordado entre agentes usando o protocolo ECDH com autenticação dos agentes usando assinaturas ECDSA.
