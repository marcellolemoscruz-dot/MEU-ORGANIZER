# 03 — Frente SaaS Ricoleilões (Programa Parceiro)

> **Prioridade**: 🥈 Segunda em peso de esforço estratégico.
>
> **Estado**: depende de evolução técnica da plataforma. Validar custo/prazo com desenvolvedor (templates/briefing-tecnico-ricoleiloes.md).

---

## Tese desta frente

A plataforma ricoleilões.com.br já está em produção operando 18 leiloeiros. O próximo passo é transformá-la em **ativo licenciável** pra outros leiloeiros oficiais — convertendo software em receita recorrente, não só comissão por operação.

## Modelo proposto — "Programa Parceiro Ricoleilões"

Em vez de SaaS frio (qualquer leiloeiro contrata), criar programa **com filtro**:

> Leiloeiros oficiais menores ou de outras regiões (interior SP, outros estados) usam a plataforma sob marca compartilhada ou white-label, em troca de:
> - Setup único (R$ 5–15k)
> - Mensalidade (R$ 1.500 – R$ 3.000/mês)
> - **Comissão sobre arrematação processada** (0,5% – 1%) — ou repasse de 15–25% da comissão do leiloeiro parceiro

## Por que esse modelo é melhor que SaaS frio

- **Filtro**: você escolhe quem entra (não vira concorrente de si mesmo)
- **Rede**: cada parceiro pode te indicar caso grande que ele não consegue operar
- **Multiplicador**: mais transações = mais reputação + mais receita
- **Comunidade**: vira referência regional/nacional do nicho

## O mercado-alvo

**Mais de 2.000 leiloeiros oficiais no Brasil**. Maioria opera solo ou em pequenas equipes. Maioria usa Sodimac/AGS/Superbid pagando 15-40% da receita.

Eles adorariam alternativa **com menos taxa, marca própria, suporte regional**.

### Sub-segmentos prioritários

1. **Leiloeiros do interior SP** (Sorocaba, Ribeirão, Bauru, Marília, SJ Rio Preto, Presidente Prudente)
2. **Leiloeiros que querem mudar de plataforma** (insatisfeitos com Sodimac/Superbid)
3. **Leiloeiros novos** (recém-credenciados sem infraestrutura)
4. **Prefeituras pequenas** que querem plataforma própria sem desenvolver

## Investimento técnico necessário

Validar com desenvolvedor (template em `.claude/skills/gestor-pessoal/templates/briefing-tecnico-ricoleiloes.md`):

| Item técnico | Estimativa |
|---|---|
| Multi-tenant (cada parceiro tem sua conta isolada) | R$ 30k – R$ 80k |
| Branding configurável (logo, cores, domínio) | R$ 20k – R$ 50k |
| Faturamento automatizado (setup + mensal + transacional) | R$ 15k – R$ 30k |
| Compliance LGPD multi-tenant | R$ 10k – R$ 20k |
| Painel de gestão (admin Marcello vê todos) | R$ 15k – R$ 30k |
| **Total estimado** | **R$ 90k – R$ 210k** |

## Plano de execução

### Trimestre 1 (mês 1–3)

- [ ] Reunião com desenvolvedor — definir custo/prazo de evolução (semana 1)
- [ ] Decidir: build in-house, dev shop externo ou hybrid
- [ ] Iniciar desenvolvimento das funcionalidades multi-tenant
- [ ] Em paralelo: identificar 5–10 leiloeiros candidatos a beta

### Trimestre 2 (mês 4–6)

- [ ] MVP white-label pronto
- [ ] Beta com 3–5 leiloeiros parceiros (gratuito ou simbólico, em troca de feedback + case)
- [ ] Documentar onboarding (Como adicionar parceiro? Quanto tempo leva?)

### Trimestre 3 (mês 7–9)

- [ ] Abre comercial
- [ ] Setup landing page de "Parceiros Ricoleilões"
- [ ] Comunicação ativa: LinkedIn, Sindleiloeiro SP, eventos de leiloeiro
- [ ] Meta: 5–10 parceiros pagantes

### Trimestre 4 (mês 10–12)

- [ ] Escala pra 10–20 parceiros
- [ ] Receita recorrente estabilizada
- [ ] Avaliar evolução do modelo (precisa funcionário dedicado? Outras features?)

## Receita projetada

### Mês 12 (rampa final do ano 1)

- 10–15 parceiros pagantes
- Setup acumulado no ano: R$ 50–150k (única vez)
- Mensalidade no mês: R$ 15–45k
- Comissão transacional no mês: R$ 10–30k
- **Receita mensal mês 12**: R$ 30–80k

### Regime (ano 2)

- 30–80 parceiros
- Receita mensal recorrente: **R$ 80–250k/mês**
- Custo marginal por novo parceiro: ~zero
- **Margem líquida**: 70–85%

## Por que essa frente é estratégica além da receita

1. **Múltiplo de venda do negócio sobe 3–5x**: empresa com SaaS vale mais que empresa só de serviços
2. **Rede nacional**: vira hub de leiloeiros parceiros, fluxo de informação cruzado
3. **Receita previsível**: SaaS suaviza ciclos de licitação e ciclos políticos
4. **Lock-in**: parceiros não trocam de plataforma fácil (treinamento, base de dados, processos)

## Decisões críticas

### Build vs Buy vs Hybrid

- **Build (desenvolver multi-tenant in-house)**: maior controle, maior custo
- **Buy (comprar SaaS pronto white-label)**: menor controle, menor custo, dependência
- **Hybrid (manter core, comprar módulos)**: equilibrado, recomendado

Decidir com desenvolvedor.

### Quanto cobrar

Pricing inicial sugerido:
```
Plano Solo (R$ 1.500/mês + 0,5% transacional)
- 1 leiloeiro
- Domínio personalizado
- Branding básico (logo + cores)
- Até 50 leilões/mês

Plano Equipe (R$ 2.500/mês + 0,5% transacional)
- Até 3 leiloeiros
- Domínio próprio
- Branding total
- Leilões ilimitados
- Suporte prioritário
```

Setup único: R$ 5.000 – R$ 15.000 conforme customização.

### Posicionamento da marca

"Ricoleilões Parceiros" ou white-label total (leiloeiro vê só sua marca)?

Recomendação: oferecer ambos. Cobrar mais pelo white-label total. Manter "Ricoleilões Parceiros" como tier "Pro" com mais visibilidade.

## Métricas-chave (mês a mês)

| Métrica | M3 | M6 | M9 | M12 |
|---|---|---|---|---|
| MVP técnico % concluído | 30% | 100% | — | — |
| Parceiros em beta | 1 | 3–5 | — | — |
| Parceiros pagantes | 0 | 0 | 5–10 | 10–20 |
| MRR (receita recorrente mensal) | R$ 0 | R$ 0 | R$ 10–30k | R$ 30–80k |
| Setup acumulado | R$ 0 | R$ 0 | R$ 30–80k | R$ 50–150k |

## Risco e mitigação

| Risco | Mitigação |
|---|---|
| Custo técnico estoura | Hybrid (módulos prontos) ou MVP minimalista |
| Adesão lenta | Beta gratuito ampliado, indicação Sindleiloeiro |
| Concorrência (Sodimac, AGS) | Filtro qualitativo + relacionamento local |
| Sobrecarga operacional do Marcello | Funcionário dedicado a partir de 15 parceiros |
