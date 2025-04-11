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

📁 [E-Commerce Cosmetics Dataset](https://www.kaggle.com/datasets/devi5723/e-commerce-cosmetics-dataset/data)
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
- PySpark
- MLlib
- Pandas

---

## 💬 Sobre mim

Sou Mãe do Conrado, carioca, bibliotecária pela UFRJ, product manager atuando no Ifood 🍔, com 9 anos de experiência. Apaixonada por entender problemas reais, construir soluções com propósito e, agora, aplicando esse olhar na **ciência de dados**.  
Com formação em **biblioteconomia** e uma bagagem prática em produto, sigo acreditando na interdiciplinaridade como chave para ser um difernecial no mercado, com foco em aprendizado constante — este projeto é parte dessa 
jornada. 💙

---

## 📚 Catálogo de Dados - E-Commerce Cosmetics Dataset

Este catálogo apresenta uma descrição detalhada do conjunto de dados utilizado no projeto, com informações sobre os campos disponíveis, seus tipos, domínios (valores esperados), e a linhagem dos dados. O objetivo é facilitar a compreensão da estrutura dos dados para futuras análises e modelagens.

---

### 🔗 Linhagem dos Dados

- **Fonte**: [E-Commerce Cosmetics Dataset - Kaggle](https://www.kaggle.com/datasets/devi5723/e-commerce-cosmetics-dataset/data)
- **Formato Original**: CSV
- **Origem dos Dados**: Scraping de sites de e-commerce (Ulta, Amazon, Flipkart, Sephora)
- **Técnica de Coleta**: Web scraping (detalhes não fornecidos na fonte original)
- **Transformações Realizadas**:
  - Unificação de estruturas entre websites
  - Padronização de campos (ex: preços em INR, normalização de categorias)

---

### 🧬 Dicionário de Dados

| Coluna               | Tipo     | Descrição                                                        | Domínio / Exemplos                              |
|----------------------|----------|-------------------------------------------------------------------|-------------------------------------------------|
| `Product_name`       | String   | Nome do produto                                                   | Ex: `Lakme Absolute Blur Perfect Primer`        |
| `Website`            | String   | Site de origem do produto                                         | `Ulta`, `Amazon`, `Flipkart`, `Sephora`         |
| `Category`           | String   | Categoria geral do produto cosmético                              | `eyes`, `face`, `lips`, `body`, `skincare`, `hair` |
| `Subcategory`        | String   | Subcategoria mais específica do produto                           | Ex: `Lipstick`, `Foundation`, `Concealer`       |
| `href`               | String   | URL do produto no site original                                   | Link clicável                                   |
| `Price`              | Float    | Preço do produto em INR                                           | Mín: ~50 — Máx: ~5000+                          |
| `Brand`              | String   | Marca responsável pelo produto                                    | Ex: `Lakme`, `Maybelline`, `L'Oreal`, `Sugar`   |
| `Ingredients`        | String   | Ingredientes do produto (texto livre)                             | Ex: `Aqua, Dimethicone, Titanium Dioxide...`    |
| `Form`               | String   | Consistência ou forma física do produto                           | Ex: `Liquid`, `Cream`, `Gel`, `Powder`          |
| `Type`               | String   | Informações adicionais do produto                                 | Ex: `Matte`, `Long Wear`, `Waterproof`          |
| `Color`              | String   | Cor do produto (quando aplicável)                                 | Ex: `Cherry Red`, `Ivory`, `Nude`               |
| `Quantity`           | Float    | Volume do produto em mililitros (ml)                              | Mín: ~5ml — Máx: ~1000ml                        |
| `Rating`             | Float    | Avaliação média dos clientes (escala de 0 a 5)                    | Mín: 0.0 — Máx: 5.0                             |
| `Number of ratings`  | Integer  | Número total de avaliações recebidas                              | Mín: 0 — Máx: 90.000+                           |

---

### 📈 Domínio dos Dados Numéricos

| Campo               | Valor Mínimo | Valor Máximo | Observações                        |
|--------------------|---------------|---------------|------------------------------------|
| `Price`            | ~50           | ~5000         | Provavelmente valores em INR       |
| `Quantity`         | ~5 ml         | ~1000 ml      | Pode conter ruído ou unidades faltantes |
| `Rating`           | 0.0           | 5.0           | Escala padrão de avaliações        |
| `Number of ratings`| 0             | 90.000+       | Quantidade total de avaliações     |

---
### 🏷️ Domínio dos Dados Categóricos

#### `Website`
Plataformas de e-commerce de onde os dados foram extraídos:
- Ulta
- Amazon
- Flipkart
- Sephora

#### `Category`
Categorias principais de produtos cosméticos:
- Eyes (olhos)
- Face (rosto)
- Lips (lábios)
- Body (corpo)
- Skincare (cuidados com a pele)
- Hair (cabelos)

#### `Subcategory`
Subcategorias específicas dentro das categorias principais:
- Mascara
- Eyeliner
- Foundation
- Lipstick
- Moisturizer
- Shampoo
- Sunscreen
- Blush
- Concealer
- Conditioner

#### `Brand`
Marcas populares dos produtos:
- Maybelline
- Lakme
- L'Oréal
- MAC
- Sugar Cosmetics
- Revlon
- The Body Shop
- Neutrogena
- Biotique
- WOW Skin Science

#### `Form`
Formato ou consistência dos produtos:
- Liquid
- Cream
- Powder
- Gel
- Balm
- Serum
- Lotion
- Stick

#### `Type`
Características adicionais do produto:
- Matte
- Glossy
- Waterproof
- Long Wear
- Natural Finish
- SPF Protection
- Oil-Free
- Fragrance-Free

#### `Color`
Cores informadas nos produtos:
- Red
- Nude Beige
- Deep Brown
- Coral Crush
- Cherry Red
- Classic Ivory
- Natural Buff
- Pink Blossom

### 🗂️ Modelo de Dados - Esquema Estrela

![Esquema Estrela do Dataset de E-commerce](https://github.com/maizamgs/MVP-CatalogAI/blob/66e6c2742fa8fe55c47e0e10fa10ba316897b607/esquema%20estrela.png?raw=true)


## 📒 Notebook no Databricks

Você pode acessar e executar o notebook completo diretamente no Databricks através do link abaixo:

[🔗 Abrir notebook no Databricks](https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/1173022975515537/1628847209129796/6057031536656093/latest.html)


