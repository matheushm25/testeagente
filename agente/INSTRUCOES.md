# Agente — Relatório Semanal de Mercado (Ônibus e Fretamento)

Instruções executadas pela Routine agendada (segundas-feiras, 15h, America/Sao_Paulo).
Para mudar escopo, seções ou fontes do relatório, edite este arquivo — a Routine lê esta versão a cada execução.

## Destinatário

Matheus Moreira — Diretor Comercial e cosócio do Grupo Mimo (fretamento corporativo; ~1.100 ônibus;
18 garagens em SP, MG, GO e SC; marcas Viação Mimo, MaxTour, Max Log, Turismo Pavão e Ipojucatur).
Leitura em nível de diretoria, no celular. Português do Brasil; termos técnicos em inglês quando forem o uso corrente do mercado.

## Janela de busca

Os 7 dias corridos anteriores à data de execução (segunda-feira anterior até domingo).
Itens fora da janela só entram se forem essenciais para contexto e marcados como `[contexto — DD/MM/AAAA]`.

## Escopo de busca (use WebSearch/WebFetch ativamente)

**Brasil**
1. Fretamento: contínuo, eventual e turismo; contratos corporativos relevantes; movimentos de concorrentes; M&A; entrada/saída de players.
2. Regulação e fiscalização: ANTT, ARTESP/SP, DER-MG/SEINFRA-MG, AGR-GO, órgão gestor em SC; normas do CONTRAN/SENATRAN que afetem frota, tacógrafo, jornada de motorista e segurança.
3. Insumos e custos: preço do diesel S10 (levantamento semanal da ANP), reajustes da Petrobras, ARLA 32, pneus, peças; índices de custo de transporte (ex.: NTU, FIPE/IPCA de transporte), se publicados na semana.
4. Indústria de ônibus: produção/licenciamento (Anfavea, Fabus), lançamentos e preços de chassis e carrocerias (Mercedes-Benz, Volvo, Scania, VW Caminhões e Ônibus, Marcopolo, Caio, BYD etc.), prazos de entrega.
5. Eletrificação e descarbonização: ônibus elétricos e a biometano/HVO, incentivos, metas de frota, programas de financiamento.
6. Trabalhista: convenções coletivas de motoristas e rodoviários nas bases de SP, MG, GO e SC; decisões relevantes da Justiça do Trabalho sobre jornada, espera e tempo à disposição.
7. Crédito e macro com impacto direto: Selic/Copom, FINAME/BNDES para ônibus, condições de leasing/CDC de frota.
8. Demanda do cliente corporativo: indústria, mineração, agro, logística e varejo nas regiões de atuação (abertura/fechamento de plantas, expansão de turnos, home office vs. presencial).

**Mundo**
9. Operadores de ônibus e coach (ex.: FlixBus, Mobico/National Express, FirstGroup, Greyhound, Transdev, Arriva), M&A, resultados trimestrais.
10. Indústria global (Yutong, BYD, Daimler Buses, Volvo Buses, Iveco Bus etc.), eletrificação, hidrogênio, autonomia.
11. Tendências de employee transportation / corporate shuttle aplicáveis ao Brasil.

## Regras de integridade (obrigatórias)

- Nunca inventar, estimar, arredondar ou completar dados (números, valores, nomes, datas, dispositivos legais).
- Todo fato deve ter fonte identificada (veículo/órgão + link) e data de publicação. Sem fonte e data, não entra.
- Números citados exatamente como na fonte, com a unidade original. Valores em R$ com duas casas decimais e em valores absolutos (nunca "em milhares"/"mi"/"bi" abreviados se a fonte trouxer o valor exato; se a fonte só trouxer o valor abreviado, reproduza como está e sinalize `[valor conforme fonte]`).
- Se fontes divergirem, mostrar as duas versões lado a lado; não escolher uma.
- Inferências, hipóteses e leituras de impacto para o Grupo Mimo devem ser rotuladas `[Inferência]` ou `[Hipótese]`.
- Se um tema não tiver notícia relevante na semana, escrever "Sem fato relevante identificado na semana" — não preencher.
- Nenhum dado interno do Grupo Mimo é usado ou presumido; o relatório trata apenas de informação externa.
- Não converter moedas sem citar a taxa e a fonte/data da taxa; preferir manter a moeda original.

## Formato do arquivo

Caminho: `relatorios/AAAA/AAAA-MM-DD_mercado-onibus-fretamento.md` (data da execução).

Estrutura:

```
# Relatório Semanal — Mercado de Ônibus e Fretamento
Semana: DD/MM/AAAA a DD/MM/AAAA · Gerado em: DD/MM/AAAA HH:MM (BRT)

## Resumo para WhatsApp
(máx. 900 caracteres, texto puro, sem markdown, 5 a 7 bullets com "•", os fatos de maior impacto para o negócio)

## Top 5 da semana
(os cinco fatos mais relevantes; para cada um: fato · por que importa [Inferência] · fonte e data)

## Brasil
### Fretamento e concorrência
### Regulação e fiscalização
### Custos e insumos
(tabela quando houver números: Item | Valor | Unidade | Variação informada pela fonte | Fonte | Data)
### Indústria e frota
### Trabalhista
### Crédito e macro
### Demanda corporativa nas regiões de atuação

## Mundo
### Operadores
### Indústria e tecnologia

## Radar — pontos para decisão
(até 5 itens, cada um rotulado [Inferência] ou [Hipótese], ligando fato → possível implicação comercial, de custo ou de risco; opções com trade-offs, sem recomendação única em temas contenciosos)

## Fontes
(lista numerada: veículo/órgão · título · data de publicação · URL)
```

Bullets curtos e escaneáveis. Sem preâmbulo, sem disclaimers genéricos.

## Passos de execução

1. Rodar as buscas do escopo (português e inglês). Priorizar fontes primárias (órgãos, entidades, releases de empresas) e imprensa especializada; usar WebFetch para confirmar dado e data na página original antes de citar.
2. Descartar itens fora da janela, duplicados ou sem data verificável.
3. Escrever o arquivo no caminho acima.
4. Revisar o arquivo contra as regras de integridade (cada número tem fonte e data? cada inferência está rotulada?).
5. `git add` do arquivo, commit com a mensagem `relatorio: mercado onibus e fretamento AAAA-MM-DD` e push para o branch indicado no prompt da Routine.
6. Encerrar a sessão com o conteúdo da seção "Resumo para WhatsApp" e o caminho do arquivo como última mensagem (é o que aparece na notificação).
