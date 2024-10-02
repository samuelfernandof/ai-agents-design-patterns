# Gerador de Planos Multipath

## Resumo
O **gerador de planos multipath** permite a criação de múltiplas opções em cada etapa intermediária, visando alcançar os objetivos dos usuários.

## Contexto
Um agente é considerado uma "caixa preta" para os usuários, enquanto estes podem se importar com o processo de como um agente atinge seus objetivos.

## Problema
Como um agente pode gerar uma solução de alta qualidade, coerente e eficiente, considerando inclusividade e diversidade, quando apresentado a uma tarefa ou problema complexo?

## Forças
- **Subespecificação**: Usuários podem atribuir tarefas com alta abstração, o que pode ser desafiador para os agentes lidarem com a incerteza ou ambiguidade no contexto fornecido.
- **Coerência**: Usuários e outras ferramentas/agentes interagentes esperarão respostas ou diretrizes coerentes para alcançar certos objetivos.
- **Alinhamento às preferências humanas**: Certos objetivos exigem que os agentes capturem as preferências dos usuários para fornecer soluções personalizadas.
- **Simplificação excessiva**: Para tarefas complexas, os agentes podem simplificar demais o processo de raciocínio, resultando em soluções que não atendem às exigências dos usuários.

## Solução
A ![Figura 10](link-da-imagem) ilustra uma representação gráfica de alto nível do gerador de planos multipath. Baseado no gerador de planos unidirecionais, o gerador de planos multipath pode criar várias opções em cada etapa em direção à realização dos objetivos. As preferências dos usuários podem influenciar os passos intermediários subsequentes, levando a diferentes planos finais. O uso de agentes e ferramentas envolvidos será ajustado de acordo. O conceito de **Tree-of-Thoughts** exemplifica esse padrão de design.

## Consequências

### Benefícios
- **Certeza no raciocínio**: O gerador de planos multipath pode gerar um plano com múltiplas escolhas de passos intermediários para resolver a incerteza ou ambiguidade no processo de raciocínio.
- **Coerência**: Os usuários interagentes, agentes e ferramentas recebem um caminho claro e coerente em direção aos objetivos finais.
- **Alinhamento às preferências humanas**: Os usuários podem confirmar cada passo intermediário para finalizar o planejamento, absorvendo assim as preferências humanas na estratégia personalizada gerada.
- **Inclusividade**: O agente pode especificar múltiplas direções no processo de raciocínio para tarefas complexas.

### Desvantagens
- **Sobrecarga**: A decomposição de tarefas e a geração de múltiplos planos podem aumentar a sobrecarga de comunicação entre o usuário e o agente.
