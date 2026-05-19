# Template — Briefing Técnico para Desenvolvedor Ricoleilões

## Objetivo

Documento estruturado pra Marcello levar ao desenvolvedor/responsável técnico da plataforma ricoleilões.com.br, pra discutir evolução da plataforma rumo a modelo "Parceiro Ricoleilões" (white-label / multi-tenant).

## Contexto da conversa

A plataforma ricoleilões hoje opera 18 leiloeiros do escritório próprio. A próxima evolução estratégica é permitir que **outros leiloeiros oficiais externos** usem a plataforma sob marca compartilhada ou white-label, em troca de comissão + mensalidade.

Esse documento é o briefing técnico pra entender:
1. Estado atual do código
2. Gap pra suportar multi-tenant
3. Custo e prazo de evolução
4. Decisões de arquitetura

---

## Perguntas a fazer ao desenvolvedor

### Estado atual

1. **Stack atual**: linguagem, framework, banco, hospedagem?
2. **Arquitetura**: monolito? Microserviços? Frontend separado de backend?
3. **Multi-usuário**: hoje suportamos quantos leiloeiros simultâneos sem degradação?
4. **Dados isolados**: cada leiloeiro tem dados isolados ou compartilhados na base?
5. **Branding**: cada leiloeiro pode ter logo/cores próprias? Onde isso é configurado?
6. **Domínio**: rodamos em ricoleiloes.com.br apenas, ou suportamos subdomínio por leiloeiro?
7. **Faturamento**: hoje cobramos o quê de quem? Como está estruturado?
8. **Compliance**: temos certificado digital, assinatura eletrônica, LGPD compliance?

### Gap pra multi-tenant white-label

1. **Quantas horas/dias estima** pra implementar:
   - Modelo multi-tenant (cada leiloeiro = uma "conta master")
   - Branding configurável (logo, cores, domínio personalizado)
   - Permissionamento granular (admin master, leiloeiro, atendente)
   - Faturamento separado por tenant (setup, mensalidade, comissão)
   - Painel de gestão (Marcello vê todos os tenants, cada tenant vê o próprio)
   - Suporte multi-domínio (ex: leiloeiro-x.ricoleiloes.com.br ou domínio próprio)

2. **Estimativa de custo** total (desenvolvimento + infraestrutura)

3. **Existem partes do código** que precisariam ser reescritas do zero? Quais?

4. **Riscos técnicos** identificados na evolução?

### Decisões de arquitetura a tomar

1. **Multi-tenant**: shared database (mesma base, separação por tenant_id) ou separated database (uma base por tenant)?
   - Shared = mais barato, mais rápido, menos isolamento de segurança
   - Separated = mais caro, mais lento, isolamento total

2. **Branding**: configurável via painel (não-técnico ajusta) ou via deploy (cada tenant é um deploy customizado)?

3. **Hospedagem**: vamos manter onde está (AWS/Azure/GCP) ou migrar? Custo escalona linear com tenants?

4. **Backup e disaster recovery**: como ficaria? Backup por tenant ou global?

5. **Monitoramento**: precisa instrumentação por tenant pra cobrança variável (% sobre arrematação)?

### Modelo comercial pretendido

Pra conversa com desenvolvedor entender o que o software precisa suportar:

```
Tier Basic (R$ 1.500/mês + 0,5% transacional)
- 1 leiloeiro vinculado
- Plataforma sob domínio personalizado
- Branding básico (logo + cores)
- Até 50 leilões/mês

Tier Pro (R$ 2.500/mês + 0,5% transacional)
- Até 3 leiloeiros vinculados
- Domínio próprio
- Branding total
- Leilões ilimitados
- Suporte premium

Setup único: R$ 5.000 – R$ 15.000 (varia conforme customização)
```

## Output esperado da conversa

Ao final, Marcello deve sair com:

- [ ] Estimativa de custo (R$ ___) pra implementar modelo white-label completo
- [ ] Estimativa de prazo (semanas ___) pra ter MVP comercial
- [ ] Lista de riscos técnicos identificados
- [ ] Recomendação técnica do desenvolvedor (build vs comprar SaaS pronto vs hybrid)
- [ ] Próximo passo concreto (orçamento formal, MVP, prova de conceito)

## Decisão pós-conversa

| Cenário | Resposta do desenvolvedor | Próximo movimento |
|---|---|---|
| Custo < R$ 80k e prazo < 60 dias | **GO** — aprovar orçamento e prosseguir | Frente 3 entra no mês 2 do plano |
| Custo R$ 80–200k e prazo 60–120 dias | **AVALIAR** — analisar ROI projetado | Frente 3 entra no mês 4–6 |
| Custo > R$ 200k ou prazo > 4 meses | **REVER ESTRATÉGIA** — pensar em SaaS terceiro? | Adiar Frente 3 pro ano 2 |
| Riscos técnicos altos | **PROVA DE CONCEITO PRIMEIRO** | Investir R$ 10–20k em PoC antes |

## Quando ter essa conversa

Conforme plano: **primeira semana do plano de 30 dias**. Não adiar — destrava Frente 3 inteira.
