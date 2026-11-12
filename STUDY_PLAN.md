# Plano pessoal de estudos em DevOps

Este documento registra o nivelamento, a trilha e o progresso de `jhgarcia0`.
O objetivo e transformar experiencia em desenvolvimento de software em
competencia pratica para entregar e operar aplicacoes.

## Nivelamento inicial

**Ponto de partida:** desenvolvedor experiente iniciando a transicao para
DevOps. Nao e necessario recomecar por programacao basica nem fazer um curso
completo de Git.

| Area | Nivel inicial | Observacao |
| --- | --- | --- |
| Programacao e automacao | Intermediario/avancado | Experiencia profissional e automacoes em batch |
| Git | Basico funcional | Usa clone e pull; precisa consolidar fetch e colaboracao |
| CI/CD e secrets | Basico consistente | Entende gates de testes e GitHub Secrets |
| Diagnostico e logs | Basico consistente | Procura logs e saturacao de recursos |
| Linux | Basico | Precisa consolidar permissoes, processos e servicos |
| Redes e HTTP | Basico | Precisa consolidar interfaces, portas e headers |
| Docker | Basico | Conhece volumes; precisa consolidar portas e persistencia |
| Observabilidade | Basico | Reconhece CPU e memoria como sinais iniciais |
| Infraestrutura como codigo | Nao iniciado | Terraform/OpenTofu e Ansible ainda nao estudados |
| Cloud | Nao iniciado | Nenhum provedor administrado ate o momento |
| Kubernetes | Nao iniciado | Deve vir depois dos fundamentos |

## Principios do estudo

- Aproximadamente 70% de pratica e 30% de leitura.
- Sintaxe consultavel nao precisa ser decorada.
- Cada assunto deve produzir uma evidencia versionada.
- Usar uma aplicacao pequena como projeto continuo de aprendizado.
- Nao avancar apenas por terminar um curso: avancar ao conseguir diagnosticar,
  explicar e reproduzir o que foi construido.

## Trilha

### Fase 1: Linux operacional

- [ ] Trabalhar em um ambiente Linux real, preferencialmente Ubuntu no WSL.
- [x] Entender usuarios, grupos e permissoes.
- [x] Inspecionar e controlar processos.
- [ ] Trabalhar com variaveis de ambiente, arquivos de configuracao e logs.
- [ ] Automatizar inicio, verificacao e encerramento de uma aplicacao.

**Evidencia:** aplicacao executada como processo Linux, com logs e script de
operacao.

### Fase 2: Redes e HTTP

- [ ] Entender localhost, interfaces, IP privado e `0.0.0.0`.
- [ ] Entender portas, DNS, TCP, HTTP e HTTPS.
- [ ] Inspecionar requests, responses, headers e codigos HTTP.
- [ ] Publicar a aplicacao na rede local.
- [ ] Configurar Nginx como reverse proxy.

**Evidencia:** aplicacao acessivel pela rede por meio do Nginx.

### Fase 3: Docker

- [ ] Diferenciar imagem, container, rede e volume.
- [ ] Criar um Dockerfile adequado para a aplicacao.
- [ ] Dominar mapeamento de portas e variaveis de ambiente.
- [ ] Diagnosticar containers encerrados e consultar seus logs.
- [ ] Executar aplicacao, banco e Nginx com Docker Compose.

**Evidencia:** ambiente completo iniciado com um comando e dados persistentes
apos a recriacao dos containers.

### Fase 4: CI/CD

- [ ] Executar testes e build no GitHub Actions.
- [ ] Interromper o pipeline quando uma validacao falhar.
- [ ] Consumir secrets sem grava-los no repositorio.
- [ ] Criar e publicar uma imagem Docker versionada.

**Evidencia:** pipeline que testa, empacota e publica a aplicacao.

### Fases posteriores

- [ ] Infraestrutura como codigo com Terraform ou OpenTofu.
- [ ] Configuracao de sistemas com Ansible.
- [ ] Um provedor de cloud.
- [ ] Metricas, logs, traces, dashboards e alertas.
- [ ] Kubernetes somente depois dos fundamentos anteriores.

## Registro de progresso

| Data | Atividade | Evidencia | Dificuldades/proximo passo |
| --- | --- | --- | --- |
| 2026-11-12 | Nivelamento inicial | Este documento | Iniciar Linux operacional |
| 2026-11-12 | Permissoes no Linux | [`study/progress/2026-11-12-linux-permissions.md`](study/progress/2026-11-12-linux-permissions.md) | Estudar processos e sinais |
| 2026-11-12 | Processos e sinais | [`study/progress/2026-11-12-linux-processes.md`](study/progress/2026-11-12-linux-processes.md) | Estudar variaveis de ambiente e codigos de saida em scripts |
| 2026-11-12 | Variaveis de ambiente | [`study/progress/2026-11-12-environment-variables.md`](study/progress/2026-11-12-environment-variables.md) | Aplicar configuracao e codigos de saida em um script |

## Proxima atividade

Seguir a aula pratica em
[`study/01-linux-permissions.md`](study/01-linux-permissions.md).
