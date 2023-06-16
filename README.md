# Challenge Django Consultant
## _Teste Técnico para Consultor Django DigitalSys_

### Introdução

Esse teste técnico visa avaliar a sua proficiência em Django com um problema real, vocẽ terá passo-a-passo de como proceder para realizar e enviar o teste técnico

### Entrega

A entrega desse desafio deverá ser feita através do e-mail code-challenge@digitalsys.com.br com as seguintes características:

- **Título do E-mail:** Code-Challenge: Django Consultant- 
- **Conteúdo do E-mail:** Seu nome completo, link do github e link do seu linkedin

### _Definition of Done_ para seu projeto

- Tenha em mente que a pessoa que for avaliar seu projeto não lerá seu código antes de vê-lo funcionar, por isso, inclua no README do projeto as instruções para rodar seu projeto com sucesso.
- Dê preferência a uma solução dockerizada, um docker-compose com todas as dependências do projeto costumam funcionar melhor do que depender que o ambiente da outra pessoa possua as dependências
- Certifique-se que seu projeto faz o setup do ambiente corretamente, como, por exemplo realizar as migrações de banco, criação de usuário inicial e qualquer outra config que se fizer necessária

**Importante:** Testes técnicos não funcionais são automaticamente desconsiderados do processo

### Stack Desejada ###
- Django
- Django Celery
- Django Rest Framework

## Desafio Técnico ##
A `Loans For Good` (LFG) é uma empresa multinacional especializada na concessão de crédito e está vindo para o Brasil, para iniciar sua operação, você foi contratado como o primeiro desenvolvedor dela no Brasil e será o responsável por criar a plataforma de empréstimo.

### Requisitos Funcionais ###
O sistema deverá ter uma interface web onde pessoas possam solicitar propostas, nessa interface não será necessário que a pessoa esteja logada no sistema ou mesmo que ela possua um usuário no sistema

O sistema deve oferecer flexibilidade para que o admin do sistema possa configurar quais os campos que a proposta deve conter, ou seja, caberá a alguém de dentro da empresa definir o que deverá ser pedido de informação para o solicitante da proposta

A proposta deverá passar por uma avaliação automatizada através de uma API de Análise de Crédito já desenvolvida (documentação da API disponível em: https://loan-processor.digitalsys.com.br/swagger/index.html), caso a API retorne o status de não aprovado, a proposta deve ser negada automaticamente, caso seja aprovada, deverá ser disponibilizada para avaliação humana.

Deve haver uma listagem dentro do sistema para que o admin visualize as propostas, para aquelas marcadas para análise humana o admin deve poder mudar o status da proposta para 'Aprovada' ou 'Negada'

### Sugestão para o Desenvolvimento ###

- Fazer a interface de preenchimento de propostas numa interface á parte (pode ser usado um framework web como ReactJS, VueJS, Angular ou mesmo só HTML com CSS e JS)
- Essa interface de preenchimento de propostas deve se comunicar com o projeto em Django através de API
- Utilizar o Django Celery para receber as propostas vindo da API Django e realizar a chamada para a API de Análise de Crédito
- Utilizar o Django Admin para toda a parte de back-office (criação dos campos de proposta, análise da proposta, etc)
