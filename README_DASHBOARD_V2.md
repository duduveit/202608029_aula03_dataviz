# 🚀 Dashboard Avançado de Vendas - Versão 2.0

Um dashboard empresarial profissional para análise completa de vendas por estado e região, desenvolvido com **D3.js 7** e **Chart.js**, oferecendo múltiplas perspectivas de dados com interatividade avançada.

## ✨ Novas Funcionalidades (v2.0)

### 📊 Visualizações Avançadas
- **Sunburst Chart**: Hierarquia interativa Brasil → Região → Estado
- **Bar Chart**: Comparação de vendas por região com animações
- **Pie/Doughnut Chart**: Distribuição de clientes por região
- **Line Chart**: Evolução temporal de vendas
- **Scatter Plot**: Correlação entre clientes e vendas
- **Heatmap**: Matriz de estados vs métricas
- **Radar Chart**: Métricas multidimensionais por região

### 🎯 Sistema de Filtros Inteligentes
- Filtrar por região específica
- Filtro de período (3m, 6m, 12m)
- Atualização dinâmica de todos os gráficos
- Exportação de dados filtrados em JSON

### 📈 Dashboard de KPIs (6 Métricas)
1. **Faturamento Total** - Em milhões (R$)
2. **Total de Pedidos** - Transações realizadas
3. **Total de Clientes** - Clientes únicos
4. **Ticket Médio** - Valor médio por pedido
5. **Cidades Atendidas** - Municípios alcançados
6. **Taxa de Entrega** - % de sucesso nas entregas

### 📑 Abas Temáticas (5 Seções)

#### 1️⃣ **Visão Geral**
- KPIs consolidados com card design moderno
- Sunburst chart interativo
- Gráficos comparativos por região
- Resumo executivo

#### 2️⃣ **Detalhes por Estado**
- Ranking completo de estados por faturamento
- Posição, região, vendas, pedidos, clientes
- Taxa de entrega por estado
- Tabela interativa com ordenação

#### 3️⃣ **Análise Temporal**
- Evolução de vendas ao longo dos meses
- Top 10 meses com melhor desempenho
- Gráfico de crescimento mês a mês (MoM)
- Tendências e sazonalidade

#### 4️⃣ **Comparação Regional**
- Heatmap de estados vs regiões
- Scatter plot (clientes vs vendas)
- Gráfico radar com múltiplas métricas
- Análise correlacional visual

#### 5️⃣ **Análise Avançada**
- Correlação estatística (Clientes vs Vendas)
- Índice de Concentração (Herfindahl)
- Coeficiente de Variação
- Desvio Padrão de Vendas
- Insights automáticos e recomendações

## 🎨 Design & UX

