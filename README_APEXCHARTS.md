# 🚀 Dashboard ApexCharts - Versão Premium

Um dashboard empresarial **ultra-moderno** com **ApexCharts**, oferecendo visualizações incríveis e interatividade profissional para análise completa de vendas por estado e região.

## ⭐ Por que ApexCharts é Melhor?

| Aspecto | D3.js/Chart.js | ApexCharts |
|--------|---|---|
| **Curva Aprendizado** | Muito difícil | Muito fácil |
| **Animações** | Básicas | Suaves e modernas |
| **Interatividade** | Limitada | Excelente |
| **Responsividade** | Boa | Excelente |
| **Tooltips** | Simples | Sofisticados |
| **Documentação** | Complicada | Clara e completa |
| **Performance** | Varia | Otimizada |
| **Temas** | Manual | Automático |
| **Zoom/Scroll** | Complicado | Nativo |
| **Exportação** | Manual | Nativa (PNG, SVG, PDF, CSV) |

## 🎯 O Que Você Tem Agora

### 📊 12 Tipos de Gráficos ApexCharts

1. **Area Chart** - Faturamento por região com preenchimento gradiente
2. **Bar Chart** - Vendas comparativas com animação
3. **Pie Chart** - Distribuição de clientes
4. **Column Chart** - Comparação de múltiplas métricas
5. **Timeline/Area** - Evolução temporal com zoom
6. **Box Plot** - Top 10 meses
7. **Mixed Chart** - Dados mistos (pedidos + taxa)
8. **Radar Chart** - Métricas multidimensionais
9. **Scatter Plot** - Correlação Clientes vs Vendas
10. **Heatmap** - Matriz de Estados vs Métricas
11. **Funnel Chart** - Faturamento acumulado
12. **KPI Cards** - 6 métricas principais

### 5️⃣ Abas Temáticas

```
📈 VISÃO GERAL
├── 6 KPI Cards animados
├── Gráfico Area grande (faturamento)
├── Bar Chart (vendas por região)
└── Pie Chart (distribuição de clientes)

📊 DETALHES
├── Tabela ranking (27 estados)
└── Column Chart (comparação de métricas)

📅 TEMPORAL
├── Timeline com zoom interativo
├── Top 10 meses (bar chart)
└── Mixed chart (pedidos + taxa entrega)

⚖️ COMPARAÇÃO
├── Radar chart (5 regiões)
├── Scatter plot (correlação)
└── Heatmap (estados vs métricas)

🔬 AVANÇADO
├── Estatísticas calculadas
├── Insights automáticos
└── Funnel chart (acumulado)
```

## 🚀 Como Abrir (30 segundos)

### Opção 1: Live Server ⭐ (Recomendado)
```bash
1. VS Code → Extensões → Instale "Live Server"
2. Clique direito: dashboard_apexcharts.html
3. "Open with Live Server"
✅ Pronto!
```

### Opção 2: Python
```bash
cd /workspaces/202608029_aula03_dataviz
python3 -m http.server 8000
# Acesse: http://localhost:8000/dashboard_apexcharts.html
```

### Opção 3: Direto no Navegador
```bash
Clique duplo em: dashboard_apexcharts.html
```

## 🎨 Recursos ApexCharts

### ✨ Animações Suaves
- Gráficos animam ao carregar
- Transições fluidas entre abas
- Hover effects elegantes

### 🎯 Interatividade
- **Zoom**: Clique e arraste em gráficos de timeline
- **Seleção**: Clique em legendas para toggle
- **Detalhes**: Hover mostra valores precisos
- **Expansão**: Clique para zoom em dados

### 📊 Formatação Inteligente
- Valores monetários automáticos (R$, M, k)
- Datas formatadas em português
- Percentuais com símbolo %
- Números com separador de milhar

### 🎨 Design Profissional
- Gradientes modernos azul
- Cores de região consistentes
- Sombreamento dinâmico
- Componentes com estado hover

### ⚙️ Funcionalidades Nativas ApexCharts
- Exportação PNG/SVG/PDF (botão no gráfico)
- Download de dados (CSV)
- Zoom automático em timeline
- Redimensionamento responsivo

## 📥 Exportações

### JSON Export
```
Clique em "📥 Exportar JSON"
↓
Baixa: vendas_YYYY-MM-DD.json
↓
Contém dados filtrados com estrutura completa
```

### CSV Export
```
Clique em "📥 Exportar CSV"
↓
Baixa: vendas_YYYY-MM-DD.csv
↓
Abra em Excel ou Google Sheets
```

### PNG/SVG/PDF (Nativo)
```
Clique no ícone ⋯ de qualquer gráfico
↓
Selecione "Download as PNG/SVG/PDF"
↓
Arquivo salvo automaticamente
```

## 🎛️ Filtros

```
🔍 Região: [Dropdown ▼]
   • Todas as Regiões (padrão)
   • Norte
   • Nordeste
   • Centro-Oeste
   • Sudeste
   • Sul

✅ Atualiza TODOS os 12 gráficos em tempo real!
```

## 📊 6 KPI Cards Animados

