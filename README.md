# Site estático · Profissional de estética em Ribeirão Preto

Este site foi feito para subir na Hostinger arrastando a pasta inteira. Ele também abre com duplo clique no arquivo `index.html`.

## Como abrir

1. Abra a pasta `clinica-estetica-ribeirao-preto`.
2. Dê duplo clique em `index.html`.
3. Para publicar, envie todos os arquivos e pastas para a Hostinger: `index.html`, `.htaccess`, `css`, `js`, `lib` e `assets`.

## O que editar no Bloco de Notas

Abra `lib/manifest.js`. Quase tudo que a cliente precisa trocar está ali:

- `brand.name`: nome da profissional ou da clínica.
- `brand.profession`, `brand.register`, `brand.experience`: categoria profissional, conselho, registro, anos de experiência e formações.
- `contact.whatsappNumber`: número em formato internacional, sem espaços. Exemplo: `5516999999999`.
- `contact.displayPhone`: número como aparece no site.
- `contact.instagramHandle` e `contact.instagramUrl`: Instagram.
- `contact.address`, `contact.mapQuery`, `contact.hours`: endereço, busca do mapa e horário.
- `services`: nome, problema, solução e mensagem de WhatsApp de cada serviço.
- `reviews`: cole avaliações reais do Google. Depois de substituir, troque `placeholder: true` para `placeholder: false`.
- `gallery`: coloque as fotos em `assets/img/`, informe o caminho no campo `image` e marque `consentimento: true` somente quando houver autorização do paciente.

## Importante sobre WhatsApp

O número também aparece no `index.html` como segurança para o site funcionar mesmo se o JavaScript não carregar. Depois de trocar o WhatsApp no `manifest.js`, procure por `5516999999999` no `index.html` e substitua pelo número correto.

## Trocar fotos

Coloque as novas imagens em `assets/img/`. Prefira arquivos `.webp`. Se usar `.jpg` ou `.png`, escreva o nome completo no `manifest.js`.

As imagens atuais são placeholders locais. Não publique resultados de queloide, lóbuloplastia ou outro procedimento de saúde sem confirmar as regras do conselho profissional e sem consentimento formal do paciente.

## Antes/depois e conformidade

As regras exatas de antes/depois dependem do conselho da profissional:

- Médicos: verificar CFM, incluindo Resolução 2.336/2023.
- Biomédicos, enfermeiros, esteticistas e outras categorias: verificar as normas do conselho correspondente.

Antes de publicar fotos de procedimentos de saúde, confirme as normas do conselho e tenha termo de consentimento de cada paciente. Não use linguagem como “resultado garantido”, “cura”, “sem dor”, “sem riscos”, “efeito imediato” ou “satisfação garantida”. Todo CTA deve convidar para avaliação.

## Se algo não atualizar

1. Aperte `Ctrl + F5` no navegador.
2. Se ainda assim o arquivo antigo aparecer, troque o número de versão no `index.html`. Procure `?v=20260617` e altere para outra data, por exemplo `?v=20260618`.

## Bibliotecas locais

O site carrega `lib/gsap.min.js` e `lib/ScrollTrigger.min.js` como arquivos locais. Nesta entrega eles estão como fallback offline, porque o download externo foi bloqueado pelo ambiente. Se quiser usar a biblioteca oficial, substitua esses dois arquivos pelos builds oficiais do GSAP e ScrollTrigger mantendo os mesmos nomes.
