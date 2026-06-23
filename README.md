# 📱 Análise de Mercado para Aplicativos Móveis

## 🚀 Sobre o Projeto

Este projeto realiza uma análise exploratória de dados de aplicativos da **Google Play Store** e da **Apple App Store** com o objetivo de identificar quais categorias de aplicativos gratuitos possuem maior potencial de atrair usuários e gerar receita através de anúncios.

A proposta simula o cenário de uma empresa que desenvolve aplicativos gratuitos para Android e iOS, cuja principal fonte de receita é a monetização por anúncios.

---

## 🎯 Objetivo

Identificar perfis de aplicativos que apresentem potencial de sucesso simultaneamente na Google Play Store e na Apple App Store, utilizando dados reais de mercado para apoiar a tomada de decisão.

---

## 📂 Bases de Dados

Os dados utilizados foram obtidos no Kaggle:

* Google Play Store Dataset
* Apple App Store Dataset

As bases contêm informações sobre:

* Categoria
* Avaliação dos usuários
* Número de avaliações
* Instalações
* Preço
* Gênero
* Classificação etária
* Versão
* Entre outras métricas

---

## 🛠️ Tecnologias Utilizadas

* 🐍 Python
* 📓 Jupyter Notebook
* 📂 CSV
* 📊 Análise Exploratória de Dados (EDA)

---

## 🔍 Etapas do Projeto

### 1️⃣ Importação dos Dados

* Leitura dos arquivos CSV
* Separação de cabeçalhos e registros
* Exploração inicial das bases

### 2️⃣ Limpeza dos Dados

* Remoção de registros com erros
* Identificação de inconsistências
* Exclusão de aplicativos duplicados
* Seleção da versão mais relevante dos registros duplicados com base na quantidade de avaliações

### 3️⃣ Filtragem dos Dados

Foram mantidos apenas:

✅ Aplicativos gratuitos

✅ Aplicativos em inglês

✅ Registros únicos

---

## 📊 Análise de Mercado

Foi realizada uma análise das categorias mais populares em ambas as plataformas.

### Apple App Store

Principais categorias identificadas:

* 🎮 Games (58,16%)
* 🎬 Entertainment (7,88%)
* 📷 Photo & Video (4,97%)
* 🎓 Education (3,66%)
* 🌐 Social Networking (3,29%)

Observação:

A App Store apresenta predominância de aplicativos voltados para entretenimento e lazer.

---

### Google Play Store

Principais categorias identificadas:

* 👨‍👩‍👧 Family
* 🛠️ Tools
* 🎬 Entertainment
* 🎓 Education
* 💼 Business
* 📈 Productivity

Observação:

A Google Play apresenta uma distribuição mais equilibrada entre aplicativos de entretenimento e aplicativos utilitários.

---

## 💡 Principais Insights

Após a análise das duas plataformas, observou-se que a categoria **Books & Reference** apresenta potencial interessante:

* Alta demanda de usuários
* Menor concorrência em comparação com jogos
* Possibilidade de monetização por anúncios
* Potencial para funcionalidades adicionais

Exemplos de recursos sugeridos:

* 📖 Leitura digital
* 🎧 Audiobooks
* 📅 Citações diárias
* 📝 Quizzes
* 💬 Fóruns de discussão

A recomendação final foi desenvolver um aplicativo baseado em livros populares, agregando funcionalidades adicionais que aumentem o engajamento dos usuários.

---

## 📈 Resultados

* Limpeza e preparação de mais de 10 mil registros da Google Play Store.
* Identificação de padrões de mercado em duas plataformas distintas.
* Comparação entre oferta e demanda de categorias de aplicativos.
* Definição de uma estratégia baseada em dados para desenvolvimento de novos produtos digitais.

---

## 📚 Competências Desenvolvidas

* Análise Exploratória de Dados (EDA)
* Limpeza e Tratamento de Dados
* Manipulação de Listas e Dicionários
* Leitura de Arquivos CSV
* Estruturas de Controle em Python
* Análise de Mercado
* Tomada de Decisão Baseada em Dados

---

## 👨‍💻 Autor

Projeto desenvolvido por AlderARS como parte dos estudos em Python, Análise de Dados e Ciência de Dados.
