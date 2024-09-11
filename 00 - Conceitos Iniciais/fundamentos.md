# Conceitos Iniciais

Estamos cercados por tecnologia, carregando no bolso um computador extremamente sofisticado chamado smartphone. Nele, trocamos mensagens instantâneas, assistimos a filmes, acessamos nossas contas bancárias, fazemos compras, utilizamos redes sociais, jogamos e muito mais. Também temos computadores em casa, no trabalho, nos carros, nas indústrias, no espaço, etc.  
Nós simplesmente acreditamos que fazemos tudo isso com segurança, acreditamos que estamos protegidos e que apenas nós teremos acesso às nossas contas, aos nossos dados e às nossas redes. E sabe o que tudo isso tem em comum? **CRIPTOGRAFIA**!

## Mas o que é Criptografia?

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

_Outros personagens foram adicionados posteriormente e serão apresentados quando for oportuno._

Além dos participantes, temos também outras nomenclaturas:

- **Plaintext** (texto claro): É o texto em formato legível.
- **Ciphertext** (texto cifrado): É o texto em formato ilegível, não podendo ser lido.
- **Encryption** (cifragem ou criptografia): É o processo que transforma o texto claro em texto cifrado.
- **Decryption** (decifragem ou descriptografia): É o processo inverso da criptografia, transformando o texto cifrado em texto claro, legível.

## Como funciona a Criptografia?

Quando queremos transmitir uma mensagem com segurança utilizando criptografia, fazemos da seguinte forma:

1. Pegamos uma mensagem, o _plaintext_.
2. Usamos o plaintext como entrada de uma função de cifragem, _encryption_.
3. A saída do passo anterior gera nosso texto cifrado, _ciphertext_.
4. O ciphertext é então enviado ao destinatário.
5. O destinatário recebe o ciphertext e utiliza a função de decifragem, _decryption_.
6. A saída do passo anterior gera o texto original, _original plaintext_.

<br>

<div style="text-align: center">
<img src="../graphics/encryption-decryption.svg" alt="diagrama básico do processo de criptografia e descriptografia" style="max-width: 80%; height: 100px">
<p style="font-size: 12px;">Criptografia e Descriptografia</p>
</div>
