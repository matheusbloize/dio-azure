# Criando máquinas virtuais na Azure

Antes de criar um recurso na nuvem, é essencial definir o propósito e a necessidade de alta disponibilidade.  
Já que aplicações mal planejadas podem gerar custos excessivos e impactar no orçamento da empresa.

- SLA (Service Level Agreement):
  - Define o tempo máximo aceitável de inatividade do serviço.
  - Dica: Mais 9s no SLA = menor indisponibilidade.
  - Exemplo: 99% permite até 1.68 horas de inatividade/mês, enquanto 99.99% reduz esse tempo para 1 minuto.

- Impacto na Arquitetura:
  - Para cada serviço, é necessário definir o nível de SLA adequado conforme a necessidade do negócio.
  - Recursos nativos da nuvem podem ter SLAs garantidos pelo provedor, enquanto recursos personalizados podem não ter cobertura.
  - Disponibilidade pode ser aumentada através de zonas de disponibilidade e conjuntos de dimensionamento.
  
- Replicação e Redundância:
  - Armazenamento pode ter diferentes níveis de redundância (LRS, GRS, ZRS, GZRS).  
  - Mais redundância melhora a disponibilidade, mas também aumenta os custos.