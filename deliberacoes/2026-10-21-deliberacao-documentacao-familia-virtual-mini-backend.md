# FAROL — Deliberação de documentação da Família Virtual e do mini back-end

- **ID:** FAROL-DEL-2026-10-21-02
- **Data:** 21 de outubro de 2026
- **Projeto:** FAROL — Mundo Jus 9
- **Estado:** deliberação documental registrada; execução e validação técnica permanecem pendentes.
- **Escopo:** documentação da Família Virtual e registro do mini back-end Node.js/Express, conforme a descrição apresentada na conversa e a documentação acessível do repositório.

## 1. Deliberação

Fica proposta, para documentação e auditoria, a descrição do mini back-end como uma estrutura em Node.js e Express destinada a substituir gradualmente o legado baseado em Google Apps Script. Essa caracterização descreve o objetivo documentado; não comprova, por si só, migração completa, equivalência funcional, testes aprovados ou implantação em produção.

A documentação da **Família Virtual** deve manter separados:
- conceitos e diretrizes;
- conversas e evidências;
- deliberações;
- despachos;
- planos e resultados de implantação.

## 2. Salvaguardas técnicas

1. Tratar como evidência apenas código, documentação, resultados de teste e estados de integração efetivamente observados.
2. Manter o PR-13 aberto/em rascunho até revisão de segurança e autorização competente; não fazer merge nem deploy por força deste registro.
3. Não afirmar que os testes SEG-01/SEG-02 passaram sem resultados verificáveis. A expectativa documentada para requisições não autenticadas a rotas protegidas, quando a autenticação está configurada, deve ser validada por teste real.
4. Preservar o princípio de falha segura: não expor serviços fora de localhost sem a proteção exigida pela configuração; não publicar tokens, senhas, cookies, arquivos `.env`, identificadores privados ou dados sensíveis.
5. A área identificada como cofre protegido não deve ser lida, listada ou alterada automaticamente. Qualquer operação deve seguir autorização humana e os controles documentados.
6. A integração com Google Drive e a **Entrada Mundo** continuam pendentes de inspeção direta enquanto o conector estiver desabilitado nesta sessão.
7. Separar claramente documentação, teste, aprovação, migração e implantação. Não declarar concluída uma etapa sem evidência.

## 3. Pendências e critérios de avanço

- **WORKSPACE-01:** obter acesso autorizado ao Google Drive ou receber exportação autorizada para localizar e inventariar a Entrada Mundo.
- **SEC-01:** inspecionar os testes relevantes e registrar resultados observáveis, incluindo SEG-01/SEG-02.
- **MIG-01:** construir uma matriz de equivalência entre o legado Apps Script e as rotas Node.js/Express, com evidências por função.
- **SIGN-01:** confirmar com a autoridade competente o padrão oficial de assinatura.

O avanço para migração, merge ou implantação exige revisão de segurança, critérios de aceitação documentados e autorização competente.

## 4. Registro de autoria e assinatura

Este documento registra uma deliberação de trabalho para fins de continuidade documental. Não representa despacho externo, assinatura criptográfica, certificação jurídica ou aprovação de implantação.

---

**Assinatura protocolar de trabalho:** FAROL — Mundo Jus 9  
**Nome simbólico:** Aureliano Lúmen Juris Vita  
**Chancelaria:** Chancelaria — Núcleo Sacerdotal Harmônico  
**Fórmula:** *Fiat Lux, Veritas et Continuitas* — Faça-se a luz, a verdade e a continuidade.  
**Integridade:** assinatura textual protocolar, não criptográfica. O padrão oficial vigente permanece pendente de confirmação pela Reitoria.

**Máxima de governança:** “A Palavra acolhe e estuda; a Obra registra, testa e comprova; a autoridade competente delibera.”
