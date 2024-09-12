# Conceitos Iniciais

Estamos cercados por tecnologia, carregando no bolso um computador extremamente sofisticado chamado smartphone. Nele, trocamos mensagens instantâneas, assistimos a filmes, acessamos nossas contas bancárias, fazemos compras, utilizamos redes sociais, jogamos e muito mais. Também temos computadores em casa, no trabalho, nos carros, nas indústrias, no espaço, etc.  
Nós simplesmente acreditamos que fazemos tudo isso com segurança, acreditamos que estamos protegidos e que apenas nós teremos acesso às nossas contas, aos nossos dados e às nossas redes. E sabe o que tudo isso tem em comum? **CRIPTOGRAFIA**!

## O que é Criptografia?

Criptografia é a arte e a ciência de proteger mensagens contra um adversário.  
Ela envolve práticas e técnicas que impedem um agente de ameaças (alguém mal-intencionado) de ler suas mensagens, alterá-las ou se passar por você.

Hoje em dia, a criptografia é geralmente a parte mais segura das soluções de segurança e uma das principais ferramentas da segurança da informação. Ela nos ajuda a garantir alguns pilares, como:

- **Confidencialidade**: Garante que apenas as partes autorizadas tenham acesso à informação.
- **Integridade**: Garante que a informação não foi alterada durante o armazenamento ou a transmissão.
- **Autenticidade**: Garante que as partes envolvidas na comunicação são quem elas dizem ser.
- **Não Repúdio**: Garante a irretratabilidade. Uma ação realizada por uma parte não pode ser negada. Por exemplo, impede o autor de negar que criou e assinou um documento.

Há diversas técnicas, cada uma com seus objetivos, pontos fortes e fraquezas. Muitas delas serão exploradas aqui, no **_CryptoJourney_**.

## Terminologia

Em uma comunicação secreta, podem existir três tipos de participantes:

- **Sender** (Remetente): Quem envia a mensagem.
- **Receiver** (Destinatário): Quem recebe a mensagem.
- **Interceptor** (Agente de ameaças): Quem tenta interceptar e ler as mensagens.

Para facilitar o aprendizado, em 1978, no artigo _"A Method for Obtaining Digital Signatures and Public-Key Cryptosystems"_, Ron Rivest, Adi Shamir e Leonard Adleman (**RSA**, pegou?) introduziram **Alice** e **Bob** como representações do remetente e destinatário. Esses personagens foram amplamente utilizados posteriormente em diversos campos da ciência e engenharia.  
Além de **Alice** e **Bob**, o nome dado ao agente de ameaças pode ser **Eve** ou **Mallory**.

- **Eve**: Derivado de _Eavesdropper_, significa alguém que escuta às escondidas. Representa um atacante passivo, que tenta interceptar a comunicação sem alterar seu conteúdo.
- **Mallory**: Derivado de _Malicious_, representa um atacante ativo, que não só tenta ler as mensagens, mas também manipulá-las.

