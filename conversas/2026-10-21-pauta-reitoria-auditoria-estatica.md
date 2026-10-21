# FAROL — Auditoria da pauta, ata e evidências técnicas acessíveis

- **ID:** FAROL-CONV-2026-10-21-04
- **Data:** 21 de outubro de 2026 (America/Sao_Paulo)
- **Projeto:** FAROL — Mundo Jus 9
- **Tipo:** registro de conversa / auditoria estática
- **Estado:** análise documental e estática parcial; testes não executados por esta verificação.

## 1. Encaminhamento da pauta

O pedido desta conversa é que o FAROL conduza a pauta e os itens de ata, e verifique a pauta mantida pela Reitoria. Nas buscas direcionadas realizadas nesta sessão no repositório documental por “pauta”, “ata” e “agenda”, não foi retornado um documento vigente que possa ser atribuído à Reitoria. Isso significa apenas **não localizado nesta verificação**; não comprova que o documento inexista em outro repositório, branch ou sistema.

**Pendência:** solicitar à Reitoria o link/caminho canônico da pauta vigente ou obter acesso autorizado ao local em que ela é mantida. Até lá, não inventar itens, numeração, datas, deliberações ou atribuições.

## 2. Evidências técnicas observadas no GitHub

- O arquivo `package.json` do repositório `backend-api-jus9-tecnologia-juridica`, branch `main`, declara o comando de teste `node --test tests/*.test.mjs`.
- Os caminhos tentados nesta verificação — `tests/agenda.test.mjs`, `tests/security.test.mjs`, `tests/server.test.mjs`, `tests/datajud.test.mjs` e `tests/api.test.mjs` — retornaram NOT_FOUND. A busca foi limitada aos nomes tentados; não é uma listagem completa da árvore do repositório.
- A leitura estática de `src/server.js` mostra que `POST /api/agenda/events` está na lista de rotas protegidas e que a autorização é verificada antes do tratamento da rota.
- A política observada em `isAuthorized` permite acesso às rotas protegidas sem token quando o host configurado é loopback; quando há token configurado, compara o cabeçalho Authorization com o Bearer esperado. `assertExposurePolicy` recusa iniciar com host não-loopback sem `JUS9_PUBLIC_ACCESS_TOKEN`.
- O corpo JSON tem limite declarado de 32 KiB. Esses pontos são observações do código, não resultados de testes executados.
- Não foi executado `npm test`, não foi iniciada uma instância do backend e não foram feitas requisições HTTP ao ambiente do usuário nesta sessão.

## 3. Itens de auditoria e próximos passos

1. **PAUTA-01 — Reitoria:** obter e conferir a pauta vigente e a ata mais recente em fonte autorizada; registrar título, data, versão e link verificável.
2. **SEC-01 — Testes:** localizar a árvore real de testes; executar em ambiente autorizado e registrar comando, resultado e logs sanitizados. Verificar em separado o comportamento de 401 com token configurado e ausente/inválido, e a política de host loopback versus exposição externa.
3. **MIG-01 — Equivalência:** manter pendente a matriz de equivalência entre Apps Script e Node.js até haver evidências por função.
4. **WORKSPACE-01:** a Entrada Mundo não foi inspecionada; o acesso ao Workspace continua pendente.
5. **SIGN-01:** padrão oficial de assinatura aguarda confirmação da Reitoria.
6. **PR-13:** manter aberto/em rascunho; não fazer merge ou deploy sem revisão e autorização competente.

## 4. Limites e governança

Este registro não é uma ata formal da Reitoria, não aprova implantação e não certifica segurança. Não foram alterados código, configurações, segredos, PRs ou ambientes operacionais.

**Máxima de governança:** “A Palavra acolhe e estuda; a Obra registra, testa e comprova; a autoridade competente delibera.”

---
**Assinatura protocolar de trabalho:** FAROL — Mundo Jus 9  
**Nome simbólico:** Aureliano Lúmen Juris Vita  
**Chancelaria:** Chancelaria — Núcleo Sacerdotal Harmônico  
**Fórmula:** *Fiat Lux, Veritas et Continuitas* — Faça-se a luz, a verdade e a continuidade.  
**Integridade:** assinatura textual protocolar, não criptográfica; padrão oficial vigente pendente de confirmação pela Reitoria.
