# Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

- Computação e Serviços de Rede no Azure
  - Revisão geral sobre computação no Azure, cobrindo instâncias, contêineres, web apps e área de trabalho virtual.
  - Agora, foco na prática: criação de máquinas virtuais (VMs).

- Criação de Máquinas Virtuais no Azure
  - Opção de criação manual ou uso de configurações pré-definidas para facilitar o processo.
  - Algumas opções incluem ambientes otimizados para testes ou produção.
  - Escolha da família de VM com base no tipo de carga de trabalho (ex.: série F para otimização de memória).
  - Algumas VMs vêm com aplicações prontas, como WordPress em Linux.

- Recursos Criados Automaticamente ao Criar uma VM
  - O Azure configura diversos recursos automaticamente, como:
    - Endereço IP
    - Grupo de segurança
    - Chave SSH
    - Banco de dados e cache (ex.: MySQL e Redis)
  - A vantagem disso é que evita a necessidade de criar esses recursos manual e separadamente.

- Opções de Disponibilidade e Escalabilidade
  - Opções de disponibilidade determinam a redundância da infraestrutura.
  - Zonas de disponibilidade permitem separar os recursos em diferentes data centers dentro de uma região.
  - Conjuntos de dimensionamento (Scale Sets) permitem escalabilidade automática para atender picos de demanda.

- Configuração de Escalabilidade Automática
  - Definição do número mínimo e máximo de máquinas virtuais.
  - Critérios para aumentar ou diminuir instâncias com base no uso da CPU.
  - Exemplo:
    - Se o uso da CPU passar de 80%, adiciona-se mais instâncias.
    - Se cair abaixo de 40%, reduz-se a quantidade de máquinas.
  - Essa configuração é útil em eventos como Black Friday, onde a demanda pode variar rapidamente.

- Instâncias Spot no Azure
  - São máquinas virtuais com custo reduzido, porém podem ser desalocadas a qualquer momento se um cliente pagar o valor cheio.
  - Recomendadas para ambientes de desenvolvimento e testes, mas não para produção devido ao risco de interrupção.

- Escolha da Família de VM
  - Diferentes famílias de máquinas atendem diferentes tipos de carga de trabalho:
    - Série D: uso geral.
    - Série B: cargas que não exigem desempenho constante.
    - Série H: otimizadas para alta necessidade de memória.
    - Série DC: foco em segurança e criptografia de dados.
  - Não é necessário decorar todas, pois a escolha depende do cenário específico.