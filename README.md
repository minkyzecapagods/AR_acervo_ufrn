# 📚 AR\_acervo\_ufrn

Análise de Redes aplicada ao acervo da UFRN: construção, métricas e visualizações de grafos para identificar padrões de empréstimo, comunidades temáticas e nós centrais.

---

## 🚀 Sobre o projeto

Este repositório contém notebooks, dados e scripts que:

✅ Constroem grafos a partir de dados de empréstimos e exemplares
✅ Calculam métricas de redes (centralidades, modularidade, clustering)
✅ Detectam comunidades (Louvain, Gephi)
✅ Geram visualizações interativas com Pyvis e exportações para SigmaJS (Gephi)

---

## 📂 Estrutura

```
AR_acervo_ufrn/
├── _config.yml
├── data
│   ├── acervo-exemplares.csv
│   ├── emprestimos.csv
│   └── exemplares.csv
├── dicionario
│   ├── acervo-exemplares-dicionario.pdf
│   ├── emprestimos-dicionario.pdf
│   └── exemplares--dicionario.pdf
├── index.html
├── livros_network.html
├── notebook
│   └── AR_acervo_ufrn.ipynb
└── README.md
```

---

## 🛠 Pré-requisitos

* Python 3.8+
* Instale as dependências com:

```bash
pip install networkx igraph pandas numpy matplotlib seaborn pyvis python-louvain
```

---

## 💻 Como usar

1. **Clone o repositório**

   ```bash
   git clone https://github.com/minkyzecapagods/AR_acervo_ufrn.git
   cd AR_acervo_ufrn
   ```

2. **Execute os notebooks em ordem** (`notebook/`):

   * 01\_dados.ipynb → prepara dados e constrói grafos
   * 02\_analise\_metrica.ipynb → calcula métricas
   * 03\_comunidades\_visual.ipynb → detecta comunidades e visualiza

3. **Pyvis**

   * Gere a rede interativa em `pyvis/visualizacao_pyvis.ipynb`
   * Exporte como HTML e publique com GitHub Pages:

     * Acesse *Settings → Pages* e aponte para a pasta `/pyvis`

4. **Gephi**

   * Importe `data/grafo_filtrado.gexf` no Gephi
   * Execute layout, modularidade e exporte com SigmaJS
   * Coloque o HTML em `/gephi` para deploy no GitHub Pages

5. (Opcional) **Streamlit**

   * Crie uma app com filtros interativos
   * Faça deploy no [Streamlit Cloud](https://streamlit.io/cloud)

---

## 📊 Métricas calculadas

* **Centralidades**: Degree, Betweenness, Closeness, Eigenvector
* **Clustering**: global e local
* **Assortatividade**: grau e assuntos
* **Distribuição de grau**: ajuste power-law
* **Modularidade**: comunidades com Louvain (valores \~0.9 = forte estrutura modular)

---

## 🌐 Visualizações

* 🔵 **Pyvis** – grafo interativo com cores por comunidade
---
