# Supermercado São João — Dashboard com leitor integrado

Abra `dashboard.html` no navegador. No menu **Operação**, escolha **Leitor de Código de Barras**.

Arquivos: `dashboard.html`, `style.css`, `app.js`. Todas as telas anteriores continuam no mesmo projeto.

O leitor consulta o mesmo cadastro de produtos mantido pelo dashboard em `localStorage` (`sj_products_v1`). Não cria um cadastro paralelo. Para testar, use o código **001** (Arroz Branco 1kg) ou outro código existente no Cadastro. O campo aceita códigos digitados e scanners USB que emulam teclado e enviam Enter.

A câmera é opcional e depende de `BarcodeDetector`, permissão de câmera e HTTPS ou localhost. Alguns navegadores não oferecem essa API. O histórico de leituras é temporário e não altera quantidades de estoque.

O sistema continua como protótipo front-end com armazenamento local; não está conectado ao Flask/SQL.
