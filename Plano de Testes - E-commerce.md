## **Plano de Testes E-commerce** 


### 1. **Introdução:**

**Descrição do sistema:** O E-commerce permitirá a compra de produtos online.

**Objetivos dos testes:** Garantir que o sistema de e-commerce funcione corretamente, permitindo que o usuário possa utilizar as funcionalidades de login, navegação, busca de produtos, compra e pagamento.

<br>

**Escopo dos Testes:**

<br>

**Funcionalidades não inclusas:**

* Login com diferentes tipos de usuários disponíveis  
* Ordenação e filtragem de produtos  
* Fluxo completo de compra (do carrinho até finalização)  
* Remoção de itens do carrinho  
* Navegação entre páginas  
* Logout

<br>

**Funcionalidades não inclusas:**

* Integração com sistemas externos como gestão de estoque  
* Integração com aplicativos de marketing

<br>

### 2. **Metodologia e Ferramentas:**  

<br>

**Metodologia:** Teste Ágil com ciclos de iteração de duas semanas.

**Ferramentas:** Cypress para automação de testes de interface.

<br>

### 3. **Casos de Teste:**

<br>

**Cenário 1: Login**

<br>

**Caso de Teste 1.1: Login com dados válidos**

<br>

* **Descrição:** O usuário insere um “Username” válido e um “Password” válido, realiza o login e é redirecionado à página inicial.

* **Pré-condições:** Credenciais válidas previamente cadastradas.

* **Resultado Esperado:** O login é realizado com sucesso.

<br>

**Caso de Teste 1.2: Login com dados inválidos**

<br>

* **Descrição:** O usuário insere um “Username” correto, mas uma senha inválida.

* **Pré-condições:** Usuário cadastrado na plataforma.

* **Resultado Esperado:** O sistema exibe uma mensagem de erro: *"Epic sadface: Username and password do not match any user in this service"*.

<br>

**Cenário 2: Ordenação e filtragem de produtos**

<br>

**Caso de Teste 2.1: Ordenação de produtos por preço crescente**

<br>

* **Descrição:** O usuário ordena os produtos com a opção "Preço: do menor para o maior".

* **Pré-condições:** A lista de produtos possui itens com diferentes faixas de preço.

* **Resultado Esperado:** Os produtos são exibidos em ordem crescente de preços.

<br>

**Caso de Teste 2.2: Ordenação de produtos por preço decrescente**

<br>

* **Descrição:** O usuário ordena os produtos com a opção "Preço: do maior para o menor".

* **Pré-condições:** A lista de produtos possui itens com diferentes faixas de preço.

* **Resultado Esperado:**  Os produtos são exibidos em ordem crescente de preços.

<br>

**Caso de Teste 2.3: Ordenação de produtos por ordem alfabética**

<br>

* **Descrição:** O usuário ordena os produtos com a opção "Nome: A to Z".

* **Pré-condições:** A lista de produtos possui itens com diferentes nomes.

* **Resultado Esperado:**  Os produtos são exibidos em ordem alfabética.
  
<br> 

**Caso de Teste 2.4: Filtragem de produtos**

<br>

* **Descrição:** O usuário filtra os produtos pelas características e variações

* **Pré-condições:** Os produtos possuem características cadastradas no backend.

* **Resultado Esperado:**  Os produtos podem ser filtrados na lista de produtos.

<br>

**Cenário 3:  Fluxo completo de compra (do carrinho até finalização)**

<br>

**Caso de Teste 3.1: Adicionar produto no carrinho através da Página Inicial**

<br>

* **Descrição:** O usuário clica em “Add to cart” na Página Inicial.

* **Pré-condições:** O usuário está na página inicial, visualizando todos os produtos.

* **Resultado Esperado:**  O produto é adicionado no carrinho.  

<br>

**Caso de Teste 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**  

<br>

* **Descrição:** O usuário clica em “Add to cart” na Página de Detalhes do Produto.

* **Pré-condições:** O usuário está na página de detalhes do produto.

* **Resultado Esperado:**  O produto é adicionado no carrinho

<br>

**Caso de Teste 3.3: Finalização de compra com cartão de crédito válido**

<br>

* **Descrição:** O usuário adiciona itens ao carrinho, seleciona o método de pagamento por cartão de crédito válido e conclui a compra.

* **Pré-condições:** O carrinho possui itens, e os dados do cartão são válidos.

* **Resultado Esperado:** O pedido é concluído, e uma mensagem de sucesso com o número do pedido é exibida.

<br>

**Cenário 4: Remoção de itens do carrinho**

