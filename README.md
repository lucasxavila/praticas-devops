# Desafio: Implementação de Práticas DevOps em um Ambiente Empresarial Fictício

> ## Descrição da empresa
>
>A **Tech** é uma empresa fictícia especializada em desenvolvimento de software, que oferece soluções inovadoras para clientes de diversos setores. Sua missão é simplificar a vida das pessoas através da tecnologia.
>
>### Equipe:
>
>- Desenvolvimento: 14 desenvolvedores com experiência em Java, C# e JavaScript. Apenas um profissional tem conhecimento em Delphi, a linguagem do sistema legado.
>- Operações: A equipe de operações, composta por 4 profissionais, enfrenta desafios para manter a infraestrutura de TI e os sistemas em funcionamento eficiente, frequentemente lidando com problemas de
>escalabilidade e desempenho.
>
> ### Projetos em andamento
>
> 1. Sistema de Gestão de Vendas (LEGADO): Um aplicativo para gerenciamento de vendas que inclui controle de estoque, emissão de notas fiscais e relatórios de vendas.
> 2. Plataforma de E-commerce: uma plataforma de e-commerce escalável para clientes do setor varejista.
>
>### Descrição dos processos atuais da empresa
>
> 1. **Entrega de Código:** Após a conclusão do desenvolvimento de um novo recurso, os desenvolvedores preparam um pacote de implantação e o encaminham à equipe de operações.
> 2. **Deploy:** O deploy é realizado manualmente no ambiente de produção, sem seguir um procedimento padronizado ou utilizar automação.
> 3. **Testes:** A equipe de operações conduz testes manuais no ambiente para verificar a funcionalidade e a integridade do código após o deploy em produção.
> 4. **Monitoramento:** Após o deploy, a equipe de operações monitora manualmente o sistema de logs do servidor, para identificar problemas ou falhas que possam surgir.
>
> ### Dados de desempenho:
>
> - Tempo médio entre a entrega do código e o deploy: 2 dias.
> - Taxa de sucesso dos deploys manuais: 80%.
> - Número de incidentes após o deploy: média de 2 por semana.
> - Tempo médio de recuperação (MTTR) de incidentes: 4 horas.

## Implementação das Prática DevOps

### Etapas do projeto:
1. Diagnóstico Cultural (C de CALMS)
- O principal ponto de atrito na empresa fictícia é a falta de colaboração e o processo manual de entrega e implantação. A equipe de Desenvolvimento passa o código para Operações, que por sua vez, tem a responsabilidade de fazer tudo manualmente (deploy, testes e monitoramento), trazendo um mentalidade de "muro de responsabilidade" e deixando a integração entre equipes de lado, o que vai contra a cultura DevOps.

2. Automação (A de CALMS)
- A solução de automação deve ser um pipeline de CI/CD (Integração Contínua/Entrega Contínua), com um plano de implementação:
  - Centralizar os logs;
  - Automatizar a criação do pacote de implantação e a execução dos testes (CI);
  - Automatizar o deploy em ambientes de teste e de produção (CD);
  - Configurar alertas automatizados sobre falhas no pipeline de CI/CD e monitoramento de logs;
  - Adotar uma ferramenta de monitoramento de desempenho de aplicações (APM);
 
3. Mensuração e Compartilhamento de Conhecimento (M e S de CALMS)
- Para mensuração, métricas que podem ser estabelecidas para avaliar o impacto das automações, seriam:
  - Tempo de ciclo (Lead Time): Tempo médio desde que o código é "committado" até que seja implantado em produção;
  - Frequência de Implantação (Deployment Frequency): Quantas vezes a empresa implanta código em produção por dia/semana;
  - Tempo Médio para Recuperação (MTTR - Mean Time to Recovery): O tempo que leva para restaurar o serviço após uma falha;
  - Taxa de Falha de Implantação (Change Failure Rate): A porcentagem de implantações que resultam em falha (incidentes, rollbacks, etc.);
 
- Para compartilhament, o sabendo que tem só um profissional que sabe Delphi (síndrome da pessoa-herói), o plano pode ser o seguinte:
  - Sessões de "Show and Tell";
  - Documentação centralizada e contínua;
  - Canais de comunicação dedicados;
  - Reuniões de revisão pós-incidente ("post-mortems") sem culpa;
 
4. Três Maneiras
- Primeira Maneira (Acelerar o Fluxo): Oportunidades para acelerar a entrega de valor aos clientes, são: Identificar e eliminar o gargalo do deploy manual e reduzir o tamanho dos lotes de trabalho;
- Segunda Maneira (Ampliar o Feedback): Alguns mecanismos para o feedback contínuo, seria o feedback rápido para os desenvolvedores, feedback do monitoramento (monitoramento de logs, deve ser acessível para ambas equipes) e sessões de post-mortem;
- Terceira Maneira (Experimentar e Aprender): Incentivar a experimentação criando um ambiente onde as equipes possam tentar novas ferramentas, técnicas ou processos sem medo de falhar, aprendizado como prioridade onde em vez de culpar alguém, a pergunta deve ser: "O que podemos aprender com isso para evitar que aconteça novamente?" e promover a inovação;
