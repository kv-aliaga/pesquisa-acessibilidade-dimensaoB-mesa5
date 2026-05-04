# ♿ Acessibilidade Digital — Pesquisa Comparativa

## Sobre esta pesquisa

Esta pesquisa investiga a dimensão **legislativa e técnica** da acessibilidade digital, analisando como grandes empresas (IBM, Meta, JBS e Seara) implementam políticas de acessibilidade em seus produtos, quais ferramentas adotam, e quais riscos jurídicos existem para times de desenvolvimento que ignoram o tema.

---

## O que descobrimos (Principais Achados)

- **96,3% dos sites analisados pelo WebAIM Million apresentam falhas de acessibilidade automáticas detectáveis**, e apenas 2,9% dos sites brasileiros passaram em todos os testes em 2024 — o que revela que acessibilidade ainda é exceção, não regra. *(Fonte: WebAIM Million Report 2024)*

- **A IBM exige conformidade com WCAG 2.2 internamente desde outubro de 2024** (versão 7.3 do checklist interno CI162) e publica ACRs (*Accessibility Conformance Reports*) para todos os seus produtos, tornando-se referência corporativa global em acessibilidade digital. *(Fonte: IBM Accessibility Policy / VPAT® 2.x)*

- **O caso Robles v. Domino's Pizza (EUA) consolidou que sites e apps são cobertos pela ADA**: após seis anos de litígio, a Suprema Corte recusou revisar a decisão favorável ao usuário cego, confirmando que a acessibilidade digital é exigência legal — não apenas boa prática. *(Fonte: Robles v. Domino's Pizza, 9th Circuit, 2019)*

- **No Brasil, o Ministério Público Federal já acionou empresas por barreiras digitais**: a operadora Claro foi notificada a implementar leitor de tela integral em seu site e guia de TV, e a plataforma Gov.br recebeu recomendação de correção urgente para acesso de pessoas com deficiência visual. *(Fonte: Recomendações MPF, 2023–2024)*

- **18,6 milhões de brasileiros têm deficiência (8,9% da população)**, e a LBI prevê multa máxima de R$ 214.301.536,00 por descumprimento — o que torna o risco de omissão concreto e mensurável para qualquer produto digital no mercado nacional. *(Fonte: IBGE / Lei Brasileira de Inclusão — LBI 13.146/2015)*

---

## Ferramentas / Casos / Legislação

### 🗺️ Mapa Comparativo — Acessibilidade Digital nas Empresas

| Empresa | Política Formal | Padrão Adotado | Ferramentas / Recursos | Caso Público |
|---|---|---|---|---|
| **IBM** | ✅ Sim (CI162 interna + ACRs públicos) | WCAG 2.2, Section 508, EN 301 549 | Equal Access Toolkit, IBM Equal Access Checker, NavCog, Vision D | Nenhum processo. Pioneira em leitor de tela para DOS nos anos 1980. |
| **Meta** | ⚠️ Parcial (Transparency Center, sem conformidade declarada) | Não declarado formalmente | Alt text por IA, legendas automáticas, audiodescrição, Ray-Ban Meta Smart Glasses | NFB (2024): descontinuação do MBasic excluiu usuários cegos. Correções parciais em jan/2025. |
| **JBS / Friboi** | ⚠️ Interno (ESG, sem política digital pública) | Não declarado | SAC em Libras ao vivo, curso de Libras interno, site com score 100% Lighthouse (técnico, sem recursos ao usuário) | Nenhum processo. |
| **Seara** | ⚠️ Interno (alinhada ao Grupo JBS) | Não declarado | SAC em Libras ao vivo (primeira marca de alimentos processados do grupo) | Nenhum processo. |

---

### ⚖️ Legislação Relevante

