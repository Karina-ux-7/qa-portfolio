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
[Ver evidência CT-002](evidencias/CT-002-usuário-inválido.png)

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
[Ver evidência CT-003](evidencias/CT-003-senha-inválida.png)

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
[Ver evidência CT-006](evidencias/CT-006-adicionar-produto-carrinho1.png)
