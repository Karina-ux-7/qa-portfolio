## CT-001 — Login com dados válidos

**Objetivo:**  
Validar o acesso ao sistema com credenciais válidas.

**Pré-condição:**  
Usuário cadastrado no sistema.

**Passos:**
1. Acessar a tela de login
2. Informar o usuário `standard_user`
3. Informar a senha `secret_sauce`
4. Clicar em Login

**Resultado esperado:**  
O usuário deve acessar o sistema com sucesso e ser direcionado para a tela de produtos.

**Resultado obtido:**  
Login realizado com sucesso e usuário direcionado para a tela de produtos.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-001](evidencias/CT-001-login-valido.png)

## CT-002 — Login com usuário inválido

**Objetivo:**  
Validar que o sistema não permita o acesso com um usuário não cadastrado.

**Pré-condição:**  
Estar na tela de login.

**Passos:**
1. Acessar a tela de login
2. Informar o usuário `karina_teste`
3. Informar a senha `secret_sauce`
4. Clicar em Login

**Resultado esperado:**  
O sistema deve impedir o acesso e informar que as credenciais são inválidas.

**Resultado obtido:**  
O acesso foi impedido e o sistema exibiu uma mensagem informando que o usuário e a senha não correspondem a nenhum usuário cadastrado.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-002](evidencias/CT-002-usuario-invalido.png)

## CT-003 — Login com senha inválida

**Objetivo:**  
Validar que o sistema não permita o acesso quando a senha informada estiver incorreta.

**Pré-condição:**  
Estar na tela de login.

**Passos:**
1. Acessar a tela de login
2. Informar o usuário `standard_user`
3. Informar uma senha inválida
4. Clicar em Login

**Resultado esperado:**  
O sistema deve impedir o acesso e informar que as credenciais são inválidas.

**Resultado obtido:**  
O acesso foi impedido e o sistema exibiu uma mensagem informando que o usuário e a senha não correspondem a nenhum usuário cadastrado.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-003](evidencias/CT-003-senha-invalida.png)

## CT-004 — Login com campos vazios

**Objetivo:**  
Validar que o sistema não permita o login quando os campos obrigatórios estiverem vazios.

**Pré-condição:**  
Estar na tela de login.

**Passos:**
1. Acessar a tela de login
2. Deixar o campo de usuário vazio
3. Deixar o campo de senha vazio
4. Clicar em Login

**Resultado esperado:**  
O sistema deve impedir o acesso e informar que o campo de usuário é obrigatório.

**Resultado obtido:**  
O acesso foi impedido e o sistema exibiu uma mensagem informando que o nome de usuário é obrigatório.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-004](evidencias/CT-004-campos-vazios.png)

## CT-005 — Login com usuário bloqueado

**Objetivo:**  
Validar que um usuário bloqueado não consiga acessar o sistema.

**Pré-condição:**  
Estar na tela de login.

**Passos:**
1. Acessar a tela de login
2. Informar o usuário `locked_out_user`
3. Informar a senha `secret_sauce`
4. Clicar em Login

**Resultado esperado:**  
O sistema deve impedir o acesso e informar que o usuário está bloqueado.

**Resultado obtido:**  
O acesso foi impedido e o sistema exibiu a mensagem informando que o usuário está bloqueado.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-005](evidencias/CT-005-usuario-bloqueado.png)

## CT-006 — Adicionar produto ao carrinho

**Objetivo:**  
Validar que um produto possa ser adicionado corretamente ao carrinho.

**Pré-condição:**  
Usuário autenticado no sistema com `standard_user`.

**Passos:**
1. Acessar a tela de produtos
2. Escolher um produto
3. Clicar em Add to cart
4. Verificar a alteração do botão do produto
5. Verificar o contador do carrinho

**Resultado esperado:**  
O produto deve ser adicionado ao carrinho, o botão deve mudar para Remove e o contador do carrinho deve exibir a quantidade `1`.

**Resultado obtido:**  
O produto foi adicionado ao carrinho com sucesso, o botão foi alterado para Remove e o contador do carrinho passou a exibir `1`.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-006](evidencias/CT-006adicionar-produto-carrinho1.png)

## CT-007 — Remover produto do carrinho

**Objetivo:**  
Validar que um produto adicionado ao carrinho possa ser removido corretamente.

**Pré-condição:**  
Usuário autenticado no sistema e com um produto adicionado ao carrinho.

