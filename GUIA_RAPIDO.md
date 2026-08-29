# 🎯 GUIA RÁPIDO - Dashboard Avançado v2.0

## 🚀 COMEÇAR AGORA (30 segundos)

### Option 1: Live Server (Recomendado) ⭐
```
1. VS Code → Extensões → Instale "Live Server"
2. Clique direito em: dashboard_avancado.html
3. "Open with Live Server"
✅ Pronto! Dashboard abre automaticamente
```

### Option 2: Python (Sem instalações)
```bash
cd /workspaces/202608029_aula03_dataviz
python3 -m http.server 8000
# Abra: http://localhost:8000/dashboard_avancado.html
```

### Option 3: Navegador Direto
```
Clique duplo em: dashboard_avancado.html
✅ Abre direto no navegador
```

---

## 📊 O QUE VOCÊ VÊ?

### 🎨 Layout Principal
```
┌─────────────────────────────────────────┐
│  📊 Dashboard Avançado de Vendas        │ ← Header roxo
├─────────────────────────────────────────┤
│ 🔍 Filtro Região | 📅 Período | 📥 Exp │ ← Controles
├─────────────────────────────────────────┤
│ 📈 | 📊 | 📅 | ⚖️ | 🔬                  │ ← Abas
├─────────────────────────────────────────┤
│                                         │
│  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐  │
│  │ R$M  │ │ Ped  │ │ Cli  │ │Ticket│  │ ← KPIs
│  └──────┘ └──────┘ └──────┘ └──────┘  │
│                                         │
│  ┌───────────────────────────────────┐  │
│  │    Gráfico Sunburst Grande        │  │ ← Visualização
│  └───────────────────────────────────┘  │
│                                         │
│  ┌─────────────┐ ┌─────────────────┐   │
│  │ Bar Chart   │ │ Pie Chart       │   │
│  └─────────────┘ └─────────────────┘   │
│                                         │
└─────────────────────────────────────────┘
```

---

## 🎛️ FILTROS

### Filtro de Região
```
🔍 Filtrar por Região: [Dropdown ▼]
  • Todas as Regiões (padrão)
  • Norte
  • Nordeste
  • Centro-Oeste
  • Sudeste
  • Sul
```
**Efeito**: Todos os gráficos atualizam instantaneamente!

### Filtro de Período
```
📅 Período: [Dropdown ▼]
  • Todos os Períodos (padrão)
  • Últimos 3 Meses
  • Últimos 6 Meses
  • Últimos 12 Meses
```

### Exportar Dados
```
📥 Exportar Dados [Botão Roxo]
  → Baixa arquivo JSON com dados filtrados
  → Nomeado: vendas_YYYY-MM-DD.json
```

---

## 📑 ABAS (5 Seções)

### 1️⃣ VISÃO GERAL (Padrão)
```
O que mostra:
├── 6 KPI Cards (coloridos)
│   ├── Faturamento (azul)
│   ├── Pedidos (verde)
│   ├── Clientes (cyan)
│   ├── Ticket Médio (laranja)
│   ├── Cidades (vermelho)
│   └── Taxa de Entrega (roxo)
│
├── Sunburst Chart (grande)
│   └── Hierarquia: Brasil → Região → Estado
│
└── Bar + Pie Charts (lado a lado)
    ├── Barras coloridas por região
    └── Pizza com % de clientes
```

**Interatividade**:
- Hover em qualquer elemento → tooltip com detalhes
- Clique no Sunburst → zoom em regiões

---

### 2️⃣ DETALHES POR ESTADO
```
O que mostra:
├── Tabela Ranking (todos os 27 estados)
│   ├── Posição (🥇 🥈 🥉...)
│   ├── Estado
│   ├── Região
│   ├── Faturamento (R$)
│   ├── Pedidos (#)
│   ├── Clientes (#)
│   ├── Ticket Médio (R$)
│   └── Taxa de Entrega (%)
│
└── Ordenado por Faturamento (maior para menor)
```

**Cores**:
- Regiões com badges coloridas
- Taxa de entrega em verde

**Top 3**:
```
🥇 SP - R$ 5.998.227
🥈 RJ - R$ 2.144.380
🥉 MG - R$ 1.872.257
```

---

### 3️⃣ ANÁLISE TEMPORAL
```
O que mostra:
├── Line Chart (evolução mensal)
│   └── 25 meses de dados
│
├── Top 10 Meses (ranking)
│   └── Listar mês com maior faturamento
│
└── Gráfico de Crescimento MoM
    └── Month-over-Month crescimento
```

**Tendências Identificadas**:
- Sazonalidade
- Padrões de crescimento
- Picos de vendas

---

### 4️⃣ COMPARAÇÃO REGIONAL
```
O que mostra:
├── Heatmap (Estados vs Regiões)
│   └── Matriz de intensidade
│
├── Scatter Plot (Clientes vs Vendas)
│   └── Correlação visual
│
└── Radar Chart (métricas multidimensionais)
    └── Comparação das 5 regiões
```

**Análises**:
- Qual estado tem mais clientes?
- Qual região tem melhor eficiência?
- Existe correlação linear?

---