```
┌────────────────┐
│ 💰 Faturamento │ → Bloco azul (primary)
│  R$ 16.008M    │
└────────────────┘

┌────────────────┐
│ 📦 Pedidos     │ → Bloco verde (success)
│  103.886       │
└────────────────┘

┌────────────────┐
│ 👥 Clientes    │ → Bloco roxo (purple)
│  50.138        │
└────────────────┘

┌────────────────┐
│ 🎯 Ticket      │ → Bloco laranja (warning)
│  R$ 154.23     │
└────────────────┘

┌────────────────┐
│ 🏙️ Cidades     │ → Bloco cyan (cyan)
│  4.119         │
└────────────────┘

┌────────────────┐
│ ✅ Taxa        │ → Bloco vermelho (danger)
│  94.2%         │
└────────────────┘
```

**Animação**: Hover → Translada para cima com sombra aumentada

## 🔍 Exemplos de Uso

### Análise 1: Qual é o melhor estado?
```
1. Abra o dashboard
2. Vá para aba "📊 Detalhes"
3. Veja tabela ranking
4. Resposta: SP com R$ 5.998.227 (1º lugar)
```

### Análise 2: Qual região cresceu mais?
```
1. Abra aba "📅 Temporal"
2. Veja o gráfico timeline com zoom
3. Compare linhas de cada região
4. Resposta: Sudeste mostrado em salmão
```

### Análise 3: Existe correlação?
```
1. Abra aba "⚖️ Comparação"
2. Veja o Scatter Plot
3. Observe a distribuição de pontos
4. Resposta: Existe correlação (pontos formam tendência)
```

### Análise 4: Qual mês foi melhor?
```
1. Abra aba "📅 Temporal"
2. Veja "Top 10 Meses"
3. Leia a barra mais alta
4. Resposta: Varie conforme dados
```

### Análise 5: Dados estatísticos
```
1. Abra aba "🔬 Avançado"
2. Veja "Análise Estatística"
3. Leia correlação, variação, desvio padrão
4. Resposta: Valores calculados automaticamente
```

## 🌟 Vantagens ApexCharts vs Versão Anterior

| Recurso | V1.0 (Chart.js) | V2.0 (ApexCharts) |
|---------|---|---|
| Tipos de gráficos | 9 | 12 |
| Animações | Básicas | Sofisticadas |
| Zoom | Não | Sim (timeline) |
| Exportação nativa | Não | Sim (PNG/SVG/PDF/CSV) |
| Tooltip customizado | Não | Sim |
| Responsividade | Boa | Excelente |
| Performance | Boa | Excelente |
| Curva aprendizado | Média | Fácil |
| Documentação | Ok | Excelente |
| Interatividade | Boa | Muito Boa |

## 🛠️ Tecnologias

- **ApexCharts 3.45** - Visualizações modernas
- **HTML5** - Estrutura
- **CSS3** - Estilização (Grid, Flexbox, Gradients)
- **JavaScript ES6** - Interatividade
- **Google Fonts (Inter)** - Tipografia moderna

## 📱 Responsividade

```
Desktop (>1200px):    [Gráfico] [Gráfico]
Tablet (768-1200px): [Gráfico]
                      [Gráfico]
Mobile (<768px):     [Gráfico fullwidth]
```

Todos os gráficos se adaptam perfeitamente!

## 🎯 Compatibilidade

✅ Chrome/Chromium (recomendado)
✅ Firefox
✅ Safari
✅ Edge
⚠️ IE11 (não testado)

## 📚 Documentação Arquivo JSON

```json
{
  "regioes": {
    "Sudeste": {
      "pedidos": 43622,
      "vendas": 10340831.46,
      "clientes": 41745,
      "cidades": 1852,
      "taxa_entrega": 97.2,
      "estados": [...]
    },
    ...
  },
  "estados_ranking": [...],
  "timeline": {...},
  "total_geral": {...},
  "atualizacao": "2026-08-29T14:02:00"
}
```

## 🐛 Troubleshooting

| Problema | Solução |
|----------|---------|
| Gráficos não carregam | Abra console (F12), verifique erros |
| Dados não aparecem | Confirme `dados_vendas_avancado.json` existe |
| Filtro não funciona | Recarregue (Ctrl+F5) |
| Tooltips não aparecem | Hover devagar sobre gráficos |
| Responsivo quebrado | Redimensione janela |

## 📞 Recursos

- **Arquivo HTML**: `dashboard_apexcharts.html` (50 KB)
- **Dados JSON**: `dados_vendas_avancado.json` (55 KB)
- **Documentação**: Este arquivo
- **Versões Anteriores**: 
  - `dashboard.html` (D3.js v1.0)
  - `dashboard_avancado.html` (Chart.js v2.0)

## ✅ Checklist

☑️ 12 gráficos ApexCharts
☑️ 6 KPI cards animados
☑️ 5 abas temáticas
☑️ Filtros dinâmicos
☑️ Tabela ranking (27 estados)
☑️ Análise estatística
☑️ Insights automáticos
☑️ Exportação (JSON, CSV)
☑️ Zoom em timeline
☑️ Design responsivo
☑️ Performance otimizada
☑️ Documentação completa

## 🎉 Versão Final

**Versão**: 3.0 ApexCharts Premium  
**Data**: 29/08/2026  
**Status**: ✅ Pronto para Produção

### Changelog v3.0
- ✨ ApexCharts (12 gráficos modernos)
- ✨ Animações sofisticadas
- ✨ Zoom interativo em timeline
- ✨ Exportação nativa PNG/SVG/PDF
- ✨ Tooltips customizados
- ✨ Design ultra-moderno
- ✨ Performance superior
- ✨ Responsividade perfeita
- ✨ 8 Insights automáticos

---

**Aproveite! 🚀**
