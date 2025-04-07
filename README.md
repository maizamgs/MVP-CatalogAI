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

📁 [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce):

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


## 📊 Catálogo de Dados

Este projeto utiliza dois arquivos principais do [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce):

---

### 🗂️ 1. `olist_products_dataset.csv`

Contém informações detalhadas sobre os produtos vendidos na plataforma.

| Coluna                     | Tipo     | Descrição                                                                 |
|----------------------------|----------|---------------------------------------------------------------------------|
| `product_id`               | string   | Identificador único do produto                                            |
| `product_category_name`    | string   | Nome da categoria original (em português)                                 |
| `product_name_lenght`      | inteiro  | Quantidade de caracteres no nome do produto                               |
| `product_description_lenght` | inteiro | Quantidade de caracteres na descrição do produto                          |
| `product_photos_qty`       | inteiro  | Quantidade de fotos disponíveis                                           |
| `product_weight_g`         | inteiro  | Peso do produto em gramas                                                 |
| `product_length_cm`        | inteiro  | Comprimento do produto em centímetros                                     |
| `product_height_cm`        | inteiro  | Altura do produto em centímetros                                          |
| `product_width_cm`         | inteiro  | Largura do produto em centímetros                                         |

🔎 **Observações:**
- A coluna `product_category_name` será utilizada como **rótulo (target)** para a classificação.
- As demais colunas podem ser utilizadas como **features complementares**.
- Campos com valores nulos precisam ser tratados no pré-processamento.

---

### 📘 2. `product_category_name_translation.csv`

Tabela de apoio com a tradução das categorias de produto para o inglês.

| Coluna                       | Tipo     | Descrição                                           |
|------------------------------|----------|-----------------------------------------------------|
| `product_category_name`      | string   | Nome da categoria em português                      |
| `product_category_name_english` | string | Nome da categoria traduzido para o inglês           |

🔗 Pode ser integrado ao `olist_products_dataset.csv` via `product_category_name`.

---

## 🧩 Como esses dados serão usados no MVP?

- A partir do `olist_products_dataset.csv`, o MVP utilizará principalmente:
  - `product_category_name` como **target**
  - A estrutura do nome, descrição e atributos físicos como **features**
- O objetivo é treinar um modelo que consiga prever a categoria de um produto com base nas informações disponíveis.

---

## 🧠 Modelagem 

                    ┌────────────────────────────┐
                    │  olist_products_dataset    │
                    └────────────────────────────┘
                       │
                       │ product_category_name
                       ▼
        ┌────────────────────────────────────┐
        │ product_category_name_translation  │
        └────────────────────────────────────┘

                    ▼
     ┌──────────────────────────────────────┐
     │   Pré-processamento e Engenharia     │
     │      de Features (nome, peso, etc)   │
     └──────────────────────────────────────┘

                    ▼
     ┌──────────────────────────────────────┐
     │  Modelo de Classificação (ML/NLP)    │
     │ Entradas: nome, descrição, medidas   │
     │ Saída: categoria sugerida            │
     └──────────────────────────────────────┘

                    ▼
     ┌──────────────────────────────────────┐
     │  Resultado:                          │
     │ - Categoria recomendada              │
     │ - Nível de confiança                 │
     │ - Tradução da categoria (opcional)   │
     └──────────────────────────────────────┘



### 🔍 Explicação Rápida:
- O projeto começa com a leitura do arquivo `olist_products_dataset.csv`.
- A categoria original é traduzida via `product_category_name_translation.csv`.
- Após o pré-processamento, os dados alimentam um modelo de machine learning para sugerir automaticamente a categoria.
- O resultado inclui a categoria prevista e o nível de confiança 

---

