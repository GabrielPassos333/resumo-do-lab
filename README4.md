RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

    Data: 13 de Agosto de 2025

    Empresa: PharmaNos S.A.

    Responsável: GP

Introdução

Este relatório apresenta o processo de implementação de ferramentas na empresa PharmaNos S.A., realizado por GP. O objetivo do projeto foi elencar 3 serviços AWS (Amazon S3, Amazon RDS e AWS Lambda), com a finalidade de otimizar a infraestrutura, aumentar a agilidade operacional e realizar diminuição de custos imediatos.
Descrição do Projeto

O projeto de implementação de ferramentas foi em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:
Etapa 1:

    Nome da ferramenta: Amazon S3 (Simple Storage Service)

    Foco da ferramenta: Armazenamento de objetos escalável, seguro e durável.

    Descrição de caso de uso: Implementação do Amazon S3 para armazenar de forma segura e econômica grandes volumes de dados não estruturados, como documentos regulatórios digitalizados, logs de auditoria de conformidade, backups de bancos de dados e relatórios de vendas. Sua escalabilidade e durabilidade garantem que dados críticos de inventário e pedidos estejam sempre disponíveis e protegidos contra falhas. Além disso, a capacidade de versionamento de objetos auxilia na rastreabilidade e na conformidade com regulamentações do setor farmacêutico.

Etapa 2:

    Nome da ferramenta: Amazon RDS (Relational Database Service) - PostgreSQL

    Foco da ferramenta: Gerenciamento e escalabilidade de bancos de dados relacionais na nuvem.

    Descrição de caso de uso: Migração dos bancos de dados relacionais existentes (ex: gestão de estoque, processamento de pedidos, informações de clientes e fornecedores) para o Amazon RDS com PostgreSQL. Isso elimina a necessidade de gerenciamento de infraestrutura de banco de dados, permitindo que a equipe de TI da PharmaNos S.A. foque em tarefas de maior valor. O RDS oferece alta disponibilidade, backups automáticos, recuperação de ponto no tempo e escalabilidade simplificada, garantindo a integridade e performance necessárias para as operações transacionais críticas de distribuição.

Etapa 3:

    Nome da ferramenta: AWS Lambda

    Foco da ferramenta: Execução de código sem provisionamento ou gerenciamento de servidores (Serverless Compute).

    Descrição de caso de uso: Desenvolvimento de funções AWS Lambda para automatizar processos de negócio e integrações. Exemplos incluem: processamento de novos pedidos recebidos de parceiros (disparado por eventos em S3 ou filas SQS), atualização automática de níveis de estoque em tempo real após entregas (disparado por eventos de bancos de dados ou APIs), geração de alertas para produtos com baixa validade, e criação de relatórios diários de distribuição. O uso de Lambda permite que a PharmaNos S.A. pague apenas pelo tempo de computação consumido, otimizando drasticamente os custos operacionais e proporcionando escalabilidade instantânea para picos de demanda.

Conclusão

A implementação de ferramentas na empresa PharmaNos S.A. tem como esperado benefícios aprimorar a resiliência e a escalabilidade da infraestrutura de TI, otimizar processos operacionais críticos (como gestão de estoque e pedidos), reduzir custos com manutenção de servidores e licenças de banco de dados, e aumentar a capacidade de inovação e agilidade na resposta às demandas do mercado, o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.
Anexos


Assinatura do Responsável pelo Projeto:

GP
