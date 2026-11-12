# Progresso: permissoes no Linux

Data: 2026-11-12

## Atividade concluida

Laboratorio realizado no Ubuntu/WSL com um arquivo temporario em `/tmp`. O
arquivo foi removido ao final para nao deixar artefatos no computador de
trabalho.

## Conceitos demonstrados

- `id` mostra a identidade do usuario e os grupos dos quais ele participa.
- `rw-------` equivale a `600`: apenas o proprietario pode ler e escrever.
- `rwx------` equivale a `700`: apenas o proprietario pode ler, escrever e
  executar.
- `chmod 700` define o estado completo das permissoes; `chmod u+x` adiciona
  apenas execucao ao proprietario.
- Executar um script diretamente exige o bit `x` e um interpretador indicado
  pelo shebang.
- `bash arquivo` nao concede privilegios administrativos. O Bash continua
  executando como o usuario atual e precisa conseguir ler o arquivo.
- A permissao para remover um arquivo depende do diretorio pai, nao da
  permissao de escrita do proprio arquivo.
- Em `/tmp`, o sticky bit permite que cada usuario remova os arquivos que lhe
  pertencem.
- `sudo` e `chmod` resolvem problemas diferentes: o primeiro muda a identidade
  efetiva do comando; o segundo altera permissoes do arquivo.

## Evidencia de compreensao

O aluno interpretou corretamente `rw-------`, preferiu conscientemente a
notacao numerica, explicou quem pode operar um arquivo com permissao `700` e
identificou que um arquivo `000` nao pode ser removido quando falta permissao de
escrita no diretorio pai.

## Proximo assunto

Processos, sinais e codigos de saida no Linux.
