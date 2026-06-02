# 📱 Mobile App Ads Analysis

## 📖 Sobre o Projeto

Neste projeto, assumimos o papel de analistas de dados em uma empresa que desenvolve aplicativos móveis gratuitos para Android e iOS.

Como a principal fonte de receita da empresa é a exibição de anúncios dentro dos aplicativos, o objetivo deste estudo é identificar quais tipos de aplicativos possuem maior potencial para atrair usuários e, consequentemente, gerar mais receita.

Para isso, foram analisados conjuntos de dados da App Store e do Google Play Store, buscando encontrar perfis de aplicativos que apresentem potencial de sucesso em ambas as plataformas.

---

## 🎯 Objetivo de Negócio

Responder à seguinte pergunta:

> Qual tipo de aplicativo gratuito possui maior potencial de atrair usuários e gerar receita por meio de anúncios tanto na App Store quanto no Google Play?

---

## 🗂️ Bases de Dados

Os dados utilizados neste projeto contêm informações sobre milhares de aplicativos disponíveis nas lojas:

* Google Play Store
* Apple App Store

As bases incluem informações como:

* Nome do aplicativo
* Categoria
* Gênero
* Número de avaliações
* Quantidade de instalações
* Classificação dos usuários
* Tipo do aplicativo (gratuito ou pago)

---

# 🧹 Limpeza e Preparação dos Dados

## 1. Identificação de Duplicatas

O primeiro passo foi verificar a existência de registros duplicados.

Duplicatas podem gerar distorções nas análises, uma vez que um mesmo aplicativo pode ser contabilizado mais de uma vez.

Para identificar essas ocorrências, foi desenvolvida uma função que analisa os nomes dos aplicativos dentro da estrutura de dados.

---

## 2. Remoção Inteligente de Duplicatas

Foi observado que alguns aplicativos possuíam múltiplos registros com pequenas diferenças na coluna **Reviews**.

Exemplo:

| Aplicativo | Reviews  |
| ---------- | -------- |
| Instagram  | 66577446 |
| Instagram  | 66577313 |

Ao invés de remover registros aleatoriamente, foi adotada a seguinte regra:

✅ Manter o registro com o maior número de avaliações.

❌ Excluir os demais registros duplicados.

Essa abordagem aumenta a probabilidade de preservar a versão mais atualizada do aplicativo.

---

## 3. Seleção de Valores Únicos

Após a remoção das duplicatas, foi criada uma nova base contendo apenas registros únicos para garantir maior consistência nas análises.

---

## 4. Filtragem de Aplicativos em Inglês

Como o objetivo do estudo é analisar aplicativos voltados para mercados de língua inglesa, foi necessário remover aplicativos destinados a outros idiomas.

Exemplos:

* 爱奇艺PPS
* 网易新闻
* 漫画道场

Para isso foi utilizada uma função baseada na tabela ASCII.

### Critério Utilizado

Caracteres pertencentes ao conjunto ASCII padrão possuem códigos entre:

0 e 127

Foi estabelecida uma tolerância de até **3 caracteres especiais por nome de aplicativo**, evitando a exclusão indevida de aplicativos que utilizam emojis ou símbolos ocasionais.

---

## 5. Seleção de Aplicativos Gratuitos

Como o modelo de negócio da empresa depende de publicidade, apenas aplicativos gratuitos foram mantidos na análise.

Aplicativos pagos foram removidos da base de dados.

---

# 📊 Análise Exploratória

## Visão Geral da App Store

Entre os aplicativos gratuitos em inglês:

| Categoria         | Participação |
| ----------------- | ------------ |
| Games             | 58,16%       |
| Entertainment     | ~8%          |
| Photo & Video     | ~5%          |
| Education         | 3,66%        |
| Social Networking | 3,29%        |

### Insight

A App Store apresenta forte concentração de aplicativos voltados para entretenimento:

* Jogos
* Música
* Esportes
* Redes Sociais
* Fotos e Vídeos

Já aplicativos voltados para produtividade e utilidade possuem menor oferta.

---

## Visão Geral do Google Play

O Google Play apresenta uma distribuição mais equilibrada entre:

* Ferramentas
* Negócios
* Produtividade
* Estilo de Vida
* Família
* Jogos

