# 🛒 Supermercado São João

Sistema web de apoio à gestão de supermercado, com foco em cadastro de produtos, acompanhamento de estoque, validade, demandas, vendas e relatórios.

> **Status:** projeto em desenvolvimento. Existem protótipos de interface e funcionalidades demonstrativas; este README descreve a visão completa do sistema, **não** afirma que todos os módulos já estão implementados ou integrados.

## 1. Visão geral

O **Supermercado São João** é uma aplicação de gestão comercial destinada a centralizar informações operacionais do supermercado. Seu painel reúne indicadores de vendas e demanda, enquanto os módulos de operação organizam produtos, insumos, vencimentos e alertas de estoque.

O design dos protótipos utiliza menu lateral azul-marinho, botões verdes, área principal clara, tabelas, cartões informativos e gráficos.

## 2. Objetivos

- Centralizar o cadastro e a consulta de produtos.
- Facilitar o acompanhamento das quantidades disponíveis em estoque.
- Identificar produtos próximos do vencimento ou vencidos.
- Apoiar decisões de reposição por meio de alertas e indicadores de demanda.
- Organizar informações de vendas, funcionários e relatórios.
- Oferecer uma interface responsiva e de fácil navegação.

## 3. Tecnologias

| Tecnologia | Aplicação |
| --- | --- |
| HTML5 | Estrutura semântica das telas |
| CSS3 | Identidade visual, layout e responsividade |
| Bootstrap 5 | Componentes de interface e grid responsivo |
| JavaScript | Interações, validações e manipulação de dados no protótipo |
| `localStorage` | Persistência local demonstrativa, quando implementada |

**Importante:** Bootstrap pode ser carregado via CDN, exigindo internet. O projeto ainda não tem uma API ou banco de dados definidos e integrados como parte desta documentação.

## 4. Módulos do sistema

### 4.1 Dashboard

**Objetivo:** oferecer uma visão consolidada do desempenho do supermercado.

Elementos previstos nos protótipos:

- Indicador de demanda em queda.
- Produto com maior crescimento de demanda.
- Produto mais vendido.
- Valor total de vendas no mês.
- Gráfico de demanda por semana.
- Gráfico dos cinco produtos mais vendidos.
- Tabela de previsão de estoque.
- Destaques de reposição e atenção.
- Pesquisa de produtos e seleção de período.

**Situação:** interface demonstrativa; os indicadores precisam ser conectados a registros reais para representar a operação.

### 4.2 Produtos

**Objetivo:** manter o catálogo de produtos comercializados.

Funcionalidades do protótipo:

- Cadastrar produtos.
- Consultar e pesquisar produtos.
- Editar dados cadastrados.
- Excluir produtos.
- Consultar preço, quantidade em estoque e validade.

**Campos de referência:** código, nome, marca, preço, quantidade em estoque, fornecedor e data de validade.

**Situação:** foi desenvolvido um protótipo de Produtos com armazenamento local no navegador. A persistência não equivale a um banco de dados corporativo.

### 4.3 Insumos

**Objetivo:** acompanhar os insumos utilizados na operação.

Escopo previsto:

- Cadastro e consulta de insumos.
- Controle de quantidade disponível.
- Registro de fornecedores.
- Identificação de itens que precisam de reposição.

**Situação:** módulo previsto; requer confirmação das regras específicas de movimentação e implementação completa.

### 4.4 Demandas

**Objetivo:** acompanhar a procura e o desempenho dos produtos.

Escopo previsto:

- Consulta de produtos com aumento ou queda de demanda.
- Comparação de períodos.
- Visualização de indicadores e gráficos.
- Apoio ao planejamento de reposição.

**Situação:** indicadores demonstrativos; cálculo real depende de histórico de vendas consistente.

### 4.5 Validade de produtos

**Objetivo:** acompanhar os prazos de vencimento.

Elementos presentes na referência visual:

- Nome do produto.
- Imagem ilustrativa do produto.
- Informação de validade.
- Navegação pelo menu lateral.

Evoluções funcionais previstas:

- Listagem por data de vencimento.
- Identificação de produtos vencidos e próximos do vencimento.
- Filtro e pesquisa.

**Situação:** protótipo visual; para alertas confiáveis, cada produto ou lote precisa de uma data completa de validade, não apenas do ano.

### 4.6 Alertas de estoque

**Objetivo:** identificar necessidade de reposição.

Escopo previsto:

- Visualização de produtos com estoque baixo.
- Destaque de itens sem estoque.
- Consulta de quantidades atuais.
- Critérios configuráveis de estoque mínimo (a definir).

**Situação:** funcionalidade prevista; os limiares de alerta e regras de atualização precisam ser definidos.

### 4.7 Caixa e PDV

**Objetivo:** registrar vendas no ponto de venda.

Escopo previsto:

- Busca e seleção de produtos.
- Inclusão de itens em uma venda.
- Cálculo de subtotal e total.
- Finalização da venda.
- Atualização do estoque após venda concluída.

**Situação:** prototipação demonstrativa; não há confirmação de integração com meios de pagamento, emissão fiscal ou equipamentos de PDV.

### 4.8 Controle de funcionários

**Objetivo:** organizar o cadastro e a consulta de colaboradores.

Escopo previsto:

- Listagem de funcionários.
- Cadastro e atualização de informações.
- Pesquisa e organização dos registros.

**Situação:** módulo abordado nos protótipos; permissões, dados obrigatórios e integração com autenticação ainda precisam ser especificados.

### 4.9 Relatórios

**Objetivo:** apresentar informações gerenciais para acompanhamento da operação.

Relatórios previstos:

- Produtos e estoque.
- Vendas por período.
- Produtos com maior saída.
- Itens com validade próxima.
- Demandas e necessidades de reposição.

