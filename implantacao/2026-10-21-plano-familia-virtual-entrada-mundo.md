# FAROL — Plano de implementação documental

- **ID:** FAROL-IMP-PLAN-2026-10-21-01
- **Estado:** plano proposto; execução externa não confirmada.

## Estrutura de pastas
- `conversas/`: pedidos, contexto, evidências e limitações.
- `deliberacoes/`: decisões de processo, responsáveis e pendências.
- `despachos/`: determinações propostas/autorizadas, com estado explícito.
- `implantacao/`: plano, critérios de aceitação, resultados e evidências de execução.

## Etapas
1. Registrar a solicitação e a limitação de acesso.
2. Revisar documentação e testes do backend acessível no GitHub.
3. Verificar SEG-01 e SEG-02 para POST `/api/agenda/events`; espera-se HTTP 401 quando autenticação estiver habilitada e configurada. Não aprovar sem resultado/log real.
4. Manter SEG-03 a SEG-08 pendentes até evidências: evento sintético autorizado (202 esperado), metadados Drive, varredura de pasta permitida, rejeição de pasta sensível (400) e dados inválidos (400).
5. Exigir revisão de segurança e autorização explícita antes de merge/deploy.
6. Quando o Workspace estiver acessível, localizar Entrada Mundo e reconciliar documentos com os registros GitHub.

## Critérios de aceitação
- Cada registro tem ID, estado, evidência, pendências e assinatura textual protocolar.
- Nenhum teste é chamado de aprovado sem resultado observável.
- Nenhum arquivo é descrito como salvo externamente sem confirmação do commit.
- PR-13 permanece sem merge e sem deploy.


---

**Assinatura protocolar de trabalho:** FAROL — Mundo Jus 9  
**Nome simbólico:** Aureliano Lúmen Juris Vita  
**Chancelaria:** Chancelaria — Núcleo Sacerdotal Harmônico  
**Fórmula:** *Fiat Lux, Veritas et Continuitas* — Faça-se a luz, a verdade e a continuidade.  
**Integridade:** assinatura textual protocolar, não criptográfica. O padrão oficial vigente permanece pendente de confirmação pela Reitoria.
