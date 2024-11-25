## **Plano de Testes \- E-commerce** 

### 1. **Introdução:**

   **Descrição do sistema:** O E-commerce permitirá a compra de produtos online.

   
   **Objetivos dos testes:** Garantir que o sistema de e-commerce funcione corretamente, permitindo que o usuário possa utilizar as funcionalidades de login, navegação, busca de produtos, compra e pagamento.

   **Escopo dos Testes:**
   

**Funcionalidades não inclusas:**

* Login com diferentes tipos de usuários disponíveis  
* Ordenação e filtragem de produtos  
* Fluxo completo de compra (do carrinho até finalização)  
* Remoção de itens do carrinho  
* Navegação entre páginas  
* Logout

**Funcionalidades não inclusas:**

* Integração com sistemas externos como gestão de estoque  
* Integração com aplicativos de marketing

###2. **Metodologia e Ferramentas:**  
     
**Metodologia:** Teste Ágil com ciclos de iteração de duas semanas.

**Ferramentas:** Cypress para automação de testes de interface.

###3. **Casos de Teste:**

**Cenário 1: Login**
   
**Caso de Teste 1.1: Login com dados válidos**

* **Descrição:** O usuário insere um “Username” válido e um “Password” válido, realiza o login e é redirecionado à página inicial.

* **Pré-condições:** Credenciais válidas previamente cadastradas.

* **Resultado Esperado:** O login é realizado com sucesso.

**Caso de Teste 1.2: Login com dados inválidos**

* **Descrição:** O usuário insere um “Username” correto, mas uma senha inválida.

* **Pré-condições:** Usuário cadastrado na plataforma.

* **Resultado Esperado:** O sistema exibe uma mensagem de erro: *"Epic sadface: Username and password do not match any user in this service"*.

**Cenário 2: Ordenação e filtragem de produtos**

**Caso de Teste 2.1: Ordenação de produtos por preço crescente**

* **Descrição:** O usuário ordena os produtos com a opção "Preço: do menor para o maior".

* **Pré-condições:** A lista de produtos possui itens com diferentes faixas de preço.

* **Resultado Esperado:** Os produtos são exibidos em ordem crescente de preços.

**Caso de Teste 2.2: Ordenação de produtos por preço decrescente**

* **Descrição:** O usuário ordena os produtos com a opção "Preço: do maior para o menor".

* **Pré-condições:** A lista de produtos possui itens com diferentes faixas de preço.

* **Resultado Esperado:**  Os produtos são exibidos em ordem crescente de preços.

  **Caso de Teste 2.3: Ordenação de produtos por ordem alfabética**

* **Descrição:** O usuário ordena os produtos com a opção "Nome: A to Z".

* **Pré-condições:** A lista de produtos possui itens com diferentes nomes.

* **Resultado Esperado:**  Os produtos são exibidos em ordem alfabética.

	  
**Caso de Teste 2.4: Filtragem de produtos**

* **Descrição:** O usuário filtra os produtos pelas características e variações

* **Pré-condições:** Os produtos possuem características cadastradas no backend.

* **Resultado Esperado:**  Os produtos podem ser filtrados na lista de produtos.

**Cenário 3:  Fluxo completo de compra (do carrinho até finalização)**

**Caso de Teste 3.1: Adicionar produto no carrinho através da Página Inicial**

* **Descrição:** O usuário clica em “Add to cart” na Página Inicial.

* **Pré-condições:** O usuário está na página inicial, visualizando todos os produtos.

* **Resultado Esperado:**  O produto é adicionado no carrinho.  
    
  **Caso de Teste 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**  
        
* **Descrição:** O usuário clica em “Add to cart” na Página de Detalhes do Produto.

* **Pré-condições:** O usuário está na página de detalhes do produto.

* **Resultado Esperado:**  O produto é adicionado no carrinho

**Caso de Teste 3.3: Finalização de compra com cartão de crédito válido**

* **Descrição:** O usuário adiciona itens ao carrinho, seleciona o método de pagamento por cartão de crédito válido e conclui a compra.

* **Pré-condições:** O carrinho possui itens, e os dados do cartão são válidos.

