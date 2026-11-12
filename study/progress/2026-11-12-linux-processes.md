# Progresso: processos e sinais no Linux

Data: 2026-11-12

## Atividade concluida

Laboratorio realizado no Ubuntu/WSL com processos `sleep`. Todos os processos
temporarios foram encerrados ao final.

## Conceitos demonstrados

- Um programa em execucao e um processo.
- PID identifica um processo no sistema; PPID identifica seu processo pai.
- `$!` e um parametro do Bash com o PID do ultimo processo iniciado em
  segundo plano pelo proprio shell.
- O valor de `$!` deve ser capturado imediatamente quando sera reutilizado.
- O numero de job, como `%1`, pertence ao Bash atual e e diferente do PID.
- Primeiro plano ocupa o terminal; segundo plano devolve o prompt; um processo
  parado continua existindo sem avancar.
- `ps` fornece uma fotografia dos processos; `jobs` mostra os jobs controlados
  pelo Bash atual.
- Nos estados observados, `R` significa executando ou pronto para executar,
  `S` significa aguardando de forma interrompivel e `T` significa parado.
- `kill` envia sinais. Foram usados `TERM` para encerrar, `STOP` para pausar e
  `CONT` para retomar.
- `Ctrl+C` envia `SIGINT` ao processo em primeiro plano; `Ctrl+Z` o suspende.
- `$?` guarda o codigo do comando imediatamente anterior: zero indica sucesso
  e valores diferentes de zero indicam falha ou encerramento por sinal.
- Um processo pode existir sem consumir CPU enquanto aguarda um evento ou
  temporizador.

## Evidencia de compreensao

O aluno diferenciou PID de job, explicou o escopo de `$!`, pausou e retomou um
processo em segundo plano e identificou por que `sleep` aparece no estado `S`.

## Proximo assunto

Variaveis de ambiente e uso de codigos de saida em scripts.