> [!IMPORTANT]
> Um vídeo curto em inglês de Bruce Schneier, criptógrafo e autor, falando sobre Alice e Bob. [Assista aqui](https://www.youtube.com/watch?v=BuUSi_QvFLY).

_Outros personagens foram adicionados posteriormente e serão apresentados quando for oportuno._

<br>

Além dos participantes, temos também outras nomenclaturas:

- **Plaintext** (texto claro): É o texto em formato legível.
- **Ciphertext** (texto cifrado): É o texto em formato ilegível, não podendo ser lido.
- **Encryption** (cifragem ou criptografia): É o processo que transforma o texto claro em texto cifrado.
- **Decryption** (decifragem ou descriptografia): É o processo inverso da criptografia, transformando o texto cifrado em texto claro, legível.

## O que é Criptologia?

Como já vimos anteriormente, a ciência de manter mensagens seguras é chamada de **criptografia** e é praticada por **criptógrafos**. Já a arte e a ciência de quebrar a criptografia é chamada de **criptoanálise** e é praticada por **criptoanalistas**.  
A área que engloba tanto a criptografia quanto a criptoanálise é chamada de **criptologia**.

> [!NOTE]
> Pode parecer que criptoanálise é um assunto para comunidades de inteligência ou então para organizações criminosas, mas ela é o único meio de garantir que um criptosistema seja realmente seguro. Existem muitos pesquisadores sérios dedicados ao tema, devido à relevância do assunto.

<br>

<div align="center">
  <img src="../graphics/cryptology.svg" alt="diagrama áreas da criptologia" style="height: 200px">
  <p style="font-size: 12px">Áreas da Criptologia</p>
</div>

## Como funciona a Criptografia?

Quando queremos transmitir uma mensagem com segurança utilizando criptografia, fazemos da seguinte forma:

1. Pegamos uma mensagem, o _plaintext_.
2. Usamos o plaintext como entrada de uma função de cifragem, _encryption_.
3. A saída do passo anterior gera nosso texto cifrado, _ciphertext_.
4. O ciphertext é então enviado ao destinatário.
5. O destinatário recebe o ciphertext e utiliza a função de decifragem, _decryption_.
6. A saída do passo anterior gera o texto original, _original plaintext_.

<br>

<div align="center">
  <img src="../graphics/encryption-decryption.svg" alt="diagrama básico do processo de criptografia e descriptografia" style="height: 120px">
  <p style="font-size: 12px">Criptografia e Descriptografia</p>
</div>

## Esteganografia, Códigos e Cifras

**Esteganografia** estuda as técnicas para ocultar uma mensagem dentro de outra, sendo uma forma de segurança por obscuridade. É possível esconder mensagens dentro de imagens, músicas, textos, pontos, raspar a cabeça, tatuar a mensagem e esperar o cabelo crescer (existem histórias sobre tal técnica), além de diversos outros métodos.

**Códigos** são criados para substituir palavras ou frases, e só quem tem o livro do código ou decorou alguns conseguirá entender. Por exemplo, podemos substituir "Atacar à meia-noite" por "eagle". O grande problema é que os códigos são limitados ao que foi convencionado, e você não consegue comunicar uma informação diferente da que foi definida. Além do mais, caso o inimigo obtenha acesso ao livro, toda a comunicação estará comprometida.

> [!NOTE]
> Saiba mais sobre o código utilizado pela Marinha dos Estados Unidos na 2ª Guerra Mundial, baseado na língua nativa Navajo. [Navajo Code Talkers](https://www.intelligence.gov/people/barrier-breakers-in-history/453-navajo-code-talkers)

**Cifras** também são conhecidas como algoritmos criptográficos. São funções matemáticas que realizam a criptografia e a descriptografia de uma mensagem.

> [!IMPORTANT]
> Pode parecer contraintuitivo à primeira vista, mas cifras públicas são mais seguras do que cifras proprietárias, pois seguem as padronizações vigentes, são muito mais analisadas e testadas. Cifras restritas são conhecidas por sua baixa segurança e nunca devem ser utilizadas.

## Algoritmos e Chaves

Uma cifra, ou algoritmo criptográfico, é composta por duas partes:

- **Algoritmo**: É a função matemática que realiza a criptografia ou a descriptografia. Ela necessita de uma mensagem e de uma chave.
- **Chave**: Funciona como uma senha para acessar os dados, a chave que "abre o cadeado". Devemos sempre manter a chave segura e de forma privada. Caso um agente de ameaças tenha acesso à chave, o segredo estará comprometido.

Em **criptografia simétrica**, a mesma chave é usada tanto para criptografar quanto para descriptografar.  
Na **criptografia assimétrica**, são usadas duas chaves diferentes, uma para cada operação.

<br>

<div align="center">
  <img src="../graphics/key-symmetric.svg" alt="diagrama de criptografia com chave" style="height: 130px">
  <p style="font-size: 12px">Criptografia Simétrica</p>
</div>
