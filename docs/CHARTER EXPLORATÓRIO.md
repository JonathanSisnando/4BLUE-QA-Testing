# Cobertura de Testes - Charter Exploratório

---

### Criar Conta - Nome Completo

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Válido:** Tentar criar conta inserindo um nome com caracteres alfabéticos e espaços entre prenomes. | Pass | Não | - |
| **Inválido:** Tentar criar conta inserindo o campo Nome Completo Vazio e os demais preenchidos. | Fail | Sim | 0000002 [BUG - Criar Conta] Criação de conta permitida sem preenchimento do "Nome Completo" |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000003 {Melhoria} - [Cadastrar Conta] - Indicação visual de campos obrigatórios no formulário de cadastro |
| **Inválido:** Tentar criar conta inserindo um nome contendo caracteres alfanuméricos. | Fail | Sim | 0000004 [BUG - Criar Conta] Campo "Nome Completo" permite a inserção de caracteres numéricos |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000005 {MELHORIA} - [Cadastrar Conta] - Refinamento da validação de caracteres e restrição de símbolos no campo "Nome Completo" |
| **Inválido:** Tentar criar conta inserindo um nome contendo apenas caracteres especiais. | Fail | Sim | 0000006 [BUG - Criar Conta] Campo "Nome Completo" aceita caracteres especiais e permite o cadastro |
| **Partição (Limite Inferior):** Tentar criar conta contendo apenas 1 caractere no nome. | Pass | Sim | 0000007 {MELHORIA} - [Criar Conta] - Implementar limite mínimo de caracteres no campo "Nome Completo" |
| **Partição (Limite Superior):** Tentar criar conta contendo mais de 100 caracteres no nome. | Fail | Sim | 0000008 [BUG - Criar Conta] Quebra de layout nos campos "Telefone" e "Confirmar Senha" |

---

### Criar Conta - Telefone

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Válido:** Tentar criar conta inserindo um Nº de Telefone contendo exatamente 11 números (padrão celular). | Pass | Não | - |
| **Válido:** Tentar criar conta inserindo um Nº de Telefone contendo exatamente 10 números (padrão fixo). | Pass | Sim | 0000010 {MELHORIA} - [Criar Conta] - Implementação de máscara dinâmica para telefones fixos e celulares |
| **Inválido:** Tentar criar conta com o campo TELEFONE Vazio. | Fail | Sim | 0000011 [BUG - Criar Conta] Criação de conta permitida com o campo "TELEFONE" vazio |
| **Inválido:** Tentar criar conta inserindo um Nº de Telefone contendo apenas 8 números. | Fail | Sim | 0000012 [BUG - Criar Conta] Sistema permite cadastro com número de telefone incompleto (8 dígitos) |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000013 {MELHORIA} - [Criar Conta] - Feedback visual e instrução para telefone insuficiente |
| **Inválido:** Tentar criar conta inserindo um Nº de Telefone contendo letras ou caracteres especiais. | Fail | Sim | 0000014 [BUG - Criar Conta] Campo "TELEFONE" aceita caracteres especiais e permite o cadastro |
| **Partição:** Tentar criar conta inserindo um Nº de Telefone com 12 ou mais números. | Fail | Sim | 0000015 [BUG - Criar Conta] Campo "TELEFONE" permite inserção ilimitada de caracteres e cadastro de dados inválidos |
| **Interface (Máscara):** Tentar preencher o campo e verificar se a máscara (00) 00000-0000 é aplicada automaticamente durante a digitação. | Fail | Sim | 0000009 {MELHORIA} - [Criar Conta] - Aplicação automática de máscara de formatação no campo "Telefone" |
| **Borda (Negativo):** Tentar criar conta inserindo um número composto apenas por zeros (00000000000). | Fail | Sim | 0000016 [BUG - Criar Conta] Campo "TELEFONE" aceita sequências numéricas inválidas (apenas zeros) |

---

