# Calculadora de IRRF – Folha de Pagamento (2026)
Igarapé Digital · by Anderson Marinho

## Visão Geral
Este repositório contém um simulador técnico de IRRF (retenção na fonte) voltado para conferência de folha de pagamento, com foco em transparência e rastreabilidade do cálculo: base tributável, método aplicado, IR antes da redução e IR final.

O projeto foi pensado para uso prático por RH/DP, Controladoria e Auditoria, principalmente em cenários de validação de parametrizações e conferências de mudanças legais.

## Destaque 2026 – Redução do IR mensal (Lei nº 15.270/2025)
A partir de janeiro de 2026, passou a existir uma regra de redução do imposto mensal que, na prática:
- zera o IR para rendimentos tributáveis mensais até R$ 5.000,00 (redução “até R$ 312,89”, limitada ao imposto devido);
- aplica redução parcial para rendimentos entre R$ 5.000,01 e R$ 7.350,00, por fórmula linear;
- não concede redução para rendimentos acima de R$ 7.350,00.

Base legal (texto oficial – Art. 3º-A da Lei nº 15.270/2025):
- Faixa até R$ 5.000,00: redução “até R$ 312,89 (de modo que o imposto devido seja zero)”
- Faixa de R$ 5.000,01 até R$ 7.350,00: redução = 978,62 – (0,133145 × rendimentos tributáveis sujeitos à incidência mensal)
- Acima de R$ 7.350,00: redução não aplicável

Observação técnica: a redução é aplicada sobre o imposto apurado (etapa posterior ao cálculo pela tabela progressiva). Ela não altera a base tributável; altera o imposto final.

## Conceito central: Base Tributável (tecnicidade)
Base tributável não é salário bruto. O IRRF depende do método.

Este simulador trabalha com:
- Modelo 1: Deduções legais (padrão)
- Modelo 2: Desconto simplificado (comparativo)

### Modelo 1 – Deduções legais (padrão do sistema)
Componentes típicos da base:
- Remuneração tributável
- (-) INSS
- (-) dedução por dependentes (quando aplicável)
- (-) pensão alimentícia dedutível (quando aplicável)
- (-) outras deduções legais (quando aplicável)

Fórmula conceitual:
Base Legal = (Rendimento – INSS) – Deduções Legais

### Modelo 2 – Desconto simplificado (configuração do simulador)
Neste repositório, o desconto simplificado está configurado como:
Base Simplificada = Rendimento – Desconto Simplificado

Importante: por decisão de configuração do simulador (para comparabilidade e alinhamento com o objetivo interno do projeto), nesta base simplificada não se deduz INSS. Isso é uma escolha do projeto (não uma afirmação de regra universal).

## Funcionalidades
- Ano-base 2026 ativo por padrão
- Opção padrão forçada: “Só deduções legais”
- INSS automático (tabela progressiva) com opção de desligar e informar manualmente
- Comparativo Legal vs Simplificado (base, alíquota efetiva e IR)
- Memória de cálculo detalhada (auditável)
- Barra visual (IR a pagar vs redução aplicada) usando as cores Sonova
- Footer com chave Pix para doação

## Como usar
1) Abra o arquivo index.html no navegador (projeto 100% estático).
2) Informe a remuneração tributável.
3) Mantenha “INSS Auto” ligado (recomendado) ou informe o INSS manualmente.
4) (Opcional) Informe dependentes, pensão e outras deduções legais.
5) Clique em Calcular e consulte:
   - base escolhida
   - IR antes de redução
   - redução 2026
   - IR final
   - memória de cálculo

## Estrutura do projeto
- index.html  (interface)
- style.css   (estilo)
- app.js      (regras, tabelas e cálculo)
- README.md   (este arquivo)

## Aviso
Este simulador é destinado a conferência e entendimento do cálculo na fonte (folha). Não substitui sistemas oficiais e não constitui orientação fiscal/jurídica.

## Autor e apoio
Igarapé Digital · by Anderson Marinho

Doações (Pix – chave):
oab.adv.anderson@gmail.com
