# Mapa de IA para escritórios de advocacia: esqueleto v0.1

Rascunho de trabalho · 08/10/2026 · dados em `mapa-ia-escritorios-dados-2026-10-08.json`

## 1. Para que serve

Uma conversa estruturada de duas horas com os sócios que termina em quatro entregas: notas para 12 dores, um ranking de 21 casos de uso, um plano em três ondas e indicadores de linha de base. Serve como diagnóstico de abertura e como material de venda consultiva.

As dores de bancas pequenas e médias se repetem, o que permite um mapa padrão. O que muda de uma banca para outra são as notas que cada sócio dá às dores.

## 2. Fluxo

1. **Perfil da banca:** áreas, número de advogados, ferramentas em uso e quem decide.
2. **Notas às dores:** cada uma de 0 a 3 (0 não pesa, 1 incomoda, 2 pesa, 3 urgente).
3. **Foco (opcional):** filtrar por frente (Proteger, Produzir, Reter, Crescer) ou por interno/externo.
4. **Ranking:** o mapa ordena os casos pelas notas, pelo impacto e pelo esforço.
5. **Plano em três ondas:** 0 a 90 dias, 3 a 6 meses, 6 a 12 meses.
6. **Relatório:** mapa, plano, indicadores e próximo passo.

## 3. Regras de pontuação

- **Prioridade** = 3 × impacto + soma das notas das dores que o caso ataca − 2 × esforço.
- **Onda 1** (0 a 90 dias): esforço ≤ 2 e impacto ≥ 3.
- **Onda 3** (6 a 12 meses): esforço ≥ 4.
- **Onda 2** (3 a 6 meses): os demais.
- **Limite de plano:** mostrar de 3 a 5 casos por onda, na ordem de prioridade. O resto fica na fila.

Impacto e esforço vão de 1 a 5 e são julgamentos iniciais. Devem ser calibrados com dados reais dos pilotos.

## 4. As 12 dores

| ID | Dor | Descrição |
|---|---|---|
| P1 | Prazos e publicações | Intimações chegam por vários canais. Leitura, contagem e agenda dependem de uma pessoa, e um prazo perdido custa caro. |
| P2 | Pesquisa lenta e citação sem lastro | Cada tese consome horas, e há o risco de citar precedente inexistente ou que não diz o que a peça afirma. |
| P3 | Peças repetitivas, qualidade irregular | A mesma petição é reescrita do zero e o padrão muda de advogado para advogado. |
| P4 | Conhecimento preso nas pessoas | Teses, modelos e pareceres ficam em pastas e e-mails. Quem sai leva o saber junto. |
| P5 | Documentos em volume | Autos, contratos, provas e cálculos exigem leitura integral, e o tempo de leitura aperta o prazo. |
| P6 | Horas, honorários e faturamento | Lançamento de horas atrasado, cobrança irregular e pouca visibilidade da rentabilidade. |
| P7 | Cliente que quer informação | "Como está meu processo?" ocupa advogados, e os relatórios são feitos à mão. |
| P8 | Sigilo e proteção de dados | Dados de clientes circulam em ferramentas pessoais ou sem contrato que proíba o treino com eles. |
| P9 | IA sem regra nem registro | Cada um usa a ferramenta que prefere e ninguém sabe quem conferiu o quê antes de protocolar. |
| P10 | Pressão de preço e de eficiência | Clientes empresariais comparam bancas, auditam faturas e pedem previsibilidade de custo. |
| P11 | Captação e relacionamento | Novos clientes dependem de indicação, e a triagem inicial e a presença digital são artesanais. |
| P12 | Gestão e sucessão da banca | Decisões sem indicadores de carteira, prazo e margem, com forte dependência dos sócios fundadores. |

## 5. As quatro frentes e os 21 casos

- **Proteger** (4 casos): Reduz risco: prazo perdido, citação sem lastro, vazamento de dado.
- **Produzir** (7 casos): Ganha tempo na peça, na pesquisa e na leitura de documentos.
- **Reter** (3 casos): Transforma o saber dos sócios em patrimônio da banca.
- **Crescer** (7 casos): Melhora a relação com o cliente, a gestão e a captação.

### Visão geral