### Criar Conta - Email

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Válido:** Tentar criar conta inserindo um e-mail no formato padrão (usuario@dominio.com). | Pass | Não | - |
| **Inválido:** Tentar criar conta com o campo EMAIL Vazio. | Fail | Sim | 0000017 [BUG - Criar Conta] Criação de conta permitida com o campo "E-MAIL" vazio |
| **Inválido:** Tentar criar conta com o campo EMAIL Vazio (Validação secundária). | Fail | Sim | 0000018 [BUG - Criar Conta] Criação de conta permitida com o campo "E-MAIL" vazio |
| **Inválido:** Tentar criar conta inserindo um e-mail sem o caractere "@". | Fail | Sim | 0000019 [BUG - Criar Conta] Sistema permite cadastro com e-mail sem extensão de domínio |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000020 {MELHORIA} - [Criar Conta] - Feedback visual e instrução para e-mail inválido |
| **Inválido:** Tentar criar conta inserindo um e-mail com dois caracteres "@". | Fail | Sim | 0000021 [BUG - Criar Conta] Sistema permite cadastro com e-mail contendo "@" duplicado ("@@") |
| **Partição:** Tentar criar conta inserindo um e-mail com domínio extremamente longo para verificar a integridade do layout. | Pass | Não | - |
| **Integridade (Trim):** Tentar criar conta inserindo espaços em branco antes ou depois do e-mail e verificar se o sistema ignora esses espaços. | Fail | Sim | 0000022 [BUG - Criar Conta] Sistema permite cadastro com e-mail contendo espaços em branco |

---

### Criar Conta - Senha e Confirmar Senha

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Válido:** Tentar criar conta inserindo uma senha com 8 caracteres sendo um deles especial. | Pass | Não | - |
| **Válido:** Tentar criar conta inserindo uma senha com mais de 8 caracteres e múltiplos caracteres especiais. | Pass | Não | - |
| **Inválido:** Tentar criar conta com o campo SENHA ou CONFIRMAR SENHA Vazio. | Fail | Sim | 0000023 [BUG - Criar Conta] Sistema permite cadastro com os campos "Senha" e "Confirmar Senha" vazios |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000024 {MELHORIA} - [Criar Conta] - Desabilitar botão "Criar conta" para formulários incompletos |
| **Inválido:** Tentar criar conta inserindo uma senha com 8 caracteres mas sem nenhum caractere especial. | Fail | Sim | 0000025 [BUG - Criar Conta] Sistema permite cadastro de senha sem caractere especial |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000026 {MELHORIA} - [Criar Conta] - Validação rigorosa de critérios de segurança na senha |
| **Inválido:** Tentar criar conta inserindo uma senha com menos de 8 caracteres mesmo contendo especial. | Fail | Sim | 0000027 [BUG - Criar Conta] Sistema permite cadastro com senha de 8 caracteres (Abaixo do limite de 9) |
| **Inválido:** Tentar criar conta inserindo uma senha válida, mas com o campo CONFIRMAR SENHA divergente. | Fail | Sim | 0000028 [BUG - Criar Conta] Sistema permite cadastro com senhas divergentes (Senha vs. Confirmação) |
| Sugestão baseada no cenário acima. | Pass | Sim | 0000029 {MELHORIA} - [Criar Conta] - Validação em tempo real para senhas divergentes |
| **Partição (Limite Inferior):** Tentar criar conta inserindo uma senha com 7 caracteres e 1 especial. | Fail | Sim | 0000030 [BUG - Criar Conta] Sistema permite cadastro com senha contendo apenas 8 caracteres |
| **Segurança (Privacidade):** Tentar copiar o conteúdo do campo Senha e verificar se a função de cópia está bloqueada. | Pass | Não | - |

---

### Criar Conta - Navegação e Interface

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Navegação (Teclado):** Verificar se a tecla "TAB" percorre todos os campos e o botão na ordem lógica da tela. | Pass | Não | - |
| **Redirecionamento:** Clicar em "Voltar para login" e verificar se o usuário é enviado para a tela de autenticação. | Pass | Sim | 0000024 {MELHORIA} - [Criar Conta] - Desabilitar botão "Criar conta" para formulários incompletos *(Nota: ID associado conforme documento original)* |

---

### Login - Fluxo Base e Email

| Cenário de Teste | Resultado | Falhas | ID e Comentários |
| :--- | :--- | :--- | :--- |
| **Caminho Feliz:** Tentar realizar login inserindo um e-mail já cadastrado e a senha correta correspondente. | Fail | Sim | 0000031 [BUG - Login] Sistema exibe toast de "Erro Inesperado" após login bem-sucedido |
| **Válido (Email):** Tentar inserir um e-mail no formato padrão (usuario@dominio.com). | Pass | Não | - |
| **Inválido:** Tentar realizar login com o campo EMAIL Vazio e a senha preenchida | Pass | Não | - |