* **Resultado Esperado:** O pedido é concluído, e uma mensagem de sucesso com o número do pedido é exibida.

**Cenário 4: Remoção de itens do carrinho**

**Caso de Teste 4.1: Remoção de um item específico**

* **Descrição:** O usuário remove um item do carrinho clicando no botão "Remover" ao lado do produto.

* **Pré-condições:**  O carrinho possui ao menos dois itens.

* **Resultado Esperado:**  O item é removido, e o subtotal do carrinho é atualizado.

**Caso de Teste 4.2:  Remoção de todos os itens do carrinho**

* **Descrição:** O usuário clica em "Remove" na Lista de Produtos da página inicial.

* **Pré-condições:**  O produto está adicionado no carrinho..

* **Resultado Esperado:** O item é removido do carrinho.

 **Cenário 5: Navegação entre Páginas**

**Caso de Teste 5.1: Navegar no menu lateral** 

* **Descrição:** O usuário clica no link da página "About" no menu lateral  
    
* **Pré-condições:**  Estar na página inicial ou na página de detalhes do produto.

* **Resultado Esperado:** A próxima página “About” é exibida, com informações sobre a empresa.

  **Caso de Teste 5.2: Retornar da Página de um Produto à Página Inicial**

* **Descrição:** O usuário clica no botão "Back to products" para voltar à página anterior da listagem.

* **Pré-condições:**  O usuário está em uma página de detalhes de um produto.

* **Resultado Esperado:** Os produtos da página inicial são exibidos corretamente.

  **Caso de Teste 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

* **Descrição:** O usuário clica no botão "Continue Shopping" para voltar à página anterior da listagem.

* **Pré-condições:**  O usuário está na página do Carrinho de Compras.

* **Resultado Esperado:** Os produtos da página inicial são exibidos corretamente e usuário pode continuar comprando.

**Caso de Teste 5.4: Retornar à primeira página do Carrinho de Compras**

* **Descrição:** O usuário clica no botão "Cancel" para voltar à página do Carrinho de compras.  
    
* **Pré-condições:**  O usuário está na página do primeiro passo do Checkout.

* **Resultado Esperado:** A página do Carrinho de Compras é exibida. 

**Cenário 6\. Logout**

**Caso de Teste 6.1: Logout pelo menu de usuário**

* **Descrição:** O usuário clica no botão "Logout" no menu lateral para encerrar a sessão.

* **Pré-condições:**  Usuário está logado.

* **Resultado Esperado:** O sistema encerra a sessão e redireciona o usuário para a página de login.

**Caso de Teste 6.2: Acesso a página protegida após logout**

* **Descrição:** O usuário tenta acessar uma página protegida após realizar o logout.

* **Pré-condições:**  Usuário não está logado.

* **Resultado Esperado:** O sistema não deve permitir o acesso e deve exibir a mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in".

###4. **Cronograma de Testes:**

* **Semana 1:** Preparação do ambiente de testes, criação dos casos de teste e revisão da documentação.  
* **Semana 2:** Execução dos testes manuais e automatizados, análise dos resultados e correção de defeitos encontrados.

###5. **Equipe de Testes:**

* Testador  
* Analista de Qualidade  
* Tech Lead 

###6. **Critérios de Aceitação:**

* Todos os casos de teste devem ser executados sem erros.  
* As funcionalidades de login, ordenação de produtos, fluxo de compra, remoção de produtos, navegação entre páginas e logout devem atender aos requisitos especificados.

###7. **Considerações Finais:**

Ao final dos testes, será gerado um relatório detalhado com os resultados, relatório de bugs e recomendações de melhoria para a equipe de Desenvolvimento.

**Resultados dos testes executados** 

**Funcionalidade: Login**

Como um usuário    
Quero fazer login no sistema  **Swag Labs**  
Para acessar minhas informações e funcionalidades personalizadas

**Caso de Teste 1.1: Login com dados válidos**

Dado que estou na página de login    
Quando eu insiro um usename válido "standard\_user"    
E eu insiro um password válido "secret\_sauce"    
E clico no botão “Login"  
Então devo ser redirecionado para a página inicial  

**Resultado da Execução:** 

O usuário foi redirecionado corretamente para a página inicial.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Login

