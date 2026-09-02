# Simulador de Investimentos em Fundos Imobiliários (FIIs)

##   Sobre o Projeto

Este projeto é uma ferramenta desenvolvida em Excel para simular investimentos em Fundos de Investimento Imobiliário (FIIs). A planilha funciona como um pequeno dashboard interativo, permitindo ao usuário calcular o valor total investido, o patrimônio acumulado ao longo do tempo e os dividendos mensais estimados — ajudando investidores iniciantes a entender melhor o impacto de seus aportes.

Projeto desenvolvido como desafio prático do curso **Excel Avançado com IA e Claude** (Santander Open Academy / DIO).

##   Objetivos

- Aplicar os conceitos de Excel no desenvolvimento de uma ferramenta prática de simulação de investimentos
- Automatizar cálculos financeiros complexos (valor investido, patrimônio acumulado, dividendos mensais)
- Documentar um processo técnico de forma clara e estruturada
- Compartilhar a solução via GitHub

##   Como a Planilha Funciona

A aba **APP** reúne todas as informações em um único painel:

### 1. Configurações
Dados de referência do usuário (salário e rendimento médio da carteira), usados para sugerir um valor de investimento mensal.

### 2. Investimentos Mensais
O usuário define:
- Quanto pretende investir por mês
- Por quantos anos pretende investir
- A taxa de rendimento mensal estimada

A partir disso, a planilha calcula automaticamente o **Patrimônio Acumulado** (usando a função `FV` — Valor Futuro, com juros compostos) e os **Dividendos Mensais** estimados sobre esse patrimônio.

### 3. Cenários
Uma tabela mostra o patrimônio e os dividendos projetados em 5 horizontes de tempo diferentes (2, 5, 10, 20 e 30 anos), permitindo comparar o efeito do tempo sobre os investimentos.

### 4. Perfil e Alocação por Tipo de FII
Um seletor (dropdown) permite escolher entre os perfis **Conservador**, **Moderado** e **Agressivo**. Ao selecionar um perfil, a planilha distribui automaticamente o valor mensal investido entre os diferentes tipos de fundos (Papel, Tijolo, Híbridos, FOFs, Desenvolvimento e Hotelarias), de acordo com percentuais pré-definidos para cada perfil de risco. Um gráfico de pizza ilustra essa distribuição em tempo real.

## ⚙️ Recursos Técnicos Utilizados

- **Intervalos nomeados** (`aporte`, `patrimonio`, `qnt_anos`, `taxa_mensal`, `rendimento_carteira`, `salario`) para tornar as fórmulas mais legíveis
- **Função FV (Valor Futuro)** para cálculo de juros compostos
- **VLOOKUP** para buscar os percentuais de alocação de cada perfil em uma tabela de apoio
- **Validação de dados** (dropdown) para o campo de seleção de perfil
- **Formatação visual** (cor de preenchimento) para diferenciar células de entrada (input) das células de resultado

##   Premissas Assumidas

- A taxa de rendimento mensal (`taxa_mensal`) e o rendimento da carteira (`rendimento_carteira`) são estimativas médias, ajustáveis conforme o histórico real dos fundos escolhidos pelo usuário
- Os percentuais de alocação por perfil de risco (Conservador/Moderado/Agressivo) são valores de referência, não recomendações de investimento

## 🗂️ Estrutura do Repositório

```
├── README.md
├── Simulador_de_Investimentos.xlsx
└── images/
    └── (capturas de tela da planilha)
```

##   Como Usar

1. Baixe o arquivo `Simulador_de_Investimentos.xlsx`
2. Preencha os campos destacados (Salário, Rendimento da Carteira, Quanto Investir por Mês, Por Quantos Anos, Taxa de Rendimento)
3. Escolha seu perfil de investidor no dropdown
4. Acompanhe os resultados calculados automaticamente

##   Autora

Aura Gaspar Ribeiro
