# TOKEN-INTER

## O Token deve ser gerado com certificado

Os tokens devem ser gerados com o uso do certificado, que foi obtido na criação da aplicação, caso contrário, o token gerado será inválido e seu sistema não conseguirá consumir os serviços do Inter.

## Certificado
Faça login no site do Banco do Inter.<br>
Clique em conta digital e selecione Gestão de aplicações<br>

- Criar aplicação
- baixe o certificado em seu computador (são 2)
- Clique na seta  esquerda ao lado do nome da aplicação e pegue ClientId e ClientSecret.

## Geraçõ do Token
Essa API gera o token e gerencia o tempo de uso do token, apenas precisa informar o local que esta os certificados e informar 

```php
    $dd = new stdClass;
    $dd->certificate = '../cert/Inter_API_Certificado.crt';
    $dd->certificateKey = '../cert/Inter_API_Chave.key';
    $dd->client_id = '';//seu client_id
    $dd->client_secret = '';//client_secret
    $dd->data = '';

    
    $bankingInter = new InterBanking($dd);
```