![][image1]

**Caso de Teste 1.2: Login com dados inválidos**

Dado que estou na página de login    
Quando eu insiro um usename válido "standard\_user"  
E eu insiro uma senha inválida "secret\_sauce1"    
E clico no botão "Login"    
Então devo ver a mensagem de erro "Epic sadface: Username and password do not match any user in this service"    
E devo permanecer na página de login  

**Resultado da Execução:**

O sistema exibiu a mensagem correta de erro.  
O usuário permaneceu na página de login.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Login

![][image2]

**Funcionalidade: Ordenação e filtragem de produtos**

Como um usuário    
Quero ordenar os produtos conforme opções disponíveis

**Caso de Teste 2.1: Ordenação de produtos por preço crescente**
 
Dado que estou na página Products   
Quando eu seleciono a opção "Price: low to high" no menu de ordenação  
Então os produtos devem ser exibidos em ordem crescente de preço  
E o primeiro produto deve ser o de menor preço disponível

**Resultado da Execução:**

Os produtos de menor valor aparecem no topo da lista.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Products

![][image3]

**Caso de Teste 2.2: Ordenação de produtos por preço decrescente**  
	  	  
Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Price: high to low" no menu de ordenação  
Então os produtos devem ser exibidos em ordem decrescente de preço  
E o primeiro produto deve ser o de maior preço disponível

**Resultado da Execução:**

Os produtos de maior valor aparecem no topo da lista.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Products

![][image4]

**Caso de Teste 2.3: Ordenação de produtos por ordem alfabética**

Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Name: A to Z" no menu de ordenação  
Então os produtos devem ser exibidos em ordem alfabética  
E o primeiro produto deve ser exibido na ordem de A a Z.

**Resultado da Execução:**

Os produtos são exibidos por ordem alfabética de A a Z.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Product

![][image5]

**Caso de Teste 2.4: Filtragem de produtos**

Dado que estou na página de listagem de produtos  
Quando eu seleciono a opção "Filtrar"  
Então as características do produto são exibidas

**Resultado da Execução:**

Funcionalidade não disponível.

**Status:** Bloqueado.

**Observações:** Existe apenas a opção de ordenar produtos, mas não aparecem opções de filtragem com as características ou variações de cor, tamanho, material.

**Evidência:**

Tela Products

**![][image6]**

**Funcionalidade:  Fluxo completo de compra (do carrinho até finalização)**

Como um usuário    
Quero adicionar produtos ao carrinho  
Para realizar uma compra com cartão de crédito  
    
    
**Caso de Teste 3.1: Adicionar produto no carrinho através da Página Inicial**

Dado que estou na página Products de listagem de produtos    
Quando eu visualizo os produtos disponíveis  
E clico no botão “Add to cart" do produto desejado  
Então o produto deve ser adicionado ao carrinho  

**Resultado da Execução:**

O produto foi adicionado ao carrinho. 

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Products

![][image7]

**Caso de Teste 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**

	Dado que estou na página de Detalhes do Produto   
Quando eu clico no botão “Add to cart"  
Então o produto deve ser adicionado ao carrinho

**Resultado da Execução:**

O produto foi adicionado ao carrinho. 

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela de Detalhes do produto

**![][image8]**

**Caso de Teste 3.3: Finalização de compra com cartão de crédito válido**

 Dado que adicionei um produto ao carrinho    
 E cliquei no botão "Checkout"    
 E preenchi os dados pessoais e de entrega válidos  
 E clico em “Continue”    
 Quando eu insiro os dados de um cartão de crédito válido    
 E clico no botão "Finish"    
 Então o sistema deve exibir a mensagem de agradecimento:   
*"Thank you for your   order\!"*

**Resultado da Execução:**

O pedido foi finalizado com sucesso e a mensagem de agradecimento exibida.

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidências:**

Tela Checkout Passo 1

**![][image9]**

Tela Checkout Passo 2

**![][image10]**

Tela Checkout Passo 3

**![][image11]**  
**Funcionalidade: Remoção de itens do carrinho**

Como um usuário    
Quero remover produtos do carrinho    
Para ajustar minha seleção de itens antes de finalizar a compra  