### Tema Visual
- **Gradient Moderno**: Azul-roxo em header e botões
- **Cards com Efeito Hover**: Animações suaves
- **Paleta de Cores por Região**:
  - 🔴 Norte: Vermelho (#FF6B6B)
  - 🔵 Nordeste: Teal (#4ECDC4)
  - 🟡 Centro-Oeste: Azul Claro (#45B7D1)
  - 🟠 Sudeste: Salmão (#FFA07A)
  - 🟢 Sul: Verde Água (#98D8C8)

### Responsividade
- Totalmente responsivo (desktop, tablet, mobile)
- Grid adaptativo
- Abas em cascata em telas pequenas

## 📁 Arquivos Necessários

```
/workspaces/202608029_aula03_dataviz/
├── dashboard_avancado.html       # Dashboard principal (v2.0)
├── dados_vendas_avancado.json    # Dados enriquecidos
├── dashboard.html                # Dashboard v1.0 (legado)
├── dados_vendas.json             # Dados simples (legado)
└── docs/
    └── schema.md                 # Documentação do banco
```

## 🚀 Como Usar

### Método 1: Live Server (VS Code) ⭐ Recomendado
```bash
# No VS Code:
1. Instale a extensão "Live Server"
2. Clique direito em dashboard_avancado.html
3. Selecione "Open with Live Server"
```

### Método 2: Navegador Direto
```bash
# Simplesmente abra o arquivo:
file:///workspaces/202608029_aula03_dataviz/dashboard_avancado.html
```

### Método 3: Servidor Python
```bash
cd /workspaces/202608029_aula03_dataviz
python3 -m http.server 8000

# Acesse: http://localhost:8000/dashboard_avancado.html
```

## 📊 Dados Inclusos

### Volume de Dados
- **27 Estados** brasileiros
- **5 Regiões** (Norte, Nordeste, Centro-Oeste, Sudeste, Sul)
- **25 Períodos** de tempo (meses)
- **103.886 Pedidos** analisados
- **R$ 16.008.872,12** em faturamento total

### Destaques Regionais
| Região | Faturamento | Pedidos | Clientes | Taxa Entrega |
|--------|-------------|---------|----------|--------------|
| **Sudeste** | R$ 10,3M | 43.622 | 41.745 | 97% |
| **Sul** | R$ 2,3M | 5.668 | 5.466 | 95% |
| **Nordeste** | R$ 1,9M | 3.610 | 3.380 | 93% |
| **Centro-Oeste** | R$ 1,0M | 2.204 | 2.140 | 92% |
| **Norte** | R$ 414k | 970 | 896 | 90% |

## 🔧 Recursos Técnicos

### Bibliotecas Utilizadas
- **D3.js v7** - Visualizações avançadas
- **Chart.js 3.9** - Gráficos com animação
- **Poppins Font** - Tipografia moderna
- **CSS3 Grid/Flexbox** - Layout responsivo

### Compatibilidade
- ✅ Chrome/Chromium (recomendado)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ IE11 (não testado)

## 💡 Funcionalidades Interativas

### Hover & Tooltips
- Todos os gráficos mostram tooltips ao passar o mouse
- Informações detalhadas com formatação monetária
- Cores destacadas durante interação

### Cliques e Navegação
- Sunburst: Clique para explorar camadas
- Filtros: Atualizam todos os gráficos em tempo real
- Exportação: Baixa dados filtrados em JSON

### Animações
- Transições suaves entre abas
- Efeitos hover nos cards
- Animação de carregamento

## 📈 Análises Oferecidas

### Estatísticas Descritivas
- Média, mediana, desvio padrão
- Máximo e mínimo por métrica
- Distribuição de valores

### Análises Comparativas
- Ranking de estados/regiões
- Índices de concentração
- Variabilidade de mercado

### Séries Temporais
- Evolução mensal de vendas
- Crescimento year-over-year
- Sazonalidade identificada

### Correlações
- Clientes vs Faturamento
- Pedidos vs Clientes
- Taxa de entrega vs Volume

## 🎯 Perguntas que o Dashboard Responde

1. **Qual é o estado/região com maior faturamento?** → Sudeste (São Paulo lidera)
2. **Como estão distribuídos os clientes geograficamente?** → Visualizado em pie chart
3. **Qual é a tendência de vendas ao longo do tempo?** → Análise Temporal mostra evolução
4. **Como as regiões se comparam em desempenho?** → Comparação Regional com múltiplos gráficos
5. **Qual é o padrão de crescimento?** → Análise Avançada com estatísticas
6. **Quais cidades/regiões têm potencial de crescimento?** → Insights automáticos
7. **Como é a taxa de sucesso de entrega por região?** → Métrica exibida em KPIs

## 🔄 Atualizar Dados

Para atualizar os dados da API/banco:

```bash
# Execute o script Python que gera os JSONs
python3 gerar_dados_vendas.py
python3 gerar_dados_vendas_avancado.py
```

Os arquivos JSON serão atualizados automaticamente.

## 📱 Mobile Responsiveness

- Layout adaptado para telas pequenas
- Toque em elementos interativos funciona normalmente
- Tabelas com scroll horizontal em mobile
- Gráficos mantêm qualidade em qualquer resolução

## 🐛 Troubleshooting

| Problema | Solução |
|----------|---------|
| "Dados não carregam" | Verifique se `dados_vendas_avancado.json` está no mesmo diretório |
| "Gráficos não aparecem" | Limpe cache (Ctrl+F5) e tente novamente |
| "Filtros não funcionam" | Abra console (F12) e verifique erros |
| "Página branca" | Verifique internet e se as CDNs estão acessíveis |

## 🔐 Segurança

- ✅ Sem requisições AJAX externas (exceto CDNs)
- ✅ Todos os dados são locais
- ✅ Sem armazenamento em servidor
- ✅ Dados exportados em JSON puro

## 📞 Suporte

Para questões sobre o dashboard, consulte:
- Documentação do schema: `docs/schema.md`
- GitHub: [repositório do projeto]
- Email: [contato]

---

**Versão**: 2.0 Avançado  
**Data**: 29/08/2026  
**Status**: ✅ Funcional e Otimizado  
**Desenvolvedor**: Copilot Dashboard Team  

### Changelog v2.0
- ✅ 6 novos tipos de gráficos
- ✅ Sistema de filtros avançado
- ✅ 5 abas temáticas
- ✅ 6 KPIs profissionais
- ✅ Análises estatísticas
- ✅ Exportação de dados
- ✅ Design responsivo melhorado
- ✅ Tooltips em todos os gráficos
- ✅ Insights automáticos
- ✅ Performance otimizada
