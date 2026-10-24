# PROMPT — CRIAÇÃO DE UMA APLICAÇÃO WEB DE E-COMMERCE DE PETZ SHOP ONLINE, UTILIZANDO A IA GENERATIVA

## 1. Papel da IA

Atue como um desenvolvedor web sênior, especialista em HTML5, CSS3, JavaScript, UX/UI, responsividade, acessibilidade e regras de negócio de comércio eletrônico.

Seu objetivo é criar uma aplicação web de e-commerce funcional, organizada e visualmente profissional, utilizando exclusivamente tecnologias executadas no navegador.

**RESTRIÇÃO OBRIGATÓRIA: NÃO CRIE TESTES AUTOMATIZADOS.**

Não gere arquivos de testes, scripts de testes, testes unitários, testes de integração automatizados, testes end-to-end, configurações de frameworks de teste, pipelines de testes ou dependências destinadas à automação de testes.

Não utilize ferramentas ou frameworks como Jest, Vitest, Cypress, Playwright, Selenium, Mocha ou equivalentes.

A validação posterior da aplicação será realizada manualmente por um profissional de Quality Assurance (QA), utilizando técnicas, cenários, casos de teste e evidências documentadas fora do código-fonte da aplicação.

## 2. Contexto de negócio

Crie uma loja virtual fictícia chamada OrangeTech Store, especializada na venda de eletrônicos e acessórios tecnológicos para consumidores finais (B2C).

O público-alvo são pessoas que desejam pesquisar, comparar e comprar produtos tecnológicos por meio de computadores, tablets ou smartphones.

O objetivo é proporcionar uma experiência de compra simples, intuitiva, responsiva e consistente.

A aplicação será utilizada como projeto demonstrativo para praticar testes manuais de software, análise de riscos, identificação de defeitos e documentação de qualidade.

## 3. Requisitos técnicos obrigatórios

- Desenvolva a aplicação em um único arquivo chamado index.html.
- Utilize HTML5 para estruturar a aplicação.
- Coloque todo o CSS dentro de uma única tag style no próprio HTML.
- Coloque todo o JavaScript dentro de uma ou mais tags script no mesmo HTML.
- Não crie arquivos externos de CSS ou JavaScript.
- Não utilize frameworks de interface como React, Angular ou Vue.
- Não exija instalação de dependências, compilação ou servidor de aplicação para a demonstração básica.
- Utilize localStorage para preservar dados não sensíveis entre sessões, como carrinho e preferências.
- Trate erros de leitura e gravação no armazenamento local.
- Não armazene senhas, dados financeiros ou informações pessoais desnecessárias.
- A aplicação deverá funcionar nos navegadores modernos e adaptar-se a telas desktop e mobile.
- Não utilize APIs externas obrigatórias para que as funcionalidades essenciais funcionem.
- Caso utilize imagens externas, forneça alternativas visuais ou placeholders para situações em que as imagens não carreguem.
- Utilize dados de produtos fictícios e valores em reais (R$).

## 4. Identidade visual e experiência do usuário

Adote um tema escuro com tons de laranja como cor de destaque.

Referência visual:
- Fundo principal: grafite ou quase preto.
- Cards e painéis: cinza-escuro.
- Cor de destaque: laranja.
- Textos principais: branco ou cinza-claro.
- Textos secundários: cinza com contraste suficiente.
- Botões primários: laranja com texto legível.
- Estados de sucesso, atenção e erro: cores distintas e acessíveis.

Utilize layout moderno, espaçamento consistente, tipografia legível, cards de produtos, ícones compreensíveis e feedback visual para as ações do usuário.

Garanta navegação por teclado, foco visível, rótulos para campos, mensagens de validação acessíveis e contraste adequado.

## 5. Funcionalidades obrigatórias

### 5.1 Página inicial
- Cabeçalho com logotipo OrangeTech Store.
- Campo de pesquisa.
- Navegação por categorias.
- Acesso ao carrinho com indicador de quantidade de itens.
- Área de destaque para produtos e ofertas.
- Catálogo com produtos fictícios.

### 5.2 Catálogo de produtos
- Exibir pelo menos 12 produtos fictícios.
- Utilizar categorias como smartphones, notebooks, áudio, periféricos e acessórios.
- Exibir nome, imagem ou placeholder, preço, categoria e disponibilidade.
- Disponibilizar botão para adicionar ao carrinho.
- Exibir indicação de indisponibilidade quando o estoque estiver zerado.

### 5.3 Pesquisa, filtros e ordenação
- Pesquisar produtos por nome.
- Filtrar por categoria.
- Filtrar por faixa de preço.
- Ordenar por menor preço, maior preço e nome.
- Exibir mensagem adequada quando nenhum produto corresponder à pesquisa.
- Permitir limpar os filtros.

### 5.4 Detalhes do produto
- Exibir descrição completa.
- Exibir preço e disponibilidade.
- Permitir selecionar quantidade respeitando o estoque.
- Permitir adicionar o produto ao carrinho.
- Validar dados e quantidades antes de atualizar o carrinho.

### 5.5 Carrinho de compras
- Adicionar produtos.
- Remover produtos.
- Aumentar ou diminuir quantidades.
- Impedir quantidades inválidas ou superiores ao estoque.
- Atualizar subtotal e total automaticamente.
- Exibir o estado vazio do carrinho.
- Preservar o carrinho após atualização da página.
- Disponibilizar opção para esvaziar o carrinho mediante confirmação.
- Evitar produtos duplicados como linhas independentes quando puderem ser agrupados pelo mesmo identificador.