**Situação:** módulo previsto; disponibilidade de filtros, exportação e indicadores depende dos dados efetivamente registrados.

## 5. Navegação e experiência de uso

A aplicação utiliza menu lateral para acesso aos módulos. A interface de referência possui:

- **Azul-marinho:** cabeçalho e navegação lateral.
- **Verde:** ações, seleção de menu e indicadores de produto.
- **Fundo claro:** conteúdo principal.
- **Cartões, tabelas e gráficos:** informações operacionais.

O layout deve se adaptar a telas desktop e móveis, mantendo menus e formulários acessíveis.

## 6. Estrutura de diretórios sugerida

```text
supermercado-sao-joao/
├── index.html
├── README.md
├── assets/
│   └── img/
├── css/
│   └── style.css
└── js/
    └── app.js
```

Essa estrutura é **sugerida para unificação**. Os protótipos já entregues podem utilizar `index.html`, `style.css` e `app.js` na mesma pasta; ajuste os caminhos dos arquivos conforme a organização real.

## 7. Como executar o protótipo

### Pré-requisitos

- Navegador atualizado (Chrome, Edge ou Firefox).
- Editor de código, como VS Code (recomendado).
- Extensão Live Server (opcional).
- Conexão com a internet caso o Bootstrap seja carregado por CDN.

### Passo a passo

1. Extraia os arquivos do projeto em uma pasta.
2. Abra essa pasta no VS Code.
3. Confirme que os caminhos do CSS e JavaScript no HTML estão corretos.
4. Abra o `index.html` diretamente no navegador ou execute-o com o Live Server.
5. Navegue pelas funcionalidades implementadas no protótipo.

Exemplo de referências para arquivos na mesma pasta:

```html
<link rel="stylesheet" href="style.css">
<script src="app.js" defer></script>
```

Para a estrutura sugerida com subpastas, use `css/style.css` e `js/app.js`.

## 8. Regras de negócio propostas

Estas regras precisam ser confirmadas e implementadas no sistema integrado:

1. Cada produto deve possuir um identificador único.
2. O preço de venda não pode ser negativo.
3. A quantidade em estoque não pode ser negativa.
4. Uma venda concluída deve descontar do estoque a quantidade vendida.
5. O sistema não deve concluir uma venda quando não houver quantidade suficiente, salvo se uma política específica permitir.
6. Produtos vencidos devem ser sinalizados de maneira distinta dos próximos do vencimento.
7. O histórico de movimentações deve permitir rastrear entradas, saídas e ajustes quando houver backend.
8. Os relatórios devem utilizar os mesmos dados operacionais usados nos demais módulos.

## 9. Dados e persistência

Nos protótipos, os registros podem ser mantidos em memória ou no `localStorage` do navegador. Isso é adequado para demonstrações, mas possui limitações:

- Os dados não são compartilhados entre dispositivos.
- A limpeza do armazenamento do navegador pode apagar os registros.
- Não há controle de concorrência entre caixas ou usuários.
- Não existe autenticação corporativa nem trilha de auditoria confiável.

Para uso operacional real, será necessário definir backend, banco de dados, autenticação, autorização e rotinas de backup.

## 10. Segurança e privacidade

Antes da implantação real, devem ser previstos:

- Autenticação e controle de acesso por função.
- Validação dos dados no servidor.
- Proteção contra injeção de comandos e scripts maliciosos.
- HTTPS e gerenciamento seguro de credenciais.
- Registro de operações críticas.
- Backup e recuperação de dados.
- Tratamento adequado de dados pessoais de funcionários e usuários, conforme a LGPD.

O `localStorage` não deve armazenar senhas ou informações sensíveis.

## 11. Testes recomendados

| Cenário | Resultado esperado |
| --- | --- |
| Cadastrar produto válido | Produto aparece na listagem |
| Cadastrar produto sem nome | Formulário rejeita o envio |
| Informar preço negativo | Operação é bloqueada |
| Pesquisar por nome | Lista mostra itens correspondentes |
| Editar produto | Informações são atualizadas |
| Excluir produto | Registro deixa de aparecer após confirmação |
| Registrar venda | Total é calculado corretamente |
| Vender acima do estoque | Operação é rejeitada |
| Consultar vencidos | Produtos vencidos são identificados |
| Abrir em celular | Layout permanece legível e navegável |

Esses são **casos de teste planejados**, não resultados de testes automatizados executados.

## 12. Roadmap

- [x] Definir a identidade visual inicial.
- [x] Criar referências visuais para Dashboard e Validade.
- [x] Desenvolver protótipo do módulo Produtos.
- [ ] Unificar as telas em uma única navegação funcional.
- [ ] Concluir os módulos de Insumos e Demandas.
- [ ] Concluir Validade e Alertas de Estoque.
- [ ] Implementar o fluxo completo de Caixa e PDV.
- [ ] Concluir Controle de Funcionários e Relatórios.
- [ ] Definir a arquitetura de backend e banco de dados.
- [ ] Implementar autenticação e autorização.
- [ ] Integrar os módulos a dados persistentes.
- [ ] Criar testes automatizados e documentação da API.
- [ ] Preparar implantação e operação segura.

## 13. Limitações atuais

Este projeto ainda está em evolução. Nem todas as telas compartilham um banco de dados, e os indicadores presentes nas imagens podem ser valores ilustrativos. A existência de uma tela ou botão não comprova que a respectiva rotina esteja integrada e pronta para uso em produção.

## 14. Licença e autoria

Projeto: **Supermercado São João**.

Autoria e licença de distribuição: **a definir pelo responsável pelo projeto**. Este documento não concede automaticamente licença de uso comercial ou redistribuição.

---

**Última atualização da documentação:** novembro de 2026.