**Caso de Teste 4.1: Remoção de um item específico**

 Dado que tenho um produto no carrinho  
 Quando eu clico no botão "Remover" ao lado do produto  
 Então o produto deve ser removido do carrinho  
 E o carrinho deve exibir a mensagem "Seu carrinho está vazio"

**Resultado da Execução:**

O produto foi removido corretamente do carrinho.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Carrinho de Compras com 2 Itens

**![][image12]**

Tela Carrinho de Compras Após a Remoção de 1 Item Específico

**![][image13]**

**Caso de Teste 4.2:  Remoção de todos os itens do carrinho**

Dado que tenho um produto no carrinho  
Quando eu clico no botão "Remover"   
Então o carrinho deve aparecer vazio 

**Resultado da Execução:**

Todos os produtos foram removidos corretamente.   

**Status:** Aprovado.

**Observações:** Não é exibida nenhuma mensagem avisando que o carrinho está vazio.

**Evidência:**

Tela do Carrinho de Compras com item incluso

**![][image14]**

Tela do carrinho de Compras Vazio

**![][image15]**

**Funcionalidade: Navegação entre Páginas**

Como um usuário    
Quero poder navegar entre as páginas da loja   
Para explorar melhor os produtos antes de finalizar a compra

**Caso de Teste 5.1: Navegar no menu lateral e Visitar a Página “About”**

Dado que estou na Página inicial  
E quero visitar a página “About” para conhecer a empresa  
Quando eu clico no link  
Então a página redireciona para a página “About”

**Resultado da Execução:** 

O sistema não redireciona para a página “About”**.**

**Status:** Reprovado.

**Observações:** A página redireciona para uma página institucional da empresa e o login é encerrado.

**Evidências:**

Tela Menu Lateral Aberto

**![][image16]**

Página institucional da Empresa

![][image17]

**Caso de Teste 5.2: Retornar da Página de um Produto à Página Inicial**

    Dado que estou na página de detalhes de um produto    
    Quando eu clico no botão "Back to Products"    
    Então devo ser redirecionado para a página inicial    
    E a página inicial deve carregar corretamente com todos os produtos listados  

**Resultado da Execução:** 

  A navegação pelo botão "Back to products" funcionou corretamente.    
  A página inicial carregou com a lista de produtos exibida corretamente.    
  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidências:**

Tela de Detalhes do Produto

![][image18]

Tela Página Inicial

**![][image19]**

**Caso de Teste 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

    Dado que estou na página do Carrinho de Compras    
    Quando eu clico no botão "Continue Shopping"    
    Então devo ser redirecionado para a página inicial    
    E a página inicial deve carregar corretamente com todos os produtos listados  

**Resultado da Execução:**

  A navegação pelo botão "Continue Shopping" funcionou corretamente.    
  A página inicial carregou com a lista de produtos exibida corretamente.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidências:**

Tela Carrinho de Compras

![][image20]

Tela Página Inicial

**![][image19]**

**Caso de Teste 5.4: Retornar do Checkout à primeira página do Carrinho de Compras**

Dado que estou na página da primeira fase do Checkout    
Quando eu clico no botão "Cancel"    
Então devo ser redirecionado para a página do Carrinho de Compras    
E a página inicial deve carregar corretamente os produtos que estão no carrinho de compras

**Resultado da Execução:**

A navegação pelo botão "Cancel” funcionou corretamente.    
A página do Carrinho de Compras carregou os produtos corretamente.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidências:**

Tela Primeiro Passo do Checkout

**![][image21]**

Tela Carrinho de Compras

![][image22]

**Funcionalidade: Logout**

Como um usuário autenticado  
Quero sair da minha conta   
Para proteger minhas informações pessoais

**Caso de Teste 6.1: Logout pelo menu principal**

 Dado que estou logado no sistema    
 Quando eu clico no botão  "Logout"    
 Então devo ser redirecionado para a página de login    
 E minha sessão deve ser encerrada    
    

**Resultado da Execução:**

 O botão "Logout" redirecionou corretamente para a página de login.    
 A sessão foi encerrada.    
  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Menu Lateral 

**![][image23]**  
Tela Login

