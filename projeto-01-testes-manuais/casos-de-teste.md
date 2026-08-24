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
