# Pentaho Data Integration password decrypter
## Descriptografa sehas que foram armazenadas em um job do Kettle/Spoon.

Testado com:
- Pentaho Data Integration CE 7.1.0.0-12 e CE 9.4.0.0.343

Instruções:
1. Abra o arquivo de job/transformation que contenha a senha em um editor de textos

2. Localize a string da senha criptografada, que se parece com: 2be98afc86TESTbd63c99dbdde

3. Execute o Pentaho DI, e após carregar a aplicação, abra o arquivo `Decrypt_Password.ktr` através no menu `File > Open`

4. De um duplo clique na step `Input`

5. Ma janela que se abre, vá na aba `Data`

6. Deixe o campo de email com a informação atual, e altere o campo `encrypted_password` com a string da senha criptografada que adquiriu no passo 2 e clique em **OK**

7. Execute a job, clicando no icone de play descrito como `Run`, e na janela que se abre, basta clicar no botão `Run`

8. Agora clique na step `Output` e painel de resultado da execução que se abriu na parte inferior das steps, vá na aba `Preview Data` e adquira a senha descriptografada na coluna `decrypted_passowd`

## Considerações
Ao rodar a transofrmação, como vai ser alterado a string da senha, será solicitado que salve o arquivo, e nele será gravado a senha a ser decriptada, portanto, ao fim do procedimento faça um wipe neste arquivo para evitar leaks.


* Agradecimento ao Rik https://github.com/Riktastic, só transformei o holandes para ingles. *
