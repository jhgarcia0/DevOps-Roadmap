# Progresso: variaveis de ambiente

Data: 2026-11-12

## Atividade concluida

Laboratorio realizado no Bash do Ubuntu/WSL. As variaveis temporarias foram
removidas ao final e nenhum arquivo foi criado.

## Conceitos demonstrados

- `HOME` e uma variavel de ambiente que informa a pasta pessoal do usuario.
- `$nome` pede ao Bash que expanda uma variavel antes de executar o comando.
- `nome=valor` cria uma variavel no Bash atual.
- Uma variavel interna do Bash nao e herdada automaticamente por processos
  filhos.
- `export nome` inclui a variavel no ambiente entregue a novos filhos.
- `export -n nome` remove a marca de exportacao sem apagar o valor no Bash
  atual.
- `unset nome` remove a variavel do Bash atual.
- `bash -c 'comando'` inicia um Bash filho para executar o texto fornecido.
- `NOME=valor comando` fornece uma variavel apenas ao ambiente daquele comando
  e de seus descendentes, sem alterar o Bash pai.
- Processos ja existentes nao recebem mudancas de ambiente retroativamente.

## Evidencia de compreensao

O aluno demonstrou que uma variavel nao exportada existe no Bash pai e nao no
filho, explicou que `export` permite a heranca por novos subprocessos e testou
uma variavel limitada a um unico comando.

## Proximo assunto

Aplicar variaveis de configuracao e codigos de saida em um pequeno script.