**Passos:**
1. Acessar o carrinho
2. Verificar o produto adicionado
3. Clicar em Remove
4. Verificar o conteúdo do carrinho
5. Verificar o contador do carrinho

**Resultado esperado:**  
O produto deve ser removido do carrinho e o contador deve ser atualizado, deixando de exibir a quantidade `1`.

**Resultado obtido:**  
O produto foi removido do carrinho com sucesso. O carrinho ficou vazio e o contador deixou de exibir a quantidade `1`.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-007](evidencias/CT-007-remover-produto-carrinho.png)

## CT-008 — Validar contador do carrinho com dois produtos

**Objetivo:**  
Validar que o contador do carrinho seja atualizado corretamente ao adicionar mais de um produto.

**Pré-condição:**  
Usuário autenticado no sistema.

**Passos:**
1. Acessar a tela de produtos
2. Adicionar um produto ao carrinho
3. Adicionar um segundo produto ao carrinho
4. Verificar o contador do carrinho
5. Acessar o carrinho
6. Verificar os produtos adicionados

**Resultado esperado:**  
O contador do carrinho deve exibir a quantidade `2` e os dois produtos adicionados devem estar visíveis no carrinho.

**Resultado obtido:**  
O contador do carrinho foi atualizado para `2` e os dois produtos adicionados foram exibidos corretamente no carrinho.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-008](evidencias/CT-008-contador-dois-produtos.png)

## CT-009 — Iniciar checkout com dados válidos

**Objetivo:**  
Validar que o usuário consiga avançar no checkout ao informar dados válidos.

**Pré-condição:**  
Usuário autenticado e com produtos adicionados ao carrinho.

**Passos:**
1. Acessar o carrinho
2. Clicar em Checkout
3. Informar nome válido
4. Informar sobrenome válido
5. Informar CEP válido
6. Clicar em Continue

**Resultado esperado:**  
O sistema deve aceitar os dados informados e direcionar o usuário para a tela de resumo da compra.

**Resultado obtido:**  
Os dados foram aceitos e o sistema direcionou o usuário corretamente para a tela de resumo da compra, exibindo os produtos adicionados, informações de pagamento, envio e total da compra.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-009](evidencias/CT-009-checkout-dados-validos.png)

## CT-010 — Concluir compra com sucesso

**Objetivo:**  
Validar que o usuário consiga finalizar a compra após revisar corretamente os dados do checkout.

**Pré-condição:**  
Usuário autenticado, com produtos no carrinho e checkout preenchido com dados válidos.

**Passos:**
1. Acessar a tela de resumo do checkout
2. Conferir os produtos adicionados
3. Conferir as informações de pagamento e envio
4. Conferir o valor total da compra
5. Clicar em Finish

**Resultado esperado:**  
O sistema deve concluir a compra e exibir uma mensagem de confirmação de pedido realizado com sucesso.

**Resultado obtido:**  
A compra foi concluída com sucesso e o sistema exibiu a mensagem de confirmação do pedido.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-010](evidencias/CT-010-concluir-compra-sucesso.png)

## CT-011 — Checkout com nome vazio

**Objetivo:**  
Validar que o sistema não permita avançar no checkout sem o preenchimento do nome.

**Pré-condição:**  
Usuário autenticado e com produtos adicionados ao carrinho.

**Passos:**
1. Acessar o checkout
2. Deixar o campo First Name vazio
3. Informar um sobrenome válido
4. Informar um CEP válido
5. Clicar em Continue

**Resultado esperado:**  
O sistema deve impedir o avanço e informar que o campo de nome é obrigatório.

**Resultado obtido:**  
O sistema impediu o avanço no checkout e exibiu a mensagem `Error: First Name is required`.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-011](evidencias/CT-011-checkout-nome-vazio.png)

## CT-012 — Checkout com CEP vazio

**Objetivo:**  
Validar que o sistema não permita avançar no checkout sem o preenchimento do CEP.

**Pré-condição:**  
Usuário autenticado e com produtos adicionados ao carrinho.

**Passos:**
1. Acessar o checkout
2. Informar um nome válido
3. Informar um sobrenome válido
4. Deixar o campo Postal Code vazio
5. Clicar em Continue

**Resultado esperado:**  
O sistema deve impedir o avanço e informar que o campo de CEP é obrigatório.

**Resultado obtido:**  
O sistema impediu o avanço no checkout e exibiu a mensagem `Error: Postal Code is required`.

**Status:**  
Aprovado

**Evidência:**  
[Ver evidência CT-012](evidencias/CT-012-checkout-cep-vazio.png)