| ID | Caso | Frente | Quem usa o resultado | Impacto | Esforço | Dores | Onda base |
|---|---|---|---|---|---|---|---|
| C01 | Mesa de prazos | Proteger | Equipe (interno) | 4 | 2 | P1 | 1 |
| C02 | Conferência de citações antes de protocolar | Proteger | Equipe (interno) | 5 | 2 | P2, P9 | 1 |
| C03 | Política de uso de IA e registro de conferência | Proteger | Equipe (interno) | 4 | 1 | P8, P9 | 1 |
| C04 | Anonimização antes do uso de IA | Proteger | Equipe (interno) | 3 | 2 | P8 | 1 |
| C05 | Pesquisa jurisprudencial com fonte | Produzir | Equipe (interno) | 4 | 3 | P2 | 2 |
| C06 | Primeira minuta a partir do modelo da casa | Produzir | Equipe (interno) | 5 | 3 | P3 | 2 |
| C07 | Resumo de autos e linha do tempo | Produzir | Equipe (interno) | 4 | 2 | P5, P3 | 1 |
| C08 | Revisão de contratos com checklist da banca | Produzir | Equipe (interno) | 4 | 3 | P5, P3 | 2 |
| C09 | Conferência de cálculos trabalhistas e de liquidação | Produzir | Equipe (interno) | 4 | 3 | P5, P1 | 2 |
| C10 | Due diligence em lote | Produzir | Equipe (interno) | 5 | 4 | P5, P10 | 3 |
| C11 | Preparação de audiência | Produzir | Equipe (interno) | 3 | 3 | P3 | 2 |
| C12 | Memória da banca | Reter | Equipe (interno) | 5 | 4 | P4, P2 | 3 |
| C13 | Biblioteca de instruções permanentes | Reter | Equipe (interno) | 4 | 2 | P3, P4, P9 | 1 |
| C14 | Trilha de entrada para associados e estagiários | Reter | Equipe (interno) | 3 | 2 | P4, P12 | 1 |
| C15 | Relatório periódico ao cliente | Crescer | Cliente (externo) | 4 | 2 | P7, P10 | 1 |
| C16 | Demonstrativo de valor para cliente que audita fatura | Crescer | Cliente (externo) | 3 | 2 | P10, P6 | 1 |
| C17 | Painel de gestão da banca | Crescer | Equipe (interno) | 4 | 3 | P6, P12 | 2 |
| C18 | Pré-lançamento de horas | Crescer | Equipe (interno) | 3 | 2 | P6 | 1 |
| C19 | Triagem de novos clientes | Crescer | Cliente (externo) | 3 | 2 | P11, P7 | 1 |
| C20 | Conteúdo jurídico para redes dentro das regras da OAB | Crescer | Cliente (externo) | 2 | 1 | P11 | 2 |
| C21 | Proposta e precificação | Crescer | Equipe (interno) | 3 | 3 | P10, P6 | 2 |

### Ficha resumida

