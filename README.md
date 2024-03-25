# ponderada_progSem7

## K6:

A plataforma K6 surge como uma solução avançada no âmbito de testes de carga, destinada a simular a atividade de múltiplos usuários em aplicativos web, especificamente APIs e back-ends, com o objetivo de identificar a capacidade máxima e as vulnerabilidades diante de elevadas demandas. Esta ferramenta permite aos desenvolvedores a elaboração de scripts em JavaScript, com a possibilidade de inserir solicitações HTTP, intervalos temporais para emular a interação do usuário, e a avaliação das respostas obtidas dos servidores. Diferenciando-se por sua adaptabilidade, a K6 habilita a experimentação com várias configurações de teste, incluindo o escalonamento gradual de carga, a estabilização do volume de acessos e a redução sequencial da demanda. A geração de relatórios direto no terminal enriquece o processo de diagnóstico, simplificando a detecção de falhas de desempenho e acelerando o processo decisório para aprimoramentos eficazes.

## Etapas do Teste

- **Escala até 20 usuários:** A carga sobre os endpoints aumenta gradualmente até atingir 20 usuários ativos simultâneos no primeiro minuto, avaliando a capacidade de resposta inicial do sistema.

- **Estabilização em 20 usuários:** Após alcançar a marca de 20 usuários, mantém-se essa carga por três minutos, testando a estabilidade e performance do sistema sob demanda constante.

- **Redução para 0 usuários:** Na etapa final, reduz-se a carga até zero, analisando a habilidade do sistema em se recuperar e estabilizar após a cessação do tráfego.

## Análise dos Resultados

- Testes focados em quatro dos sete endpoints, abrangendo funcionalidades de consulta e atualização.

### Resumo dos Resultados HTTP

- Sucesso nas 794 solicitações GET (status 200) e POST (status 201), confirmando a eficácia das operações.
- Eficiência na transferência de dados, com 668 KB recebidos e 390 KB enviados.
- Tempos de conexão e transmissão adequados, com destaque para o tempo de espera médio (316.04 ms) como um possível ponto de melhoria.

### Lições Aprendidas

A realização dos testes destacou a necessidade de scripts específicos para cada endpoint, permitindo uma avaliação precisa da capacidade de cada um em suportar cargas. Isso evita a generalização dos testes por módulo e favorece uma análise mais detalhada.