**![][image24]**

**Caso de Teste 6.2: Acesso a página protegida após logout**

Dado que realizei logout    
Quando eu tento acessar diretamente a URL [https://www.saucedemo.com/inventory.html](https://www.saucedemo.com/inventory.html) de uma página protegida    
Então devo ser redirecionado para a página de login    
E a mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in." deve ser exibida

**Resultado da Execução:**

O sistema redirecionou corretamente para a página de login ao tentar acessar a URL protegida.  

A mensagem "Epic sadface: You can only access '/inventory.html' when you are logged in." foi exibida.  

**Status:** Aprovado.

**Observações:** Nenhum problema identificado.

**Evidência:**

Tela Login 

**![][image25]**

    

**Sugestões de melhorias de UX/UI**

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

**Lista de bugs encontrados**

**CT 5.1: Navegar no menu lateral e Visitar a Página “About”**

**Resultado da Execução:** O sistema não redireciona para a página “About”**.**

**Status:** Reprovado.

**Evidências:**  
Tela Menu Lateral Aberto

**![][image35]**

Página institucional da Empresa

![][image36]

Vídeo:[https://www.loom.com/share/671fc7b50ba347dfa4bb08da385d677f?sid=cd6f0add-2512-45d6-a465-b4f2953e5763](https://www.loom.com/share/671fc7b50ba347dfa4bb08da385d677f?sid=cd6f0add-2512-45d6-a465-b4f2953e5763)

**Análise de Riscos** 

A aplicação não apresentou bugs de segurança, desempenho ou que possam causar impactos. Mas os riscos podem surgir devido a fatores externos, limitações técnicas ou mudanças no ambiente. 

Foi criada uma [Matriz de Rastreabilidade](https://docs.google.com/spreadsheets/d/169p11Ng1BhybtgCTZazmprV3Bo9662xw5bhbdhWaNYA/edit?gid=0#gid=0) para classificar os Casos de Testes e mapear os tipos de teste, prioridade, etc.e abaixo temos o resumo: 

**CT 1.1: Login com dados válidos**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Login

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 1.2: Login com dados inválidos**

Tipo de Teste: Funcional Negativo

Funcionalidade Associada: Login

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P2

Versão: V1.0

**CT 2.1: Ordenação de produtos por preço crescente**

Tipo de Teste: Usabilidade

Funcionalidade Associada: Ordenação e filtragem de produtos

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P3

Versão: V1.0

**CT 2.2: Ordenação de produtos por preço decrescente**

Tipo de Teste: Usabilidade

Funcionalidade Associada: Ordenação e filtragem de produtos

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P3

Versão: V1.0

**CT 2.3: Ordenação de produtos por ordem alfabética**

Tipo de Teste: Usabilidade

Funcionalidade Associada: Ordenação e filtragem de produtos

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P3

Versão: V1.0

**CT 2.4: Filtragem de produtos**

Tipo de Teste: Usabilidade

Funcionalidade Associada: Ordenação e filtragem de produtos

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P3

Versão: V1.0

**CT 3.1: Adicionar produto no carrinho através da Página Inicial**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Fluxo de compra

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 3.2: Adicionar produto no carrinho através da Página de Detalhes do Produto**

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

**CT 4.1: Remoção de um item específico**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Remoção de Produtos do carrinho

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 4.2: Remoção de todos os itens do carrinho**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Remoção de Produtos do carrinho

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 5.1: Navegar no menu lateral**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Navegação

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P2

Versão: V1.0

**CT 5.2: Retornar da Página de um Produto à Página Inicial**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Navegação

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P2

Versão: V1.0

**CT 5.3: Retornar da Página do Carrinho de Compras à Página Inicial**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Navegação 

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 5.4: Retornar à primeira página do Carrinho de Compras**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Navegação 

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 6.1: Logout pelo menu principal**

Tipo de Teste: Funcional Positivo

Funcionalidade Associada: Logout

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0

**CT 6.2: Acesso a página protegida após logout**

Tipo de Teste: Funcional Negativo

Funcionalidade Associada: Logout

Passível de Automação: Sim

Regressivo Obrigatório: Sim

Prioridade: P1

Versão: V1.0