| Norma | Âmbito | O que exige |
|---|---|---|
| **WCAG 2.1 / 2.2** | Internacional | Diretrizes técnicas de acessibilidade web (referenciadas pela LBI e e-MAG) |
| **LBI — Lei 13.146/2015** | Brasil | Acessibilidade em produtos, serviços e comunicação digital; multa de até R$ 214 mi |
| **e-MAG** | Brasil (gov) | Modelo de Acessibilidade em Governo Eletrônico, obrigatório para sites públicos |
| **Decreto 11.034/2022** | Brasil | Nova lei do SAC — inclui obrigatoriedade de canais acessíveis para PcDs |
| **ADA (Americans with Disabilities Act)** | EUA | Cobre sites e apps vinculados a estabelecimentos físicos (confirmado em Robles v. Domino's) |
| **Section 508** | EUA (gov) | Obrigatório para produtos de TI adquiridos pelo governo americano |
| **EN 301 549** | União Europeia | Norma de acessibilidade digital para contratos públicos europeus |

---

### 📋 Casos Jurídicos e Regulatórios

**🇺🇸 Robles v. Domino's Pizza (2016–2019)**
Guillermo Robles, usuário com deficiência visual, não conseguiu realizar pedidos no site e app da Domino's usando leitores de tela. A empresa alegou que a ADA não se aplicava ao ambiente digital. A Justiça decidiu que, como os serviços online estavam diretamente ligados às lojas físicas, também deveriam ser acessíveis. Em 2019, a Suprema Corte recusou revisar a decisão — consolidando a acessibilidade digital como exigência legal nos EUA. Nos anos seguintes, os processos sob a ADA passaram de 4.000/ano, com 41% contra reincidentes.

**🇧🇷 MPF × Claro**
O Ministério Público Federal recomendou que a operadora Claro implemente leitor de tela integral no guia de programação de TV por assinatura e em sua página eletrônica, garantindo que clientes com deficiência visual possam acessar nomes de atrações, horários, sinopses e menus de configuração em áudio.

**🇧🇷 MPF × Gov.br**
O MPF recomendou ajustes urgentes na plataforma Gov.br para corrigir falhas que impedem pessoas com deficiência visual de realizar login e reconhecimento facial. O prazo estabelecido para cumprimento foi de 60 dias.

**🇺🇸 Meta × National Federation of the Blind (2024–2025)**
Em 2024, a Meta descontinuou o MBasic (mbasic.facebook.com), versão simplificada do Facebook que havia se tornado a principal interface acessível para usuários de leitores de tela no desktop. A NFB iniciou negociações formais em outubro de 2024. Em janeiro de 2025, a Meta implementou correções parciais — mas a NFB sinalizou que ainda há muito a ser feito.

---

## Como isso afeta o nosso trabalho como desenvolvedores

**1. Acessibilidade é critério de entrega, não tarefa de QA**
Seguir WCAG 2.1/2.2 e e-MAG deixou de ser opcional. Na prática, isso significa: navegação completa por teclado, `alt text` descritivo em imagens, contraste de cores adequado (mínimo 4.5:1), uso correto de ARIA e compatibilidade com leitores de tela como NVDA, JAWS e VoiceOver.

**2. O planejamento começa com inclusão**
Os dados mostram que 96,3% dos sites falham em testes automáticos — o que indica que acessibilidade é sistematicamente deixada para o fim do ciclo. A partir desta pesquisa, critérios de acessibilidade devem entrar nas histórias de usuário, na definição de pronto (*definition of done*) e nas revisões de PR.

**3. O risco jurídico é real e crescente**
A LBI permite multas milionárias. O MPF já acionou empresas no Brasil. Nos EUA, mais de 4.000 processos foram abertos em 2024 — 41% contra empresas que já haviam sido processadas antes. Ignorar acessibilidade é acumular passivo jurídico.

**4. Automatizar não é suficiente — é o ponto de partida**
Ferramentas como IBM Equal Access Checker, Lighthouse e axe detectam ~30–40% das falhas de acessibilidade. O restante só é identificado com testes manuais e com usuários reais. Score 100% no Lighthouse (como o site da JBS) não significa que o site é acessível ao usuário final.

**5. Cada decisão técnica define quem pode usar o que você construiu**
18,6 milhões de brasileiros têm deficiência. Uma decisão de não adicionar `alt text`, não testar navegação por teclado ou não validar contraste de cores não é neutra — ela exclui pessoas diretamente. Acessibilidade não é sobre escrever código diferente. É sobre desenvolver com responsabilidade.