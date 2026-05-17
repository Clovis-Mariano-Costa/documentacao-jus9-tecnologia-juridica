JUS9_PACOTE_FINAL_SITE_MVP_INVESTIDORES_LIVROS_CARTA_v3_2

Base: versão v3.1.

Atualização v3.2:
- Acrescenta ao portal Livros Gratuitos da Jus 9 Tecnologia Jurídica a página enviar-obra.html.
- Inclui formulário de envio de obra para avaliação com campos de autor, CPF, CEP, e-mail, telefone, dados da obra, PDF e declarações obrigatórias.
- Configura validação matemática de CPF e preenchimento assistido de CEP.
- Direciona o envio para livros@aeonprimevo.com.br, usando abertura de e-mail na versão estática.
- Mantém a publicação como processo de avaliação manual: obra aprovada pode ser publicada; obra recusada pode ter dados e arquivo excluídos após análise.

Atenção:
O formulário é estático e não substitui backend/servidor. Para anexar PDF automaticamente e armazenar arquivos online com segurança, será necessária integração futura com serviço próprio, como Cloudflare Worker + R2 + e-mail transacional.

A Etapa 1 — Organização dos subdomínios permanece reservada para o último passo.
