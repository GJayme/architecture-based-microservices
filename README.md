# Arquitetura baseada em microsserviços
## Microsserviços
Microsserviços São:
- Aplicações comuns;
- Aplicações que possuem objetivos bem definidos;
- Aplicações que fazem parte de um ecossistema;
- Independentes ou autônomos e possuem seu próprio banco de dados. A parte mais complexa de lidar com microsserviçoes de conseguir, pois geralmente um microsserviço é dependente de outra aplicação, se essa outra aplicação cair esse microsserviço irá cair também);
- Aplicações que se comunicam o tempo todo.

## Microsserviços vs Monolítos
- Objetivos / Domínio bem definidos:
  - Monolitos: toda aplicação. Todos os contextos dentro da mesma aplicação.
  - Microsserviços: objetivos definidos.
- Linguagem de programação:
  - Monolitos: Única tecnologia.
  - Microsserviços: Diversas tecnologias (podendo utilizar linguagens que tem objetivos específicos para resolver problemas específicos).
- Deploy:
  - Monolitos: Risco maior de tudo cair.
  - Microsserviços: Menos risco.
- Organizacional das equipes:
  - Monolitos: todas as equipes trabalhando no mesmo sistema.
  - Microsserviços: exemplo: uma equipe por microsserviço
- Começar um projeto / POC:
  - Monolitos: Mais simples começar um projeto.
  - Microsserviços: Mais complexo de começar um projeto.
 
## Quando utilizar microsserviços
- Microsserviço:
  - Escalar times
  - Contexto bem definidos / área de negócio
  - Quando o projeto possuí maturidade nos processos de entrega
  - Quando o projeto possuí maturidade técnica dos times
  - Quando o projeto tem a necessidade de escala de apenas uma parte do meu sistema
  - Quando o projeto tem a necessidade de utilizar tecnologias específicas em partes do sistema
 
## Quando utilizar monolíto
- Monolíto:
  - Quando estamos iniciamos um projeto ou criando uma POC (provas de conceito).
  - Novos projetos onde não conhecemos todo o "domínio"
  - Governança simplificada sobre as tecnologias que serão utilizadas;
  - Facilidade na contratação
  - Facilidade no treinamento dos devs
  - Tudo está no mesmo lugar
  - Compartilhamento claro de libs (shared kernel)
 
## Migração de monolitos para microsserviços
- Separação de contextos (utilizar DDD);
- Evite excesso de granularidade (nanoserviços);
- Verifique dependências (monolito distribuído);
- Planeje o processo de migração dos bancos de dados;
- Eventos:
  - A ideia principal quando se trabalha com microsserviços é de utilizar comunicação assíncrona, ou seja, devem ser mapeados os eventos do sistema e eles sejam disparados para que os microsserviços possãm processá-los.
- Não tenha medo de duplicação de dados
- Consistência eventual:
  - Eventualmente os dados da aplicação não vai estar consistente.
- CI/CD, Testes, Ambientes:
  - Essas partes devem estar muito bem feita para poder seguir para a migração para um microsserviço.
- Comece pelas beiradas:
  - Comece a migraçaão com áreas de menor risco. Com isso a equipe consegue ter experiência e fica mais claro as próximas migrações.
- Padrão de estrangulamento
