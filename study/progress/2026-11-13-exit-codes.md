# Progresso: configuracao e codigos de saida

Data: 2026-11-13

## Atividade concluida

Foi criado um script temporario no Ubuntu/WSL para validar a variavel
`APP_ENV`. O arquivo e as variaveis temporarias foram removidos ao final.

## Conceitos demonstrados

- `$(comando)` substitui a expressao pela saida do comando.
- `mktemp` cria arquivos temporarios com nomes unicos e permissao restrita.
- `>` redireciona a saida normal e substitui o conteudo do destino.
- Aspas simples preservam `$VAR` literalmente; aspas duplas permitem expansao.
- `-z` testa se um texto tem tamanho zero.
- `exit 1` encerra um script indicando falha.
- O codigo `0` indica sucesso; codigos diferentes de zero indicam falha.
- `$?` e um valor a ser expandido; `echo "$?"` o imprime. Executar `$?`
  isoladamente tenta executar um comando com aquele numero.
- O codigo `127` normalmente indica comando nao encontrado.
- `&&` executa o proximo comando apenas apos sucesso.
- `||` executa o proximo comando apenas apos falha.
- Uma variavel atribuida antes de um comando vale apenas para aquela execucao.
- `stdout`, `stderr` e o codigo de saida sao mecanismos independentes: os dois
  primeiros transportam texto e o ultimo comunica sucesso ou falha.

## Evidencia de compreensao

O aluno implementou dois caminhos no script: falha sem `APP_ENV` e sucesso com
`APP_ENV=test`. Em seguida, usou `&&` e `||` para continuar ou interromper uma
sequencia de comandos de acordo com o codigo retornado.

## Proximo assunto

Logs, `stdout`, `stderr` e redirecionamento na pratica.
