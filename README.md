[//]: # (Links importantes)

[📝 Artigo de Replicação: Work Replication - G-EVAL (PDF)](./Work%20Replication%20-%20G-EVAL.pdf)

- 📄 Artigo original: [G-Eval: NLG Evaluation using GPT-4 with Better Human Alignment](https://arxiv.org/abs/2303.16634)
- 📓 Notebook da replicação: [replicacao.ipynb](https://github.com/K010TE/replicacao-geval/blob/main/replicacao.ipynb)
- 💻 Repositório original: [nlpyang/geval](https://github.com/nlpyang/geval)

# Replicação do G-EVAL: Avaliação de Geração de Linguagem Natural com GPT-4

Este repositório contém a replicação do artigo **"G-EVAL: NLG Evaluation using GPT-4 with Better Human Alignment"**, com base nos benchmarks fornecidos e adaptado ao ambiente local.

---

## 📁 Estrutura do Projeto

```
.
├── data/
│   └── summeval.json                # Dataset de referência (SummEval)
│
├── prompts/
│   └── summeval/
│       ├── coh_detailed.txt        # Prompt de Coerência
│       ├── con_detailed.txt        # Prompt de Consistência
│       ├── flu_detailed.txt        # Prompt de Fluência
│       └── rel_detailed.txt        # Prompt de Relevância
│
├── results/
│   ├── gpt4_coh_detailed.json      # Resultados de Coerência
│   ├── gpt4_con_detailed.json      # Resultados de Consistência
│   ├── gpt4_flu_detailed.json      # Resultados de Fluência
│   └── gpt4_rel_detailed.json      # Resultados de Relevância
│
├── .env                            # Contém sua chave da OpenAI (NÃO subir no GitHub)
├── .gitignore                      # Ignora arquivos sensíveis e temporários
├── gpt4_eval.py                    # Script principal para geração de avaliações
├── meta_eval_summeval.py          # Script de cálculo de correlações com dados do paper
├── avaliar_correlacoes.py         # Versão adaptada em português para análise local
├── replicacao.ipynb               # Notebook completo da replicação
├── LICENSE
└── README.md
```

---

## 🚀 Como Executar

1. **Configure sua chave da OpenAI:**

Crie um arquivo `.env` com o conteúdo:

```
OPENAI_API_KEY=sua-chave-aqui
```

2. **Instale as dependências:**

```bash
pip install -r requirements.txt
```

3. **Execute o notebook:**

```bash
jupyter notebook replicacao.ipynb
```

4. **Ou rode os scripts manualmente:**

```bash
python gpt4_eval.py
python avaliar_correlacoes.py
```

---

## 📊 Resultados

Os resultados finais são apresentados como correlações (Pearson, Spearman, Kendall-Tau) entre as avaliações do G-EVAL e os julgamentos humanos para os critérios: **Coerência, Consistência, Fluência e Relevância**.

---

## 📄 Licença

Este projeto segue a licença do repositório original. Consulte o arquivo `LICENSE` para mais detalhes.
