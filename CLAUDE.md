# hila-trips

Este repositório publica as propostas de viagem da Hila Travel. Cada proposta fica numa pasta própria com um arquivo `index.html`. O Netlify publica automaticamente tudo que entra na branch `main` em `https://trip.hilatravel.com/<nome-da-pasta>`.

## Como publicar uma nova proposta

A Vicky vai mandar três coisas: o arquivo HTML, o nome da pasta e o título. Com isso:

1. Salve o HTML como `<nome-da-pasta>/index.html`. Se a pasta já existir, confirme antes de sobrescrever.
2. No `<head>` estático do arquivo, logo depois de `<meta charset="utf-8">`, troque o `<title>Bundled Page</title>` por `<title><TÍTULO></title>` e adicione em seguida:

   ```html
   <meta name="robots" content="noindex, nofollow">
   <meta property="og:title" content="<TÍTULO>">
   <meta property="og:description" content="Roteiro de viagem personalizado, criado por Hila Travel">
   <meta property="og:type" content="website">
   ```

   Altere só esse trecho do head; o resto do arquivo (inclusive o conteúdo empacotado) fica intacto.
3. Faça o commit direto na `main` e o push.
4. Confirme o link final: `https://trip.hilatravel.com/<nome-da-pasta>`.

Padrão de título: `<Nome do cliente> · <Tema da viagem> | Hila Travel`, por exemplo `Beatriz · Catamarãs em Paros | Hila Travel`.