Embora a categoria Família represente grande parcela dos aplicativos, boa parte dela é composta por jogos infantis.

### Insight

O Google Play possui um ecossistema mais diversificado entre entretenimento e aplicativos utilitários.

---

# 📈 Aplicativos com Maior Potencial de Usuários

## App Store

Como não existe uma coluna específica de instalações na base da App Store, foi utilizado o número de avaliações como indicador aproximado de popularidade.

### Categorias com maiores médias de avaliações

* Navigation
* Reference
* Social Networking

---

## Google Play

### Categorias com maiores médias de instalações

* Communication
* Video Players
* Social
* Productivity
* Photography
* Game
* Travel & Local
* Entertainment
* Books & Reference

---

# 🔎 Análise Aprofundada

## Navigation (App Store)

Apesar da alta média de avaliações, a categoria é fortemente dominada por:

* Google Maps
* Waze

Esses aplicativos concentram grande parte da demanda, tornando o mercado altamente competitivo.

### Conclusão

❌ Baixo potencial para novos entrantes.

---

## Reference (App Store)

A categoria apresenta média elevada de avaliações impulsionada por aplicativos como:

* Bible
* Dictionary.com

Mesmo assim, o nicho demonstra oportunidades interessantes.

### Possíveis ideias

Transformar livros populares em aplicativos com recursos adicionais:

* Citações diárias
* Audiobooks
* Quizzes
* Fóruns de discussão
* Dicionário integrado

### Conclusão

✅ Mercado promissor.

---

## Social Networking (App Store)

A média inicial era fortemente influenciada por grandes plataformas.

| Cenário       | Média de Avaliações |
| ------------- | ------------------- |
| Com mega apps | 71.500              |
| Sem mega apps | 13.900              |

### Conclusão

⚠️ Mercado atrativo, porém extremamente competitivo.

---

## Communication (Google Play)

A categoria apresenta números impressionantes de instalações.

| Cenário       | Média de Instalações |
| ------------- | -------------------- |
| Com mega apps | 914.600.000          |
| Sem mega apps | 3.600.000            |

Os resultados são fortemente influenciados por:

* WhatsApp
* Facebook Messenger
* Skype
* Gmail
* Chrome

### Conclusão

⚠️ Mercado dominado por grandes empresas.

---

## Books & Reference (Google Play)

Média de instalações:

**8.767.811 downloads**

O segmento inclui:

* Leitores de e-books
* Bibliotecas digitais
* Dicionários
* Materiais educacionais
* Livros religiosos

Apesar da existência de alguns aplicativos extremamente populares, o mercado ainda apresenta espaço para novos produtos.

### Oportunidades identificadas

Criar aplicativos baseados em livros populares adicionando funcionalidades extras:

* Versão em áudio
* Quizzes
* Fóruns
* Recomendações personalizadas
* Citações diárias

### Conclusão

✅ Categoria com alto potencial em ambas as plataformas.

---

# 🎯 Conclusão Final

Após analisar os dados da App Store e do Google Play, identificamos que a categoria **Books & Reference** apresenta o melhor equilíbrio entre popularidade e nível de concorrência.

A recomendação é desenvolver um aplicativo baseado em um livro popular, agregando funcionalidades que diferenciem o produto das bibliotecas digitais tradicionais.

Possíveis diferenciais:

* Audiobooks
* Citações diárias
* Sistema de gamificação
* Fóruns de discussão
* Quizzes e desafios
* Recursos educacionais complementares

Essa estratégia demonstra potencial para gerar tráfego consistente e monetização através de anúncios em ambas as plataformas.

---

## 🛠️ Tecnologias Utilizadas

* Python
* Jupyter Notebook
* Estruturas de Dados (Listas e Dicionários)
* Limpeza de Dados
* Análise Exploratória de Dados (EDA)

---

## 📚 Habilidades Demonstradas

* Data Cleaning
* Data Wrangling
* Remoção de Duplicatas
* Tratamento de Dados Textuais
* Análise Exploratória
* Análise de Mercado
* Extração de Insights
* Tomada de Decisão Baseada em Dados

---

## 👨‍💻 Autor

Projeto desenvolvido para prática de Análise de Dados utilizando Python e dados reais da App Store e Google Play Store.