| ID | O que a IA faz | O que o advogado decide | Métrica |
|---|---|---|---|
| C01 | Lê intimações e publicações, conta o prazo, avisa o responsável e deixa uma minuta de providência pronta. | Confirma a contagem e assina. | Prazos perdidos; tempo entre publicação e distribuição. |
| C02 | Extrai toda citação da minuta, localiza na fonte oficial, compara o trecho e emite um relatório de conferência. | Lê o inteiro teor e decide o que fica na peça. | Citações não localizadas por peça; tempo de conferência. |
| C03 | Apoia a redação da regra, da lista de ferramentas aprovadas e do modelo de registro. | Os sócios aprovam a regra e a cláusula de transparência nos honorários. | % de peças com registro; uso de ferramentas fora da lista. |
| C04 | Remove nomes, CPFs, valores e endereços de um documento antes de ele ir para a ferramenta. | Define o que precisa ser anonimizado em cada tipo de caso. | % de documentos tratados; incidentes de dados. |
| C05 | Busca no acervo da banca e em repositórios oficiais e entrega cada decisão com link e um mapa de divergências. | Escolhe os precedentes e lê o inteiro teor. | Horas por tese; taxa de erro de citação. |
| C06 | Monta petição inicial, contestação, recurso ou notificação com os fatos aprovados, citando a folha de cada um. | Aprova os fatos antes da redação e revisa a peça. | Horas até a primeira versão; retrabalho por peça. |
| C07 | Resume o processo em ordem cronológica, com remissão à folha de cada fato. | Confere os fatos críticos nos autos. | Horas de leitura; fatos corrigidos na revisão. |
| C08 | Aplica o checklist de cláusulas, aponta riscos e cita a cláusula e a página. | Decide o que negociar e o que aceitar. | Tempo por contrato; riscos encontrados na revisão do sócio. |
| C09 | Lê a decisão, refaz o cálculo fora do modelo de linguagem e minuta a impugnação. | Valida as premissas e assina a impugnação. | Horas por cálculo; diferença encontrada. |
| C10 | Lê uma sala de dados inteira e entrega um relatório de pontos de atenção, com a fonte de cada ponto. | Prioriza os riscos e conversa com o cliente. | Horas por data room; pontos relevantes descobertos só na revisão. |
| C11 | Sugere roteiro de perguntas, pontos fortes e fracos e simula perguntas da parte contrária. | Define a estratégia e conduz a audiência. | Tempo de preparação; avaliação do advogado após a audiência. |
| C12 | Organiza teses, modelos e pareceres aprovados e responde às perguntas da equipe com a fonte interna. | Aprova o que entra, com dono, versão e data. | Consultas respondidas com fonte; tempo para achar um modelo. |
| C13 | Carrega o padrão de redação, de resumo e de conferência da banca em toda conversa com a ferramenta. | Revisa e versiona as instruções como qualquer documento da casa. | % da equipe usando o padrão; variação de qualidade entre peças. |
| C14 | Monta exercícios e estudos de caso a partir de peças aprovadas e modelos da banca. | Escolhe os casos e dá o retorno. | Tempo até autonomia do novo advogado. |
| C15 | Gera o andamento de cada processo em linguagem simples, com os pontos de atenção do período. | Revisa e envia. | Consultas de andamento recebidas; horas gastas em relatórios. |
| C16 | Reúne horas, entregas e resultado em um relatório padronizado por cliente. | Valida o texto e a narrativa de valor. | Glosas de fatura; tempo de resposta a auditorias. |
| C17 | Consolida carteira, prazos, horas e rentabilidade por área e por cliente e responde em linguagem natural. | Define os indicadores e decide a partir deles. | Decisões tomadas com dado; fechamento mensal mais rápido. |
| C18 | Sugere o lançamento a partir da agenda, dos e-mails e dos documentos do dia. | Confirma ou ajusta. | Horas lançadas no mesmo dia; faturamento sem atraso. |
| C19 | Recebe a demanda por formulário, resume o caso e propõe agenda, dentro de uma alçada definida. | Aceita ou recusa o caso e fecha o contrato. | Tempo de primeira resposta; taxa de conversão. |
| C20 | Escreve o rascunho de um conteúdo informativo a partir de um tema escolhido pelo advogado. | Aprova e garante que cumpre as regras de publicidade da advocacia. | Publicações por mês; contatos gerados. |
| C21 | Cruza histórico de horas e resultados por tipo de causa para sugerir honorários fixos, mistos ou de êxito. | Decide o preço e a estratégia comercial. | Margem por tipo de causa; taxa de aprovação de propostas. |

## 6. Simulação ilustrativa

**Aviso:** as notas abaixo são hipotéticas, para um perfil de banca com contencioso cível e trabalhista e consultivo empresarial. Não descrevem nenhum escritório real e devem ser refeitas com os sócios.

| Dor | Nota |
|---|---|
| P1 Prazos e publicações | 3 |
| P2 Pesquisa lenta e citação sem lastro | 3 |
| P4 Conhecimento preso nas pessoas | 3 |
| P8 Sigilo e proteção de dados | 3 |
| P9 IA sem regra nem registro | 3 |
| P3 Peças repetitivas, qualidade irregular | 2 |
| P5 Documentos em volume | 2 |
| P7 Cliente que quer informação | 2 |
| P6 Horas, honorários e faturamento | 1 |
| P10 Pressão de preço e de eficiência | 1 |
| P12 Gestão e sucessão da banca | 1 |
| P11 Captação e relacionamento | 0 |

