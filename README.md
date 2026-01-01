CALCULADORA DE IRRF – FOLHA DE PAGAMENTO (2026)
IGARAPÉ DIGITAL · ANDERSON MARINHO

============================================================
1) VISÃO GERAL
============================================================
Este projeto é uma calculadora técnica de IRRF na fonte (folha de pagamento), criada para simulação, conferência e entendimento aprofundado da BASE TRIBUTÁVEL, considerando as regras vigentes e, principalmente, as alterações introduzidas pela Medida Provisória que redefine a sistemática do IR mensal a partir de 2026.

O foco é transparência técnica: mostrar a lógica fiscal, permitir comparação entre métodos e registrar memória de cálculo para análise de RH/DP, Controladoria e Auditoria.

============================================================
2) CONTEXTO LEGAL – MEDIDA PROVISÓRIA (IRRF 2026)
============================================================
A Medida Provisória com vigência a partir de janeiro de 2026 trouxe mudanças relevantes na apuração do IRRF mensal, com destaque para:

- Manutenção da tabela progressiva mensal do IR
- Criação de um mecanismo de redução do imposto para rendas mensais até R$ 7.350,00
- Isenção prática do IR para rendas mensais até R$ 5.000,00, via redutor
- Redução decrescente do imposto para rendas entre R$ 5.000,01 e R$ 7.350,00
- Nenhuma redução aplicada para rendas acima de R$ 7.350,00

Ponto técnico: a MP não precisa alterar a tabela (faixas/alíquotas) para mudar o resultado final. Ela cria uma etapa posterior ao cálculo do IR pela base tributável, impactando o valor final a ser retido na fonte.

============================================================
3) CONCEITO CENTRAL – BASE TRIBUTÁVEL (TECNICIDADE)
============================================================
Base tributável não é salário bruto. A base do IRRF depende do método adotado.

O simulador trabalha com dois modelos:

------------------------------------------------------------
3.1) MODELO 1 – DEDUÇÕES LEGAIS (PADRÃO)
------------------------------------------------------------
Modelo padrão e mais comum na folha.

Componentes da base:
- Remuneração tributável
- (-) INSS
- (-) Dedução por dependentes
- (-) Pensão alimentícia dedutível
- (-) Outras deduções legais

Fórmula conceitual:
Base Legal = (Rendimento – INSS) – Deduções Legais

Este é o método configurado como PADRÃO no simulador:
- “Forçar opção” ligado
- “Só deduções legais” selecionado por padrão

------------------------------------------------------------
3.2) MODELO 2 – DESCONTO SIMPLIFICADO
------------------------------------------------------------
Modelo alternativo previsto em lei, substitui deduções legais por um valor fixo mensal.

Neste projeto (configuração atual do simulador):
Base Simplificada = Rendimento – Desconto Simplificado
Observação importante: nesta configuração, NÃO se deduz INSS na base simplificada (decisão de configuração do simulador).

Essa abordagem deixa explícito que:
- O simplificado não é automaticamente mais vantajoso
- Pode gerar base maior e IR maior dependendo do cenário
- A escolha precisa ser consciente e comparável

============================================================
4) REDUÇÃO DO IR – REGRA 2026 (APÓS O CÁLCULO DO IR)
============================================================
Após calcular o IR pela tabela progressiva mensal, aplica-se a redução (quando habilitada):

- Renda mensal até R$ 5.000,00: IR reduzido a zero
- Renda entre R$ 5.000,01 e R$ 7.350,00: aplica redutor conforme a fórmula oficial
- Renda acima de R$ 7.350,00: não aplica redução

Importante: a redução NÃO altera a base tributável; ela altera o imposto final apurado.

============================================================
5) FUNCIONALIDADES
============================================================
- Cálculo automático de INSS progressivo (quando “Auto” estiver ligado)
- Simulação mensal e 13º (exclusivo na fonte)
- Comparativo entre métodos (legal vs simplificado)
- Destaque visual do método escolhido
- Barra visual: IR a pagar vs redução aplicada (cores Sonova)
- Memória de cálculo completa e auditável
- Interface corporativa e orientada à conferência

============================================================
6) AVISO
============================================================
Este simulador é para conferência na fonte (folha) e fins de estudo/validação.
Não substitui sistemas oficiais de folha e não gera obrigação fiscal.

============================================================
7) AUTORIA E APOIO
============================================================
Igarapé Digital · by Anderson Marinho

Doações (Pix - chave):
oab.adv.anderson@gmail.com