<br>

**Caso de Teste 4.1: Remoção de um item específico**

<br>

* **Descrição:** O usuário remove um item do carrinho clicando no botão "Remover" ao lado do produto.

* **Pré-condições:**  O carrinho possui ao menos dois itens.

* **Resultado Esperado:**  O item é removido, e o subtotal do carrinho é atualizado.

<br>

**Caso de Teste 4.2:  Remoção de todos os itens do carrinho**

<br>

* **Descrição:** O usuário clica em "Remove" na Lista de Produtos da página inicial.

* **Pré-condições:**  O produto está adicionado no carrinho..

* **Resultado Esperado:** O item é removido do carrinho.

<br>

**Cenário 5: Navegação entre Páginas**

<br>

**Caso de Teste 5.1: Navegar no menu lateral** 

<br>

* **Descrição:** O usuário clica no link da página "About" no menu lateral  
    
* **Pré-condições:**  Estar na página inicial ou na página de detalhes do produto.

* **Resultado Esperado:** A próxima página “About” é exibida, com informações sobre a empresa.

<br>

**Caso de Teste 5.2: Retornar da Página de um Produto à Página Inicial**

<br>

* **Descrição:** O usuário clica no botão "Back to products" para voltar à página anterior da listagem.

* **Pré-condições:**  O usuário está em uma página de detalhes de um produto.

* **Resultado Esperado:** Os produtos da página inicial são exibidos corretamente.

<br>

**Caso de Teste 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

<br>

* **Descrição:** O usuário clica no botão "Continue Shopping" para voltar à página anterior da listagem.

* **Pré-condições:**  O usuário está na página do Carrinho de Compras.

* **Resultado Esperado:** Os produtos da página inicial são exibidos corretamente e usuário pode continuar comprando.

<br>

**Caso de Teste 5.4: Retornar à primeira página do Carrinho de Compras**

<br>

* **Descrição:** O usuário clica no botão "Cancel" para voltar à página do Carrinho de compras.  
    
* **Pré-condições:**  O usuário está na página do primeiro passo do Checkout.

* **Resultado Esperado:** A página do Carrinho de Compras é exibida. 

<br>

**Cenário 6\. Logout**

<br>

**Caso de Teste 6.1: Logout pelo menu de usuário**

* **Descrição:** O usuário clica no botão "Logout" no menu lateral para encerrar a sessão.

* **Pré-condições:**  Usuário está logado.

* **Resultado Esperado:** O sistema encerra a sessão e redireciona o usuário para a página de login.

<br>

**Caso de Teste 6.2: Acesso a página protegida após logout**

<br>

* **Descrição:** O usuário tenta acessar uma página protegida após realizar o logout.

* **Pré-condições:**  Usuário não está logado.

* **Resultado Esperado:** O sistema não deve permitir o acesso e deve exibir a mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in".

<br>

### 4. **Cronograma de Testes:**

<br>

* **Semana 1:** Preparação do ambiente de testes, criação dos casos de teste e revisão da documentação.  
* **Semana 2:** Execução dos testes manuais e automatizados, análise dos resultados e correção de defeitos encontrados.

<br>

### 5. **Equipe de Testes:**

<br>

* Testador  
* Analista de Qualidade  
* Tech Lead 

<br>

### 6. **Critérios de Aceitação:**

<br>

* Todos os casos de teste devem ser executados sem erros.  
* As funcionalidades de login, ordenação de produtos, fluxo de compra, remoção de produtos, navegação entre páginas e logout devem atender aos requisitos especificados.

<br>

### 7. **Considerações Finais:**

<br>

Ao final dos testes, será gerado um relatório detalhado com os resultados, relatório de bugs e recomendações de melhoria para a equipe de Desenvolvimento.

<br>


## **Resultados dos testes executados** 

<br>

**Funcionalidade: Login**

<br>

Como um usuário    
Quero fazer login no sistema  **Swag Labs**  
Para acessar minhas informações e funcionalidades personalizadas

<br>

**Caso de Teste 1.1: Login com dados válidos**

<br>

Dado que estou na página de login    
Quando eu insiro um usename válido "standard\_user"    
E eu insiro um password válido "secret\_sauce"    
E clico no botão “Login"  
Então devo ser redirecionado para a página inicial  

<br>

**Resultado da Execução:** 

O usuário foi redirecionado corretamente para a página inicial.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 1.2: Login com dados inválidos**

<br>

