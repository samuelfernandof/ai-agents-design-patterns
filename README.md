![Descrição da Imagem](https://raw.githubusercontent.com/samuelfernandof/ai-agents-design-patterns/main/Blue%20and%20Green%20Corporate%20project%20phases%20chart%20graph%20(1).png)

## Resumo

Foundation Models (FMs) são a base das tecnologias de inteligência artificial generativa (GenAI) e têm atraído atenção significativa de acadêmicos e indústrias. Em particular, os modelos de linguagem de grande escala (LLMs) destacam-se pela sua capacidade de entender e gerar conteúdo humano, impulsionando o desenvolvimento de uma ampla gama de tarefas que utilizam esses modelos.

Com o crescimento do interesse em agentes autônomos baseados em FMs, como AutoGPT e BabyAGI, esses agentes podem assumir um papel proativo para alcançar metas definidas pelos usuários. No entanto, a construção e implementação de agentes baseados em FM apresentam desafios, como a dificuldade em compreender e executar tarefas complexas, a limitação de informações contextuais fornecidas pelos usuários e a falta de explicabilidade em suas arquiteturas internas.

## Contribuições do Repositório

- **Catálogo de Padrões:** Uma coleção de padrões arquitetônicos que oferece soluções de design para implementações práticas de agentes.
- **Ecosistema de Agentes:** Um guia com anotações sobre padrões arquitetônicos para auxiliar no design e desenvolvimento de agentes baseados em FM.
- **Análise Curada:** Cada padrão inclui contexto de aplicação, problemas abordados, benefícios e trade-offs em atributos de qualidade de software, usos conhecidos no mundo real e relações com outros padrões.

Este repositório visa ser uma fonte de referência para profissionais que desejam entender e aplicar padrões de design em agentes baseados em modelos de fundação.

<h2>Padrões de Agentes</h2>
<table>
    <thead>
        <tr>
            <th>Padrão</th>
            <th>Descrição</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><a href="https://arxiv.org/abs/2210.03629">Criador de meta passivo</a></td>
            <td>Analisa os prompts articulados dos usuários através da interface de diálogo para preservar a interatividade, busca de metas e eficiência.</td>
        </tr>
        <tr>
            <td><a href="https://pku-proagent.github.io/">Criador de meta proativo</a></td>
            <td>Antecipar as metas dos usuários ao entender as interações humanas e capturar o contexto por meio de ferramentas relevantes, para melhorar a interatividade, a busca de metas e a acessibilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_OTIMIZACAO_DE_PROMPT_RESPOSTA">Otimizador de prompt/saídas</a></td>
            <td>Otimizando os prompts/respostas de acordo com o conteúdo de entrada ou saída desejado e formato para fornecer padronização, alinhamento de metas, interoperabilidade e adaptabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DOS_RAG_AGENTS">RAG-Agents</a></td>
            <td>Melhora a atualizabilidade do conhecimento dos agentes enquanto mantém a privacidade dos dados de implementações de modelos/base de fundação on-premise.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_CONSULTA_UNICA_AO_LLM">Consulta única ao LLM</a></td>
            <td>Acesse o modelo de fundação em uma única instância para gerar todas as etapas necessárias do plano para eficiência de custo e simplicidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_CONSULTA_INCREMENTAL">Consulta incremental</a></td>
            <td>Acesse o modelo de fundação em cada etapa do processo de geração de planos para fornecer contexto suplementar, melhorar a certeza do raciocínio e a explicabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DO_GERADOR_DE_PLANOS_DE_CAMINHO_UNICO">Gerador de planos de caminho único</a></td>
            <td>Orquestra a geração de etapas intermediárias que levam à realização da meta do usuário para melhorar a certeza do raciocínio, coerência e eficiência.</td>
        </tr>
        <tr>
            <td><a href="URL_DO_GERADOR_DE_PLANOS_DE_MULTIPLOS_CAMINHOS">Gerador de planos de múltiplos caminhos</a></td>
            <td>Permite a criação de múltiplas escolhas em cada etapa intermediária para alcançar as metas dos usuários, melhorando a certeza do raciocínio, coerência, alinhamento às preferências humanas e inclusividade.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_AUTO_REFLEXAO">Auto-reflexão</a></td>
            <td>Permite que o agente gere feedback sobre o plano e o processo de raciocínio e forneça orientações de refinamento a partir de si mesmo para melhorar a certeza do raciocínio, explicabilidade, melhoria contínua e eficiência.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_REFLEXAO_CRUZADA">Reflexão cruzada</a></td>
            <td>Usa diferentes agentes ou modelos de fundação para fornecer feedback e refinar o plano gerado e o processo de raciocínio para melhor certeza do raciocínio, explicabilidade, inclusividade e escalabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_REFLEXAO_HUMANA">Reflexão/feedback humana</a></td>
            <td>Coleta feedback dos humanos para refinar o plano e o processo de raciocínio, para alinhar efetivamente às preferências humanas, melhorando a contestabilidade e a eficácia.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_COOPERACAO_BASEADA_EM_VOTACAO">Colaboradores por votação</a></td>
            <td>Permite a expressão livre de raciocínios entre agentes e chega a um consenso por meio da submissão de seus votos para preservar justiça, responsabilidade e inteligência coletiva.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_COOPERACAO_BASEADA_EM_PAPEIS">Colaboradores por papéis</a></td>
            <td>Atribui papéis diversos e finaliza decisões de acordo com os papéis dos agentes para facilitar a divisão de trabalho, tolerância a falhas, escalabilidade e responsabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_COOPERACAO_BASEADA_EM_DEBATE">Colaboradores por debate</a></td>
            <td>Fornece e recebe feedback entre múltiplos agentes que ajustam os pensamentos e comportamentos durante o debate com outros agentes até que um consenso seja alcançado, para melhorar adaptabilidade, explicabilidade e pensamento crítico.</td>
        </tr>
        <tr>
            <td><a href="URL_DAS_BARREIRAS_MULTIMODAIS">Guardrails multimodais</a></td>
            <td>Controla as entradas e saídas dos modelos de fundação para atender a requisitos específicos, como requisitos do usuário, padrões éticos e leis, para melhorar robustez, segurança, alinhamento de padrões e adaptabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DO_REGISTRO_DE_AGENTES_FERRAMENTAS">Registro de agentes/ferramentas</a></td>
            <td>Mantém uma fonte unificada e conveniente para selecionar diversos agentes e ferramentas para melhorar a descobribilidade, eficiência, adequação das ferramentas e escalabilidade.</td>
        </tr>
        <tr>
            <td><a href="URL_DO_ADAPTADOR_DE_AGENTES">Adaptadores </a></td>
            <td>Conecta o agente e as ferramentas aprendendo novas interfaces e convertendo interfaces incompatíveis em esperadas, garantindo interoperabilidade e adaptabilidade, além de reduzir custos de desenvolvimento.</td>
        </tr>
        <tr>
            <td><a href="URL_DA_AVALIACAO_DE_AGENTES">Avaliadores </a></td>
            <td>Fornece interface para conectar o agente e ferramentas externas para a conclusão de tarefas, garantindo a adequação funcional e adaptabilidade com maior flexibilidade.</td>
        </tr>
    </tbody>
</table>