### 5.6 Frete
- Disponibilizar campo para CEP.
- Validar o formato do CEP.
- Simular o cálculo do frete com regras locais claramente definidas.
- Informar prazo estimado fictício.
- Recalcular o total quando o frete for alterado.
- Não afirmar que o prazo ou o valor representam uma cotação real.

### 5.7 Checkout e finalização da compra
- Apresentar resumo dos produtos, quantidades, subtotal, frete e total.
- Solicitar apenas os dados fictícios necessários para a demonstração.
- Validar campos obrigatórios, formatos e dados inconsistentes.
- Oferecer formas de pagamento apenas como opções simuladas.
- Não solicitar nem armazenar número real de cartão, código de segurança ou senha bancária.
- Apresentar uma etapa de revisão antes da confirmação.
- Permitir concluir uma compra simulada.
- Gerar um identificador de pedido demonstrativo.
- Exibir confirmação de pedido com resumo da compra.
- Não realizar cobranças nem integrações financeiras reais.
- Não concluir uma compra com carrinho vazio ou estoque insuficiente.

### 5.8 Histórico de pedidos
- Registrar pedidos fictícios no localStorage.
- Exibir os pedidos simulados e seus itens.
- Permitir consultar os detalhes de um pedido.
- Tratar a ausência de histórico.
- Evitar duplicação do mesmo pedido em decorrência de cliques repetidos na confirmação.

### 5.9 Feedback e tratamento de erros
- Exibir mensagens de sucesso, atenção e erro.
- Impedir ações inválidas.
- Oferecer estados de carregamento quando fizer sentido.
- Exibir mensagens compreensíveis em vez de erros técnicos diretamente ao usuário.
- Tratar dados inválidos, armazenamento indisponível e ausência de produtos.
- Solicitar confirmação para ações destrutivas.

## 6. Regras de negócio

- Cada produto deve possuir identificador único, nome, categoria, preço, descrição, imagem ou placeholder e estoque.
- Preços e totais devem ser calculados de maneira consistente, preferencialmente utilizando valores inteiros em centavos para evitar imprecisões monetárias.
- O total deverá corresponder ao subtotal mais o frete, considerando as regras demonstrativas.
- A quantidade de cada item deve ser um número inteiro positivo.
- O estoque nunca poderá ser ultrapassado por uma operação válida.
- Uma compra simulada deverá reduzir o estoque da demonstração e atualizar os dados persistidos.
- As alterações no carrinho devem atualizar imediatamente a interface.
- Dados inválidos no localStorage não podem impedir a aplicação inteira de funcionar.
- As mensagens de confirmação deverão refletir o resultado efetivo da operação.
- Dados persistidos devem ser tratados como não confiáveis e validados antes do uso.
- Não simule segurança de backend: regras implementadas apenas no navegador não garantem integridade contra manipulação pelo usuário.

## 7. Arquitetura e organização do código

Embora tudo esteja em um único arquivo HTML, organize o código de forma clara.

Separe logicamente:
- Dados e catálogo de produtos.
- Estado atual da aplicação.
- Funções de persistência.
- Renderização da interface.
- Pesquisa, filtros e ordenação.
- Operações do carrinho.
- Cálculos de subtotal, frete e total.
- Validação dos formulários.
- Checkout e criação de pedidos.
- Mensagens e tratamento de erros.

Utilize nomes de variáveis e funções claros, evite duplicação de código e mantenha as regras de negócio separadas da manipulação visual sempre que possível.

Não utilize eval ou execução de código proveniente de entradas do usuário. Evite inserir entradas não confiáveis diretamente por meio de innerHTML.

## 8. Responsividade

A aplicação deverá funcionar em:
- Desktop.
- Notebook.
- Tablet.
- Smartphone.

Utilize CSS responsivo e media queries.

No mobile:
- Ajuste a grade de produtos.
- Evite rolagem horizontal desnecessária.
- Mantenha botões e campos fáceis de utilizar por toque.
- Adapte navegação, carrinho e checkout à largura da tela.
- Garanta legibilidade e acessibilidade dos conteúdos.

## 9. Restrições de escopo

Não implemente:
- Testes automatizados de qualquer natureza.
- Frameworks de testes ou arquivos de configuração de testes.
- Backend ou banco de dados remoto.
- Autenticação real.
- Pagamentos reais.
- Integração obrigatória com serviços externos.
- Coleta de dados pessoais desnecessários.

Não confunda uma compra simulada com uma transação comercial real.

## 10. Entrega esperada

Entregue o conteúdo integral do arquivo index.html, incluindo HTML, CSS e JavaScript.

O arquivo deverá poder ser salvo localmente e aberto em um navegador moderno.

Antes de apresentar a entrega:
- Revise a consistência entre as funcionalidades implementadas e os requisitos.
- Verifique se todas as funcionalidades essenciais estão conectadas aos respectivos controles da interface.
- Revise as regras de negócio e o tratamento de erros.
- Confira a utilização do localStorage.
- Confira o comportamento responsivo.
- Remova referências a testes automatizados e dependências desnecessárias.
- Não afirme que a aplicação foi executada ou validada em navegadores reais se isso não tiver ocorrido.

Não crie nem execute testes automatizados. A validação funcional será realizada manualmente posteriormente.

Apresente primeiro uma breve descrição da arquitetura e das limitações da solução. Em seguida, entregue o código completo do arquivo index.html.

Ao final, apresente uma lista de funcionalidades implementadas e instruções simples para abrir a aplicação localmente.