### 5️⃣ ANÁLISE AVANÇADA
```
O que mostra:
├── Estatísticas Calculadas
│   ├── Correlação Clientes vs Vendas
│   ├── Índice de Concentração
│   ├── Coeficiente de Variação
│   └── Desvio Padrão de Vendas
│
└── Insights Automáticos
    ├── 🏆 Estado top performer
    ├── 📍 Total de regiões
    ├── 👥 Maior mercado
    └── 🎯 Ticket médio geral
```

---

## 🎨 CORES POR REGIÃO

```
┌─────────────────────────────────────────┐
│ 🔴 NORTE        → Vermelho (#FF6B6B)   │
│ 🔵 NORDESTE     → Teal (#4ECDC4)       │
│ 🟡 CENTRO-OESTE → Azul Claro (#45B7D1)│
│ 🟠 SUDESTE      → Salmão (#FFA07A)     │
│ 🟢 SUL          → Verde Água (#98D8C8) │
└─────────────────────────────────────────┘
```

Cores são **CONSISTENTES** em todos os gráficos!

---

## 📱 RESPONSIVIDADE

### Desktop (1200px+)
```
[Gráfico Esquerda] [Gráfico Direita]
```

### Tablet (768px - 1200px)
```
[Gráfico]
[Gráfico]
```

### Mobile (<768px)
```
[Gráfico Fullwidth]
```

**Totalmente funcional em qualquer tamanho!**

---

## 💡 DICAS DE USO

### 1. Combinar Filtros
```
Selecione: Sudeste + Últimos 6 meses
→ Ver performance apenas dessa região e período
→ Todos os gráficos se ajustam!
```

### 2. Explorar o Sunburst
```
Passe o mouse → vê tooltip com valores
Clique em região → zoom interativo
Clique de novo → volta ao nível anterior
```

### 3. Comparar Estados
```
Ir para aba "Detalhes por Estado"
→ Tabela com ranking de todos os 27
→ Ordene clicando na coluna (em implementação)
```

### 4. Exportar para Excel/Sheets
```
Clique "📥 Exportar Dados"
→ Baixa dados_YYYY-MM-DD.json
→ Abra em qualquer aplicação que suporte JSON
→ Ou converta para CSV/Excel
```

### 5. Analisar Tendências
```
Ir para "📅 Análise Temporal"
→ Ver gráfico de linhas com evolução
→ Identificar sazonalidade
→ Comparar regiões ao longo do tempo
```

---

## 🔍 PERGUNTAS QUE VOCÊ PODE RESPONDER

```
1. "Qual é o estado com maior vendas?"
   → Tabela "Detalhes por Estado" - 1º lugar
   → Resposta: SP com R$ 5.998.227

2. "Qual região cresce mais?"
   → Aba "Análise Temporal" - Line chart
   → Veja qual linha sobe mais

3. "Tem correlação entre clientes e vendas?"
   → Aba "Comparação Regional" - Scatter plot
   → Veja se pontos formam linha reta

4. "Como está a taxa de entrega?"
   → KPI Card "Taxa de Entrega" no topo
   → Atualmente: ~94% em média

5. "Quais cidades mais vendem?"
   → Dados estão no JSON exportado
   → Use Excel para análise adicional

6. "Qual mês teve melhor faturamento?"
   → Aba "Análise Temporal" - Top 10 Meses
   → Lista ordenada de melhor para pior
```

---

## ⚙️ REQUISITOS

✅ Navegador Moderno
- Chrome/Chromium (melhor)
- Firefox
- Safari
- Edge

✅ Arquivos Necessários
- `dashboard_avancado.html` (este arquivo)
- `dados_vendas_avancado.json` (mesma pasta)

✅ Não precisa de:
- Servidor backend
- Banco de dados
- Internet (tudo é local)
- Instalações adicionais

---

## 🐛 TROUBLESHOOTING

### Gráficos não aparecem
```
Solução: Limpe cache
- Pressione: Ctrl + F5 (ou Cmd + Shift + R no Mac)
- Recarregue a página
```

### Erro "Dados não carregam"
```
Solução: Verifique arquivos
- dados_vendas_avancado.json está na mesma pasta?
- Abra console: F12 → Console → veja erro
```

### Filtros não funcionam
```
Solução: JavaScript desabilitado?
- Verifique se JS está ativado no navegador
- Tente outro navegador
```

### Tooltip fica piscando
```
Solução: Movimento lento do mouse
- Problema normal de hover
- Tente passar mais devagar
```

---

## 📞 CONTATO & DOCS

- **Documentação Completa**: `README_DASHBOARD_V2.md`
- **Schema do Banco**: `docs/schema.md`
- **Versão Legado**: `dashboard.html`
- **Dados Simples**: `dados_vendas.json`

---

## ✅ CHECKLIST ANTES DE USAR

- [ ] Arquivo `dashboard_avancado.html` existe?
- [ ] Arquivo `dados_vendas_avancado.json` existe (mesma pasta)?
- [ ] Navegador está atualizado?
- [ ] JavaScript está habilitado?
- [ ] Conexão de internet está OK (para CDNs)?

---

**Versão**: 2.0 Avançado  
**Status**: ✅ Pronto para Uso  
**Data**: 29/08/2026

**Aproveite! 🚀**
