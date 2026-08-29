# 📊 Dashboard de Vendas por Estado e Região

Um dashboard interativo em HTML5 e D3.js que fornece análise demográfica de vendas por estado e região do Brasil, com funcionalidade de drill down.

## 🎯 Funcionalidades

### 1. **Visão Geral**
- Métricas consolidadas:
  - Faturamento total (em milhões)
  - Total de pedidos
  - Total de clientes
  - Ticket médio
- **Gráfico Sunburst**: Visualização hierárquica de vendas (Brasil → Região → Estado)
  - Tamanho dos segmentos proporcional ao faturamento
  - Cores diferenciadas por região
  - Hover com tooltip detalhado

### 2. **Drill Down Interativo**
- Navegação hierárquica entre níveis:
  - **Nível 1**: Regiões do Brasil (5 regiões)
  - **Nível 2**: Estados por região (27 estados)
  - **Nível 3**: Cidades por estado (4.119 cidades)
- **Treemap** para visualização de proporções
- Breadcrumb para navegação fácil
- Detalhes dinâmicos:
  - Faturamento
  - Número de pedidos
  - Quantidade de clientes
  - Ticket médio

### 3. **Comparação Regional**
- **Gráfico de Barras**: Vendas por região
  - Ordenadas por valor decrescente
  - Cores consistentes com outras visualizações
  - Escala em milhões
- **Gráfico de Pizza**: Distribuição de clientes
  - Percentuais por região
  - Valores absolutos em tooltip

### 4. **Detalhes Completos**
- Tabela ranking com todos os estados
- Ordenado por faturamento decrescente
- Colunas:
  - Região
  - Estado
  - Faturamento (R$)
  - Quantidade de pedidos
  - Quantidade de clientes
  - Ticket médio

## 📁 Arquivos Necessários

```
/workspaces/202608029_aula03_dataviz/
├── dashboard.html          # Dashboard principal
├── dados_vendas.json       # Dados extraídos do banco
└── README_DASHBOARD.md     # Este arquivo
```

## 🚀 Como Usar

### Opção 1: Abrir Localmente
1. Certifique-se que os arquivos estão no mesmo diretório:
   - `dashboard.html`
   - `dados_vendas.json`

2. Abra o arquivo `dashboard.html` em um navegador moderno (Chrome, Firefox, Edge, Safari)

### Opção 2: Usar com Live Server (VS Code)
1. Instale a extensão "Live Server" no VS Code
2. Clique com botão direito em `dashboard.html`
3. Selecione "Open with Live Server"

### Opção 3: Servir com Python
```bash
# Python 3
python3 -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

Acesse: `http://localhost:8000/dashboard.html`

## 🎨 Recursos de Interação

### Sunburst (Visão Geral)
- **Hover**: Exibe tooltip com nome, vendas e detalhes
- **Zoom**: Possibilidade de explorar níveis

### Treemap (Drill Down)
- **Clique em região**: Expande para mostrar estados
- **Clique em estado**: Expande para mostrar cidades
- **Breadcrumb**: Navegar rapidamente entre níveis
- **Cores**: Consistentes com a região pai

### Gráficos Comparativos
- **Hover**: Exibe tooltip com valores precisos
- **Respositvo**: Adapta-se ao tamanho da tela

## 📊 Regiões e Estados

### Região Norte (7 estados)
AC, AP, AM, PA, RO, RR, TO
- Faturamento: R$ 414.622,35

### Região Nordeste (9 estados)
AL, BA, CE, MA, PB, PE, PI, RN, SE
- Faturamento: R$ 1.898.479,44

### Região Centro-Oeste (4 estados)
DF, GO, MT, MS
- Faturamento: R$ 1.029.797,52

### Região Sudeste (4 estados) ⭐
ES, MG, RJ, SP
- Faturamento: R$ 10.340.831,46
- **Destaque**: São Paulo lidera com R$ 5.998.226,96

### Região Sul (3 estados)
PR, RS, SC
- Faturamento: R$ 2.325.141,35

## 🎯 Perguntas que o Dashboard Responde

1. **Qual região tem maior faturamento?**
   - Sudeste (63% do total)

2. **Como estão distribuídos os clientes?**
   - Visualizável no gráfico de pizza

3. **Qual é o ticket médio por estado?**
   - Mostrado na tabela de detalhes

4. **Como os estados de uma região se comparam?**
   - Use o drill down para explorar

5. **Qual é a correlação entre clientes e vendas?**
   - Comparável nos gráficos

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura
- **CSS3**: Estilização e gradientes
- **D3.js v7**: Visualizações de dados
- **JavaScript ES6**: Interatividade

## 📱 Compatibilidade

- ✅ Chrome/Chromium (recomendado)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ⚠️ IE11 (não testado)

## 🎨 Paleta de Cores

- **Norte**: Vermelho (#FF6B6B)
- **Nordeste**: Teal (#4ECDC4)
- **Centro-Oeste**: Azul Claro (#45B7D1)
- **Sudeste**: Salmão (#FFA07A)
- **Sul**: Verde Água (#98D8C8)

## 📝 Notas Importantes

1. O arquivo `dados_vendas.json` é gerado automaticamente do banco de dados
2. Para atualizar os dados, execute o script Python que gera o JSON
3. O dashboard é completamente client-side (não requer servidor)
4. A hierarquia de drill down é: Região → Estado → Cidade

## 🔄 Atualizando os Dados

Para atualizar os dados de vendas:

```bash
python3 scripts/gerar_dados_vendas.py
```

Ou execute o comando Python direto que gera o `dados_vendas.json`.

## 🐛 Troubleshooting

### "Erro ao carregar dados"
- Verifique se `dados_vendas.json` está no mesmo diretório
- Verifique o console (F12) para mensagens de erro

### Gráficos não aparecem
- Limpe o cache do navegador (Ctrl+F5)
- Verifique se está acessando via HTTP (não file://)
- Use Live Server ou servidor Python

### Drill Down não funciona
- Clique na área colorida (não no rótulo)
- Verifique o breadcrumb para confirmar o nível

## 📧 Suporte

Para mais informações ou reportar problemas, entre em contato com o desenvolvedor.

---

**Versão**: 1.0  
**Data**: 29/08/2026  
**Status**: Funcionando ✅
