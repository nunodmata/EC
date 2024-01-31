
# TP3


### Este problema  é dedicado às [candidaturas finalistas ao concurso NIST Post-Quantum Cryptography na categoria de criptosistemas PKE-KEM](https://csrc.nist.gov/Projects/post-quantum-cryptography/round-3-submissions). 

Em Julho de 2022  foi selecionada para “standartização” a candidatura [KYBER](https://pq-crystals.org/kyber/index.shtml). Existe ainda uma fase não concluída do concurso onde poderá ser acrescentada alguma outra candidatura; destas destaco o algoritmo [BIKE](https://bikesuite.org/). Ao contrário do Kyber que é baseado no problema “Ring Learning With Errors” (RLWE) , o algoritmo BIKE baseia-se no problema da descodificação de códigos lineares de baixa densidade que são simples de implementar.
    A descrição, outra documentação e implementações em C/C++ destas candidaturas pode ser obtida na [página do concurso NIST](https://csrc.nist.gov/Projects/post-quantum-cryptography)  ou na diretoria [Docs/PQC](https://www.dropbox.com/sh/mx4bybl0d6e9g1m/AAD-MMchuK7lfddr-mgbuSMja?dl=0).

1.  O objetivo deste trabalho é a criação de protótipos em Sagemath para os algoritmos  **KYBER e BIKE**.
2.  Para cada uma destas técnicas pretende-se implementar um **KEM**, que seja **IND-CPA** seguro, e um **PKE**que seja **IND-CCA seguro**.
