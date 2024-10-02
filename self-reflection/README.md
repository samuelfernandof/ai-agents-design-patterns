# Auto-Reflexão (Self-Reflection)

## Resumo
A **auto-reflexão** permite que o agente gere feedback sobre o plano e o processo de raciocínio, oferecendo orientações de refinamento a partir de si mesmo.

## Contexto
Diante dos objetivos e requisitos dos usuários, o agente gera um plano para decompor os objetivos em um conjunto de tarefas a serem realizadas.

## Problema
Um plano gerado pode ser afetado por alucinações do modelo fundamental. Como revisar o plano e os passos de raciocínio e incorporar feedback de forma eficiente?

## Forças
- **Incerteza no raciocínio**: Podem existir inconsistências ou incertezas embutidas no processo de raciocínio do agente, afetando a taxa de sucesso das tarefas e a precisão das respostas.
- **Falta de explicabilidade**: A confiabilidade do agente pode ser comprometida pela falta de transparência e explicabilidade de como o plano é gerado.
- **Eficiência**: Certos objetivos exigem que o plano seja finalizado dentro de um período específico.

## Solução
A ![Figura 11](link-da-imagem) representa uma visão gráfica de alto nível da auto-reflexão. Em particular, a reflexão é um processo de otimização formalizado para revisar e refinar iterativamente a resposta gerada pelo agente. O usuário solicita objetivos específicos ao agente, que gera um plano para atender aos requisitos dos usuários. Em seguida, o usuário pode instruir o agente a refletir sobre o plano e o correspondente processo de raciocínio. O agente revisará a resposta para identificar e localizar erros, gerando então um plano refinado e ajustando seu processo de raciocínio conforme necessário. O plano finalizado será executado passo a passo. A **auto-consistência** exemplifica esse padrão.

## Consequências

### Benefícios
- **Certeza no raciocínio**: Os agentes podem avaliar suas próprias respostas e procedimentos de raciocínio para verificar se há erros ou saídas inadequadas e fazer os devidos refinamentos.
- **Explicabilidade**: A auto-reflexão permite que o agente reveja e explique seu processo de raciocínio aos usuários, facilitando uma melhor compreensão do processo de tomada de decisão do agente.
- **Melhoria contínua**: O agente pode atualizar continuamente sua memória ou base de conhecimento e a maneira de formalizar os prompts e conhecimentos, fornecendo saídas mais confiáveis e coerentes aos usuários com menos passos de reflexão.
- **Eficiência**: Por um lado, é uma economia de tempo para o agente autoavaliar sua resposta, pois não há sobrecarga de comunicação adicional em comparação com outros padrões de reflexão. Por outro lado, o agente pode fornecer respostas mais precisas no futuro, reduzindo o consumo geral de tempo de raciocínio considerando a melhoria contínua.

### Desvantagens
- **Incerteza no raciocínio**: O resultado da avaliação depende da complexidade da auto-reflexão e da competência do agente em avaliar suas respostas geradas.
- **Sobrecarga**: i) A auto-reflexão pode aumentar a complexidade de um agente, o que pode afetar o desempenho geral. ii) Refinar e manter agentes com capacidades de auto-reflexão requer especialização e um processo de desenvolvimento especializado.

## Usos Conhecidos
- **Reflexion**: Reflexion emprega um modelo de auto-reflexão que pode gerar feedback nuançado e concreto com base no status de sucesso, na trajetória atual e na memória persistente.
- **Agente Bidder**: Um módulo de replano neste agente utiliza a auto-reflexão para criar novos planos textuais com base no status do leilão e em novas informações contextuais.
- **Agentes Gerativos**: Os agentes realizam reflexão duas ou três vezes ao dia, primeiro determinando o objetivo da reflexão de acordo com as atividades recentes, e então gerando uma reflexão que será armazenada na memória.


