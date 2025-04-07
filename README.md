# 🛍️ CatalogAI - Classificador Inteligente de Itens  
*MVP unindo produto, dados e organização da informação*

## ✨ Sobre o Projeto

Este é um MVP desenvolvido por uma **Product Manager com 9 anos de experiência**, atualmente aluna da pós-graduação em **Ciência de Dados e Analytics (PUC-Rio)**. Com formação em **biblioteconomia**, este projeto nasceu da vontade de explorar como a inteligência artificial pode tornar processos manuais mais ágeis, precisos e escaláveis.

O objetivo principal é construir uma **ferramenta de apoio para analistas de negócios**, automatizando a **classificação de produtos** em taxonomias predefinidas, com base em dados públicos e técnicas introdutórias de machine learning.

---

## 🎯 Objetivo

> Criar uma solução simples, funcional e com potencial de evolução que auxilie analistas a classificarem produtos automaticamente, reduzindo tempo, melhorando a consistência e facilitando revisões humanas com transparência.

---

## 👥 Público-Alvo

- Analistas de negócios de varejo e e-commerce  
- Equipes responsáveis por catalogação, curadoria ou organização de produtos  
- Profissionais que lidam com dados não estruturados e precisam organizá-los por categorias  

---

## ❗ Problema

- Classificação manual é **demorada, repetitiva e sujeita a erros**
- Taxonomias de produtos são **complexas e, muitas vezes, inconsistentes**
- O tempo gasto com essas tarefas **reduz o foco em atividades analíticas mais estratégicas**

---

## 💡 Solução Proposta

- Um sistema que recebe como entrada **nome e descrição dos produtos**
- Processa os dados usando **modelos básicos de machine learning**
- Retorna a **categoria sugerida** com um **nível de confiança (Alta / Média / Baixa)**
- Permite **revisão manual** e exportação de resultados em relatório visual

---

## 🔍 Fonte de Dados

Utiliza dados públicos disponíveis no Kaggle:

📁  [Amazon Sales Dataset (Kaggle)](https://www.kaggle.com/code/mehakiftikhar/amazon-sales-dataset-eda/input)
---

## ✅ Funcionalidades do MVP

- Upload de arquivos em **CSV ou Excel**
- Classificação automática com **modelo supervisionado**
- Interface simples para revisão dos resultados
- Geração de **relatório final** com itens classificados e exceções

---

## 🛠️ Tecnologias Utilizadas

- Python  
- Databricks

---

## 💬 Sobre mim

Sou Mãe do Conrado, carioca, bibliotecária pela UFRJ, product manager atuando no Ifood 🍔, com 9 anos de experiência. Apaixonada por entender problemas reais, construir soluções com propósito e, agora, aplicando esse olhar na **ciência de dados**.  
Com formação em **biblioteconomia** e uma bagagem prática em produto, sigo acreditando na interdiciplinaridade como chave para ser um difernecial no mercado, com foco em aprendizado constante — este projeto é parte dessa 
jornada. 💙

---


## 📚 Catálogo de Dados

### 🧬 Fonte dos Dados
- **Dataset:** [Amazon Sales Dataset - EDA](https://www.kaggle.com/code/mehakiftikhar/amazon-sales-dataset-eda/input)
- **Origem:** Kaggle - Dados coletados de produtos disponíveis na Amazon.
- **Linhagem dos Dados:** Os dados foram baixados diretamente da plataforma Kaggle. O dataset foi compilado a partir de informações públicas de listagens de produtos na Amazon. A coleta provavelmente foi realizada via scraping ou API pública da plataforma (detalhes não especificados pela autora original do dataset).
- **Objetivo do Uso:** Treinar um modelo de classificação automática de produtos com base em nome e descrição textual.

---

### 📝 Descrição das Variáveis

| Variável               | Tipo          | Descrição                                                                 | Domínio/Valores Esperados                              |
|------------------------|---------------|---------------------------------------------------------------------------|--------------------------------------------------------|
| `product_name`         | Categórica    | Nome do produto listado na Amazon                                         | Ex: "Wireless Mouse", "Yoga Mat", "Laptop Stand"       |
| `product_category`     | Categórica    | Categoria atribuída ao produto                                            | Ex: "Electronics", "Home", "Beauty", "Fashion"         |
| `product_description`  | Texto Livre   | Descrição textual do produto                                              | Textos curtos ou médios, com detalhes do produto       |
| `price`                | Numérica (float) | Preço do produto em dólares americanos (USD)                            | Mín: 0.01 / Máx: ~10.000 (valores extremos a tratar)   |
| `rating`               | Numérica (float) | Avaliação média dos usuários, de 1 a 5                                   | Mín: 1.0 / Máx: 5.0                                     |
| `number_of_reviews`    | Numérica (int) | Quantidade total de avaliações recebidas                                 | Mín: 0 / Máx: milhares (ex: 15.000+)                    |
| `brand`                | Categórica    | Nome da marca ou fabricante                                               | Ex: "Samsung", "Apple", "Nike", "Unknown"              |
| `product_url`          | Texto Livre   | URL para o produto na Amazon                                              | Ex: `https://amazon.com/....`                          |
| `image_url`            | Texto Livre   | URL da imagem do produto                                                  | Ex: `https://images.amazon.com/....`                   |

---

### 📌 Observações
- As colunas `product_name` e `product_description` serão as principais **entradas textuais** para o modelo de classificação.
- Colunas como `price`, `rating` e `number_of_reviews` podem ser usadas como **variáveis auxiliares ou filtros** na análise exploratória ou no refinamento da classificação.
- Alguns valores podem conter **nulos**, marcas desconhecidas, ou outliers (ex: preços muito baixos ou muito altos) que exigirão tratamento na etapa de pré-processamento.