### Ranking resultante

| # | Caso | Frente | Impacto | Esforço | Soma das notas | Prioridade | Onda |
|---|---|---|---|---|---|---|---|
| 1 | C02 Conferência de citações antes de protocolar | Proteger | 5 | 2 | 6 | 17 | 1 |
| 2 | C03 Política de uso de IA e registro de conferência | Proteger | 4 | 1 | 6 | 16 | 1 |
| 3 | C13 Biblioteca de instruções permanentes | Reter | 4 | 2 | 8 | 16 | 1 |
| 4 | C12 Memória da banca | Reter | 5 | 4 | 6 | 13 | 3 |
| 5 | C07 Resumo de autos e linha do tempo | Produzir | 4 | 2 | 4 | 12 | 1 |
| 6 | C01 Mesa de prazos | Proteger | 4 | 2 | 3 | 11 | 1 |
| 7 | C06 Primeira minuta a partir do modelo da casa | Produzir | 5 | 3 | 2 | 11 | 2 |
| 8 | C09 Conferência de cálculos trabalhistas e de liquidação | Produzir | 4 | 3 | 5 | 11 | 2 |
| 9 | C15 Relatório periódico ao cliente | Crescer | 4 | 2 | 3 | 11 | 1 |
| 10 | C08 Revisão de contratos com checklist da banca | Produzir | 4 | 3 | 4 | 10 | 2 |
| 11 | C10 Due diligence em lote | Produzir | 5 | 4 | 3 | 10 | 3 |
| 12 | C05 Pesquisa jurisprudencial com fonte | Produzir | 4 | 3 | 3 | 9 | 2 |
| 13 | C14 Trilha de entrada para associados e estagiários | Reter | 3 | 2 | 4 | 9 | 1 |
| 14 | C04 Anonimização antes do uso de IA | Proteger | 3 | 2 | 3 | 8 | 1 |
| 15 | C17 Painel de gestão da banca | Crescer | 4 | 3 | 2 | 8 | 2 |
| 16 | C16 Demonstrativo de valor para cliente que audita fatura | Crescer | 3 | 2 | 2 | 7 | 1 |
| 17 | C19 Triagem de novos clientes | Crescer | 3 | 2 | 2 | 7 | 1 |
| 18 | C18 Pré-lançamento de horas | Crescer | 3 | 2 | 1 | 6 | 1 |
| 19 | C11 Preparação de audiência | Produzir | 3 | 3 | 2 | 5 | 2 |
| 20 | C21 Proposta e precificação | Crescer | 3 | 3 | 2 | 5 | 2 |
| 21 | C20 Conteúdo jurídico para redes dentro das regras da OAB | Crescer | 2 | 1 | 0 | 4 | 2 |

### Plano (3 a 5 casos por onda)

- **Onda 1 · 0 a 90 dias:** C02 Conferência de citações antes de protocolar; C03 Política de uso de IA e registro de conferência; C13 Biblioteca de instruções permanentes; C07 Resumo de autos e linha do tempo; C01 Mesa de prazos
- **Onda 2 · 3 a 6 meses:** C06 Primeira minuta a partir do modelo da casa; C09 Conferência de cálculos trabalhistas e de liquidação; C08 Revisão de contratos com checklist da banca; C05 Pesquisa jurisprudencial com fonte; C17 Painel de gestão da banca
- **Onda 3 · 6 a 12 meses:** C12 Memória da banca; C10 Due diligence em lote

## 7. O que falta para virar produto

1. **Validar** as 12 dores e os 21 casos com 3 a 5 escritórios de perfis diferentes.
2. **Calibrar** impacto e esforço com dados do primeiro piloto (horas, citações não localizadas, prazos).
3. **Fontes:** documentar uma referência pública para cada dor. Hoje há base para P1, P2, P3, P5, P8 e P9; faltam P6, P10, P11 e P12.
4. **Versão interativa:** planilha ou página web com as notas, o ranking e o relatório em PDF.
5. **Revisão ética:** conferir com advogado as regras de publicidade e sigilo da OAB antes de divulgar o material.

Todo o texto é original e deve passar por revisão jurídica antes de ser publicado.
