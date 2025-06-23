
# 📝 Replicação do G-EVAL: Avaliação de Geração de Linguagem Natural com GPT-4

Este repositório contém a **replicação do experimento descrito no artigo [G-EVAL: NLG Evaluation using GPT-4 with Better Human Alignment](https://arxiv.org/abs/2303.16634)**, com o objetivo de avaliar a capacidade de modelos de linguagem em julgar automaticamente a qualidade de saídas de sistemas de Geração de Linguagem Natural (NLG), com base em critérios como **coerência**, **consistência**, **fluência** e **relevância**.

## 📁 Estrutura do Projeto

```
.
├── replicacao.ipynb         # Notebook principal com toda a execução
├── avaliar_correlacoes.py   # Script para calcular correlações com notas humanas
├── results/                 # Arquivos .json com saídas do G-EVAL
├── .env                     # Arquivo com a chave da OpenAI (NÃO subir no GitHub)
├── requirements.txt         # Dependências do projeto
└── README.md                # Este arquivo
```

## ⚙️ Requisitos

Você precisará ter o **Python 3.8 ou superior** instalado. Recomenda-se o uso de um ambiente virtual.

Instale as dependências com:

```bash
pip install -r requirements.txt
```

## 🔐 Configuração da Chave da OpenAI

Este projeto utiliza a API do GPT-4 via OpenAI. Para manter sua chave segura:

1. Crie um arquivo `.env` na raiz do projeto:
    ```ini
    OPENAI_API_KEY=sk-proj-sua-chave-aqui
    ```
2. **Nunca suba esse arquivo para o GitHub** (o `.gitignore` já está configurado para ignorá-lo).

## ▶️ Como Executar

A replicação pode ser feita diretamente pelo notebook:

1. Abra o arquivo `replicacao.ipynb`.
2. Execute as células sequencialmente.
3. Os resultados de avaliação serão salvos e plotados ao final.

Também é possível rodar a avaliação estatística separadamente:

```bash
python avaliar_correlacoes.py
```

## 📊 Resultados

Os resultados obtidos na replicação incluem os coeficientes de correlação entre as notas atribuídas pelo G-EVAL (via GPT-4) e as notas humanas de referência, como **Pearson**, **Spearman** e **Kendall-Tau** para cada critério avaliado.

## 📚 Referência Original

> Liu, X., Zhu, C., Mou, L., & Yang, D. (2023).  
> **G-EVAL: NLG Evaluation using GPT-4 with Better Human Alignment**.  
> *arXiv preprint arXiv:2303.16634*.  
> [https://arxiv.org/abs/2303.16634](https://arxiv.org/abs/2303.16634)
