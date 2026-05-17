# 🔐 IA na Governança de Dados: Classificação Automatizada e Mitigação de Riscos em Ambientes Financeiros

> **Artigo Científico** — Centro Universitário Senac, Campus Santo Amaro · São Paulo, 2026

---

## 🔗 Links Rápidos

| | Link |
|---|---|
| 🌐 **Página do Projeto** | [matheusavolio.github.io/artigo_cientifico_PI5](https://matheusavolio.github.io/artigo_cientifico_PI5/) |
| 📄 **Artigo Científico (PDF)** | [artigo_classificacao_automatica_de_dados.pdf](./artigo_classificacao_automatica_de_dados.pdf) |
| 🖼️ **Banner da Apresentação (PDF)** | [banner_artigo.pdf](./banner_artigo.pdf) |

---

## 📋 Sobre o Artigo

Este trabalho investiga como a **Inteligência Artificial** pode ser usada como mecanismo de controle na **Governança de Dados** de ambientes corporativos financeiros, classificando automaticamente informações em trânsito e reduzindo riscos de vazamento — em conformidade com a **LGPD** (Lei nº 13.709/2018) e com a norma **ABNT NBR ISO/IEC 27001:2022**.

O problema central que o artigo responde é:

> *Como a IA pode classificar automaticamente informações em trânsito e reduzir riscos de vazamento em ambientes financeiros, em conformidade com a LGPD e com os requisitos da ISO/IEC 27001?*

---

## 🧠 O Modelo Proposto

O artigo propõe um **modelo conceitual TO-BE** de classificação automatizada com IA, estruturado em **4 camadas interdependentes**:

| Camada | Função |
|--------|--------|
| **1 — Governança de Dados** | Define políticas, papéis (DPO, Data Owner, Data Steward) e critérios normativos |
| **2 — Classificação Automatizada** | Modelos de PLN (Legal-BERT+NER) analisam semanticamente os dados em trânsito |
| **3 — Controle DLP** | Aplica ações diferenciadas: liberar, alertar, bloquear ou notificar o DPO |
| **4 — Conformidade e Auditoria** | Registra logs auditáveis para a ANPD e auditorias internas |

### Os 4 Níveis de Classificação (ISO/IEC 27001 A.5.12)

| Nível | Definição | Ação DLP | Base Legal |
|-------|-----------|----------|------------|
| 🟢 **Público** | Sem restrição de acesso | Monitoramento passivo | LGPD art. 7º |
| 🔵 **Privado** | Uso interno apenas | Alerta ao usuário | LGPD art. 46 |
| 🟡 **Confidencial** | Dano à organização se exposto | Bloqueio + Log | LGPD art. 46 + 48 |
| 🔴 **Sensível** | Dano direto ao titular (saúde, biometria, crédito) | Bloqueio + Notifica DPO | LGPD art. 5º,II · 11 · 52 |

---

## 🤖 Por que Legal-BERT+NER?

O artigo avaliou cinco arquiteturas de PLN aplicadas a documentos regulatórios financeiros. O **Legal-BERT+NER** obteve os melhores resultados em todas as métricas:

| Modelo | Precisão | Recall | F1-Score | Conformidade |
|--------|----------|--------|----------|-------------|
| **Legal-BERT+NER** | **93,1%** | **91,7%** | **92,4%** | **90,8%** |
| Legal-BERT | 91,2% | 88,7% | 89,9% | 87,5% |
| FinBERT | 88,5% | 86,3% | 87,4% | 85,2% |
| Longformer | 86,7% | 83,9% | 85,3% | 82,4% |
| LSTM-SVM | 79,4% | 76,1% | 77,7% | 74,3% |

> Fonte: Adaptado de Battu (2025) — *International Journal of Science and Research Archive*, v. 15, n. 3.

Pilotos em instituições financeiras dos EUA, UE e Índia demonstraram **redução de ~40% na carga de trabalho manual de compliance** com a adoção desses modelos.

---

## ⚠️ O Problema que o Artigo Endereça

O processo manual atual (AS-IS) apresenta três fragilidades estruturais:

- **Ausência de critério padronizado** de classificação entre colaboradores
- **Dependência de julgamento individual** para identificar a sensibilidade do dado
- **Sem trilha de auditoria sistemática**, dificultando a demonstração de conformidade com o art. 46 da LGPD

O modelo TO-BE proposto endereça todas essas fragilidades ao automatizar a classificação, padronizar os rótulos e gerar registros auditáveis contínuos.

---

## 🔬 Metodologia

Pesquisa **exploratória com abordagem qualitativa**, desenvolvida em 6 etapas:

1. Definição do problema e objetivos
2. Levantamento bibliográfico (Google Acadêmico, Repositório UFU, DSpace Mackenzie, IJSRA, Planalto)
3. Leitura e organização por eixo temático
4. Análise documental da LGPD e ISO/IEC 27001:2022
5. Triangulação das fontes
6. Estruturação do modelo conceitual TO-BE

---

## 📁 Arquivos do Repositório

| Arquivo | Descrição |
|---------|-----------|
| [`index.html`](./index.html) | Demonstração interativa do modelo Legal-BERT+NER (GitHub Pages) |
| [`artigo_classificacao_automatica_de_dados.pdf`](./artigo_classificacao_automatica_de_dados.pdf) | Artigo científico completo em PDF |
| [`banner_artigo.pdf`](./banner_artigo.pdf) | Banner utilizado na apresentação do projeto |
| [`README.md`](./README.md) | Documentação do repositório |

---

## 📚 Referências Principais

- **BATTU, G. G.** Automated Interpretation of Financial Regulations Using NLP. *IJSRA*, v. 15, n. 3, p. 832–840, 2025. [DOI](https://doi.org/10.30574/ijsra.2025.15.3.1580)
- **BRASIL.** Lei nº 13.709/2018 — Lei Geral de Proteção de Dados Pessoais (LGPD). [Link](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm)
- **ABNT NBR ISO/IEC 27001:2022** — Segurança da Informação, Segurança Cibernética e Proteção à Privacidade
- **CARDOSO, J. D.** IA Generativa em ambientes corporativos: análise dos riscos de segurança e governança. UFU, 2025. [Link](https://repositorio.ufu.br/handle/123456789/45935)
- **GAYDUTSCHENKO, I.** Vazamentos de dados: uma análise a partir da LGPD e das políticas de compliance. Mackenzie, 2022. [Link](https://dspace.mackenzie.br/items/c08c0b22-9def-447c-8b02-eaffb6809dd6)
- **SOUZA, R. A.; SOUZA, J. S.** Inteligência artificial e a segurança da informação. *Research, Society and Development*, v. 13, n. 7, 2024. [DOI](http://dx.doi.org/10.33448/rsd-v13i7.46373)

---

## 👥 Autores

| Nome | E-mail | LinkedIn |
|------|--------|----------|
| Gabriela Nogueira Freire | [gabiinnog@gmail.com](mailto:gabiinnog@gmail.com) | [gabiinnog](https://linkedin.com/in/gabiinnog) |
| Jade Alves Prado | [jade.jadeprado@gmail.com](mailto:jade.jadeprado@gmail.com) | [jadeprado](https://linkedin.com/in/jadeprado) |
| Matheus Avolio Sedel | [avoliomatheus.sed@gmail.com](mailto:avoliomatheus.sed@gmail.com) | [matheusavolio](https://linkedin.com/in/matheusavolio) |
| Otavio Joaquim Fernandes | [otaviojoaquimf@gmail.com](mailto:otaviojoaquimf@gmail.com) | [otaviojfernandes](https://linkedin.com/in/otaviojfernandes) |

> Centro Universitário Senac — Campus Santo Amaro · São Paulo, SP, Brasil · 2026

---

## 🔗 Palavras-chave

`inteligência artificial` `governança de dados` `classificação da informação` `proteção de dados` `LGPD` `ISO 27001` `Legal-BERT` `NLP` `DLP` `compliance` `RegTech` `setor financeiro`