Dado que estou na página de login    
Quando eu insiro um usename válido "standard\_user"  
E eu insiro uma senha inválida "secret\_sauce1"    
E clico no botão "Login"    
Então devo ver a mensagem de erro "Epic sadface: Username and password do not match any user in this service"    
E devo permanecer na página de login  

<br>

**Resultado da Execução:**

O sistema exibiu a mensagem correta de erro.  
O usuário permaneceu na página de login.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Evidência:**

Tela Login

**![Imagem1](https://github.com/user-attachments/assets/599a9968-b76f-44db-883a-907e74f4f4a7)**

<br>

**Funcionalidade: Ordenação e filtragem de produtos**

<br>

Como um usuário    
Quero ordenar os produtos conforme opções disponíveis

<br>

**Caso de Teste 2.1: Ordenação de produtos por preço crescente**

<br>

Dado que estou na página Products   
Quando eu seleciono a opção "Price: low to high" no menu de ordenação  
Então os produtos devem ser exibidos em ordem crescente de preço  
E o primeiro produto deve ser o de menor preço disponível

<br>

**Resultado da Execução:**

Os produtos de menor valor aparecem no topo da lista.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 2.2: Ordenação de produtos por preço decrescente**  

<br>

Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Price: high to low" no menu de ordenação  
Então os produtos devem ser exibidos em ordem decrescente de preço  
E o primeiro produto deve ser o de maior preço disponível

<br>

**Resultado da Execução:**

Os produtos de maior valor aparecem no topo da lista.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 2.3: Ordenação de produtos por ordem alfabética**

<br>

Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Name: A to Z" no menu de ordenação  
Então os produtos devem ser exibidos em ordem alfabética  
E o primeiro produto deve ser exibido na ordem de A a Z.

<br>

**Resultado da Execução:**

Os produtos são exibidos por ordem alfabética de A a Z.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 2.4: Filtragem de produtos**

<br>

Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Filtrar"  
Então as características do produto são exibidas

<br>

**Resultado da Execução:**

Funcionalidade não disponível.

**Status:** Bloqueado.

**Observações:** Existe apenas a opção de ordenar produtos, mas não aparecem opções de filtragem com as características ou variações de cor, tamanho, material.

<br>

**Funcionalidade:  Fluxo completo de compra (do carrinho até finalização)**

<br>

Como um usuário    
Quero adicionar produtos ao carrinho  
Para realizar uma compra com cartão de crédito  
    
<br>
    
**Caso de Teste 3.1: Adicionar produto no carrinho através da Página Inicial**

<br>

Dado que estou na página Products de listagem de produtos    
Quando eu visualizo os produtos disponíveis  
E clico no botão “Add to cart" do produto desejado  
Então o produto deve ser adicionado ao carrinho  

<br>

**Resultado da Execução:**

O produto foi adicionado ao carrinho. 

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**

<br>

Dado que estou na página de Detalhes do Produto   
Quando eu clico no botão “Add to cart"  
Então o produto deve ser adicionado ao carrinho

<br>

**Resultado da Execução:**

O produto foi adicionado ao carrinho. 

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 3.3: Finalização de compra com cartão de crédito válido**

<br>

 Dado que adicionei um produto ao carrinho    
 E cliquei no botão "Checkout"    
 E preenchi os dados pessoais e de entrega válidos  
 E clico em “Continue”    
 Quando eu insiro os dados de um cartão de crédito válido    
 E clico no botão "Finish"    
 Então o sistema deve exibir a mensagem de agradecimento:   
*"Thank you for your   order\!"*

<br>

**Resultado da Execução:**

O pedido foi finalizado com sucesso e a mensagem de agradecimento exibida.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Evidência:**

Tela Checkout Passo 3

**![Imagem2](https://github.com/user-attachments/assets/6ab87ef8-918e-4b3d-9c02-deeb72dc0308)**  

<br>

**Funcionalidade: Remoção de itens do carrinho**

<br>

Como um usuário    
Quero remover produtos do carrinho    
Para ajustar minha seleção de itens antes de finalizar a compra  

<br>

**Caso de Teste 4.1: Remoção de um item específico**

<br>

 Dado que tenho um produto no carrinho  
 Quando eu clico no botão "Remover" ao lado do produto  
 Então o produto deve ser removido do carrinho  
 E o carrinho deve exibir a mensagem "Seu carrinho está vazio"

<br>

**Resultado da Execução:**

O produto foi removido corretamente do carrinho.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 4.2:  Remoção de todos os itens do carrinho**

<br>

Dado que tenho um produto no carrinho  
Quando eu clico no botão "Remover"   
Então o carrinho deve aparecer vazio 

<br>

**Resultado da Execução:**

Todos os produtos foram removidos corretamente.   

**Status:** Aprovado.

**Observações:** Não é exibida nenhuma mensagem avisando que o carrinho está vazio.

<br>

**Funcionalidade: Navegação entre Páginas**

<br>

Como um usuário    
Quero poder navegar entre as páginas da loja   
Para explorar melhor os produtos antes de finalizar a compra

<br>

**Caso de Teste 5.1: Navegar no menu lateral e Visitar a Página “About”**

<br>

Dado que estou na Página inicial  
E quero visitar a página “About” para conhecer a empresa  
Quando eu clico no link  
Então a página redireciona para a página “About”

<br>

**Resultado da Execução:** 

O sistema não redireciona para a página “About”**.**

**Status:** Reprovado.

**Observações:** A página redireciona para uma página institucional da empresa e o login é encerrado.

**Evidências:**

Tela Menu Lateral Aberto

**![Imagem3](https://github.com/user-attachments/assets/26e443f5-6244-481d-8278-faa89a979e60)**

Página institucional da Empresa

**![Imagem4](https://github.com/user-attachments/assets/b13f44a6-3984-4658-9425-b96656dec91c)**

<br>

**Caso de Teste 5.2: Retornar da Página de um Produto à Página Inicial**

<br>

Dado que estou na página de detalhes de um produto    
Quando eu clico no botão "Back to Products"    
Então devo ser redirecionado para a página inicial    
E a página inicial deve carregar corretamente com todos os produtos listados  

<br>

**Resultado da Execução:** 

A navegação pelo botão "Back to products" funcionou corretamente.    
A página inicial carregou com a lista de produtos exibida corretamente.    
  
**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

<br>

Dado que estou na página do Carrinho de Compras
Quando eu clico no botão "Continue Shopping"    
Então devo ser redirecionado para a página inicial
E a página inicial deve carregar corretamente com todos os produtos listados  

<br>

**Resultado da Execução:**

A navegação pelo botão "Continue Shopping" funcionou corretamente.    
A página inicial carregou com a lista de produtos exibida corretamente.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 5.4: Retornar do Checkout à primeira página do Carrinho de Compras**

<br>

Dado que estou na página da primeira fase do Checkout    
Quando eu clico no botão "Cancel"    
Então devo ser redirecionado para a página do Carrinho de Compras    
E a página inicial deve carregar corretamente os produtos que estão no carrinho de compras

<br>

**Resultado da Execução:**

A navegação pelo botão "Cancel” funcionou corretamente.    
A página do Carrinho de Compras carregou os produtos corretamente.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Funcionalidade: Logout**

<br>

Como um usuário autenticado  
Quero sair da minha conta   
Para proteger minhas informações pessoais

<br>

**Caso de Teste 6.1: Logout pelo menu principal**

<br>

 Dado que estou logado no sistema    
 Quando eu clico no botão  "Logout"    
 Então devo ser redirecionado para a página de login    
 E minha sessão deve ser encerrada    

<br>

## **Resultado da Execução:**

 O botão "Logout" redirecionou corretamente para a página de login.    
 A sessão foi encerrada.    
  
**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>

**Caso de Teste 6.2: Acesso a página protegida após logout**

<br>

Dado que realizei logout    
Quando eu tento acessar diretamente a URL [https://www.saucedemo.com/inventory.html](https://www.saucedemo.com/inventory.html) de uma página protegida    
Então devo ser redirecionado para a página de login    
E a mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in." deve ser exibida

<br>

**Resultado da Execução:**

O sistema redirecionou corretamente para a página de login ao tentar acessar a URL protegida.  

A mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in." foi exibida.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

<br>
    
## **Sugestões de melhorias de UX/UI**

<br>

**Funcionalidade: Filtro de produtos**

Não existe um filtro para escolher cores, tamanhos e características do produto, como material ou estampa. Existe apenas a opção de ordenar os produtos, porém, aparecem todos os itens. Ao criar filtros, seria possível visualizar itens que possuem as características selecionadas.

Tela Inicial da Lista de Produtos

![][image26]

Tela Inicial da Lista de Produtos

![][image27]

**Funcionalidade: Página de Detalhes do Produto**

Na página de detalhes do produto,  não existe opção para exibir produtos relacionados, através de um carrossel de produtos. 

Página de Detalhes do Produto

![][image28]

**Funcionalidade:**

No menu principal não existem categorias para segmentar os produtos e orientar melhor o usuário na localização dos produtos desejados, separados por Acessórios, Roupas, Equipamentos, etc.

Tela do Menu de Navegação

![][image29]

**Funcionalidade: Carrinho de compras**

Não existe a opção de abrir uma miniatura do carrinho de compras, para visualizar os produtos que já estão no carrinho ou confirmar visualmente o produto que foi inserido por último.

Tela de Detalhes do Produto

![][image30]

**Funcionalidade: Carrinho de Compras Vazio**

Após a remoção de todos os itens do carrinho de Compras, não é exibida nenhuma mensagem informando "Seu carrinho está vazio”, para orientar melhor o usuário sobre o sucesso na remoção.

Página do Carrinho de compras

![][image31]

**Funcionalidade: Cálculo do Frete**

Não existe uma calculadora de frete na página de detalhes do produto ou primeira fase do checkout:

Página de detalhes do produto

![][image32]

Página de início do Checkout

![][image33]

**Funcionalidade: Carrinho de Compras**

O carrinho de compras não exibe o subtotal do pedido para o usuário visualizar uma prévia do valor a pagar.

**![][image34]**

<br>

## **Lista de bugs encontrados**

<br>

**CT 5.1: Navegar no menu lateral e Visitar a Página “About”**

**Resultado da Execução:** O sistema não redireciona para a página “About”**.**

**Status:** Reprovado.

**Evidência:**  

Vídeo:[https://www.loom.com/share/671fc7b50ba347dfa4bb08da385d677f?sid=cd6f0add-2512-45d6-a465-b4f2953e5763](https://www.loom.com/share/671fc7b50ba347dfa4bb08da385d677f?sid=cd6f0add-2512-45d6-a465-b4f2953e5763)

<br>

## **Análise de Riscos** 

<br>

A aplicação não apresentou bugs de segurança, desempenho ou que possam causar impactos. Mas os riscos podem surgir devido a fatores externos, limitações técnicas ou mudanças no ambiente. 

Foi criada uma [Matriz de Rastreabilidade](https://docs.google.com/spreadsheets/d/169p11Ng1BhybtgCTZazmprV3Bo9662xw5bhbdhWaNYA/edit?gid=0#gid=0) para classificar os Casos de Testes e mapear os tipos de teste, prioridade, etc.e abaixo temos o resumo: 

<br>

**CT 1.1: Login com dados válidos**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Login
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 1.2: Login com dados inválidos**

<br>

Tipo de Teste: Funcional Negativo
Funcionalidade Associada: Login
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P2
Versão: V1.0

<br>

**CT 2.1: Ordenação de produtos por preço crescente**

<br>

Tipo de Teste: Usabilidade
Funcionalidade Associada: Ordenação e filtragem de produtos
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P3
Versão: V1.0

<br>

**CT 2.2: Ordenação de produtos por preço decrescente**

<br>

Tipo de Teste: Usabilidade
Funcionalidade Associada: Ordenação e filtragem de produtos
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P3
Versão: V1.0

<br>

**CT 2.3: Ordenação de produtos por ordem alfabética**

<br>

Tipo de Teste: Usabilidade
Funcionalidade Associada: Ordenação e filtragem de produtos
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P3
Versão: V1.0

<br>

**CT 2.4: Filtragem de produtos**

<br>

Tipo de Teste: Usabilidade
Funcionalidade Associada: Ordenação e filtragem de produtos
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P3
Versão: V1.0

<br>

**CT 3.1: Adicionar produto no carrinho através da Página Inicial**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Fluxo de compra
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Fluxo de compra
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

**CT 3.3: Finalização de compra com cartão de crédito válido**

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Fluxo de compra
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 4.1: Remoção de um item específico**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Remoção de Produtos do carrinho
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 4.2: Remoção de todos os itens do carrinho**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Remoção de Produtos do carrinho
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 5.1: Navegar no menu lateral**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Navegação
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P2
Versão: V1.0

<br>

**CT 5.2: Retornar da Página de um Produto à Página Inicial**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Navegação
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P2
Versão: V1.0

<br>

**CT 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Navegação 
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 5.4: Retornar à primeira página do Carrinho de Compras**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Navegação 
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 6.1: Logout pelo menu principal**

<br>

Tipo de Teste: Funcional Positivo
Funcionalidade Associada: Logout
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0

<br>

**CT 6.2: Acesso a página protegida após logout**

<br>

Tipo de Teste: Funcional Negativo
Funcionalidade Associada: Logout
Passível de Automação: Sim
Regressivo Obrigatório: Sim
Prioridade: P1
Versão: V1.0
