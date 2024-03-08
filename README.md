# Projeto de Sistema Bancário com Duplo Fator de Autenticação em Python

Este é um projeto de sistema bancário desenvolvido em Python, que inclui um algoritmo de duplo fator de autenticação para garantir a segurança das transações financeiras dos clientes. O código completo pode ser encontrado [aqui](https://github.com/Daniel010203/Projeto-de-Sistema-Bancario-com-duplo-fator-de-autenticacao-em-python/tree/a40611d6509335f06ef77923ee5a6f07f0203d54).

## Funcionalidades

- **Duplo Fator de Autenticação**: O código implementa um sistema de duplo fator de autenticação, que exige que os clientes forneçam não apenas uma senha, mas também um código enviado para seu e-mail e telefone celular. Isso aumenta significativamente a segurança das transações e protege contra acessos não autorizados.

- **Gerenciamento de Contas e Transações**: O sistema permite que os clientes criem contas bancárias, realizem saques, depósitos e consultem seus saldos. Todas as transações são registradas e podem ser visualizadas posteriormente para fins de auditoria e controle.

## Como Utilizar

Para utilizar o sistema, siga estas etapas:

1. **Instalação das Dependências**: Certifique-se de ter Python instalado em sua máquina. Além disso, você pode precisar instalar a biblioteca `pyautogui` se ainda não a tiver. Você pode instalá-la usando o seguinte comando:
   ```
   pip install pyautogui
   ```

2. **Execução do Código**: Clone este repositório em sua máquina e execute o arquivo Python principal `sistema_bancario.py`. Isso iniciará o sistema bancário, permitindo que você crie contas, realize transações e experimente o processo de autenticação de duplo fator.

3. **Teste do Duplo Fator de Autenticação**: Certifique-se de testar o processo de autenticação de duplo fator, fornecendo seu CPF, e-mail e número de telefone celular associados à sua conta.

## Contribuições

Contribuições são bem-vindas! Se você encontrar algum problema ou tiver alguma melhoria para sugerir, por favor, abra uma issue ou envie um pull request para que possamos discutir e revisar.

## Benefícios para as Organizações

Este projeto pode beneficiar as organizações de diversas maneiras:

- **Segurança Aprimorada**: Com a implementação do duplo fator de autenticação, as organizações podem garantir que as transações financeiras dos clientes sejam seguras e protegidas contra acessos não autorizados.

- **Confiança do Cliente**: Oferecer um sistema bancário seguro e confiável aumenta a confiança dos clientes na organização, o que pode levar a uma melhor fidelização e satisfação do cliente.

- **Conformidade Regulatória**: Com a crescente regulamentação em torno da segurança cibernética e proteção de dados, a implementação de medidas de segurança como o duplo fator de autenticação ajuda as organizações a cumprir os requisitos regulatórios e evitar multas por não conformidade.

- **Redução de Riscos Financeiros**: Ao proteger as transações financeiras dos clientes contra fraudes e ataques cibernéticos, as organizações podem reduzir os riscos financeiros associados a perdas de dados ou violações de segurança.

Este projeto de sistema bancário com duplo fator de autenticação em Python oferece uma solução robusta e segura para organizações que desejam garantir a segurança e confiabilidade de suas operações financeiras nos dias atuais.

Este código implementa um sistema bancário básico em Python, com funcionalidades como criação de contas, realização de transações (saques e depósitos), registro de histórico de transações e autenticação de duplo fator para clientes.


Aqui está uma explicação das principais funcionalidades do código:

1. **Cliente**:
   - A classe `Cliente` representa um cliente do banco. Ela possui métodos para adicionar contas, realizar transações e autenticar com duplo fator.
   - O método `adicionar_duplo_fator` permite que um cliente adicione informações de duplo fator, como e-mail e número de telefone, vinculados ao seu CPF.
   - O método `autenticar_duplo_fator` verifica se as informações de duplo fator fornecidas pelo cliente correspondem às informações registradas para aquele CPF.

2. **PessoaFisica**:
   - A classe `PessoaFisica` herda da classe `Cliente` e representa um cliente pessoa física do banco. Ela inclui atributos como nome, data de nascimento e CPF.

3. **Conta**:
   - A classe `Conta` representa uma conta bancária. Ela possui métodos para sacar e depositar dinheiro, bem como propriedades para acessar o saldo, número da conta, agência, cliente associado e histórico de transações.

4. **ContaCorrente**:
   - A classe `ContaCorrente` herda da classe `Conta` e representa uma conta corrente. Ela inclui recursos específicos de uma conta corrente, como limite de saque e número máximo de saques permitidos.

5. **Historico**:
   - A classe `Historico` é responsável por armazenar o histórico de transações de uma conta.

6. **Transacao**:
   - A classe abstrata `Transacao` define uma transação genérica. Ela possui métodos abstratos para registrar uma transação em uma conta.

7. **Saque** e **Deposito**:
   - As classes `Saque` e `Deposito` implementam transações específicas de saque e depósito. Elas registram suas transações no histórico de uma conta após serem realizadas com sucesso.

8. **autenticar_com_duplo_fator**:
   - Esta função verifica a autenticação de duplo fator para um cliente específico, comparando as informações fornecidas (CPF, e-mail e telefone) com as informações registradas.

No exemplo de uso fornecido no final do código, um cliente é criado e adicionado ao sistema bancário, informações de duplo fator são registradas para esse cliente e a função `autenticar_com_duplo_fator` é chamada para autenticar o cliente com base nas informações fornecidas.

Além disso, a função `autenticar_com_duplo_fator` emite uma mensagem no sistema operacional usando a biblioteca `pyautogui` para confirmar que o acesso foi autorizado após a autenticação de duplo fator ser bem-sucedida.
