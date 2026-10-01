# ADE SAMPA — Inteligência Territorial

**Prova Técnica Prática — Edital nº 005/2026**
**Cargo:** Assistente II — Dados e IA
**Candidata:** Camila Evelyn Rodrigues Pimenta

---

## 🔗 Aplicação publicada

Acesse a aplicação: **[https://CERPimenta.github.io/ade-sampa-inteligencia-territorial/](https://CERPimenta.github.io/ade-sampa-inteligencia-territorial/)**

Substitua `SEU-USUARIO` pelo seu nome de usuário do GitHub.

---

## 1. Título do projeto

ADE SAMPA — Inteligência Territorial: Radar de Oportunidades e Mapa de Acesso a Serviços

## 2. Descrição do problema identificado

A ADE SAMPA atua no fomento ao empreendedorismo e oferece serviços de orientação, mentoria e capacitação em espaços TEIA. Foram identificados dois problemas:
- **Módulo 1:** Microempreendedores não têm ferramenta para decidir onde abrir um negócio com base em demanda, concorrência e renda.
- **Módulo 2:** Não há visão consolidada de quais territórios estão descobertos de espaços TEIA e capacitações.

## 3. Contexto e justificativa da escolha

Ambos os módulos se alinham ao eixo de desenvolvimento econômico da ADE SAMPA e ao uso de dados para apoio à decisão. Complementam o Observatório MEI e os programas de orientação da agência.

## 4. Secretaria, órgão, política pública ou área municipal relacionada

- **Órgão:** ADE SAMPA (Agência São Paulo de Desenvolvimento)
- **Secretaria:** Secretaria Municipal de Desenvolvimento Econômico e Trabalho (SMDET)
- **Áreas:** Programas TEIA, Fábrica de Negócios, Observatório MEI

## 5. Descrição da solução desenvolvida

Aplicação web estática (HTML + CSS + JavaScript) com dois módulos independentes:
- **Módulo 1 — Radar de Oportunidades:** calcula um Índice de Oportunidade (IO) por distrito para cada tipo de atividade (CNAE), com base em população, concorrência, renda e presença de TEIA.
- **Módulo 2 — Mapa de Acesso a Serviços:** calcula um Índice de Cobertura por distrito, com base na distância até o TEIA mais próximo e no número de capacitações.

## 6. Público ou área da gestão potencialmente beneficiada

- MEIs e potenciais empreendedores da cidade de São Paulo.
- Gestores e equipes de campo da ADE SAMPA.

## 7. Principais funcionalidades

- Mapa interativo com marcadores coloridos por distrito (Leaflet).
- Ranking dos 10 melhores/piores distritos.
- Filtros por CNAE e por camadas (TEIAs/capacitações).
- Tabelas com os dados sintéticos utilizados nos cálculos.
- Exportação dos dados em CSV.

## 8. Fontes pesquisadas

- Censo 2022 (IBGE) — população por distrito.
- Mapa da Desigualdade 2024 — renda média por distrito.
- Observatório MEI (ADE SAMPA) — total de MEIs por distrito.
- GeoSampa — malha geoespacial dos distritos.
- Site institucional da ADE SAMPA — localização dos espaços TEIA.

## 9. Dados utilizados

- **Reais:** população, renda média, total de MEIs por distrito, localização dos TEIAs.
- **Sintéticos:** distribuição de MEIs por CNAE; agenda de capacitações.

## 10. Indicação clara de dados sintéticos

A distribuição de MEIs por CNAE e a agenda de capacitações são **sintéticas**. Premissas:
- A distribuição de atividades dentro de cada distrito segue a média da cidade, com ruído gaussiano de 15% (clipado entre 0,5 e 1,5).
- Os totais por distrito são calibrados pelos dados reais do Observatório MEI.

## 11. Justificativa das principais escolhas realizadas

- **Site estático:** não exige instalação de Python ou servidor;
- **Leaflet + OpenStreetMap França:** biblioteca leve, sem API key, funciona localmente.
- **Dados sintéticos:** necessários pela indisponibilidade pública de bases granulares; a calibração preserva a ordem de grandeza.
- **Índices compostos (IO e Cobertura):** traduzem múltiplas variáveis em um número interpretável para apoio à decisão.

## 12. Metodologia adotada

1. Coleta de dados públicos.
2. Geração da base sintética.
3. Cálculo dos índices (IO e Cobertura) em JavaScript.
4. Renderização de mapas e rankings no navegador.

## 13. Tecnologias, bibliotecas, plataformas e ferramentas utilizadas

- HTML5, CSS3, JavaScript (ES6)
- Leaflet 1.9 (via CDN)
- OpenStreetMap França (tiles)

## 14. Descrição resumida da utilização de inteligência artificial

- **Ferramentas:** ChatGPT.
- **Etapas:** estruturação, geração de código, redação da documentação.
- **Avaliação:** código testado localmente; dados conferidos nas fontes originais.

## 15. Limitações identificadas

- Dados sintéticos para CNAE e capacitações.
- Índices heurísticos, não modelos estatísticos.
- Sem dados em tempo real.

## 16. Possíveis melhorias ou evoluções da solução

- Substituir dados sintéticos por dados reais do Observatório MEI.
- Integrar com a API do SAADE.
- Adicionar séries temporais e camadas de equipamentos públicos.

---

## 🚀 Como executar

1. Clone ou baixe este repositório.
2. Abra o arquivo **`index.html`** no navegador (duplo clique).
3. Navegue pelos módulos pelo menu superior.

Não é necessário instalar nada. A aplicação é 100% estática.

---

## 📚 Sobre

A página **`sobre.html`** contém todas as explicações sobre a ADE SAMPA, o MEI, os espaços TEIA, o Observatório MEI, as fontes de dados, a metodologia e o uso de IA.
