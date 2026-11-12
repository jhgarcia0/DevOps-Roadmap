# Aula 1: permissoes no Linux

## Objetivo

Ao final desta atividade, voce deve conseguir diagnosticar por que um arquivo
nao pode ser executado e escolher uma correcao sem recorrer automaticamente a
privilegios administrativos.

## Modelo mental

Cada arquivo possui:

- um usuario proprietario;
- um grupo proprietario;
- permissoes para o proprietario, o grupo e os demais usuarios.

As permissoes basicas sao leitura (`r`), escrita (`w`) e execucao (`x`). Em um
diretorio, `x` significa que o usuario pode atravessa-lo e acessar itens dentro
dele.

`sudo` muda o usuario que executa o comando. `chmod` muda as permissoes do
arquivo. Portanto, eles resolvem problemas diferentes.

## Laboratorio

Execute a atividade em Ubuntu/WSL ou outra maquina Linux.

1. Crie uma pasta para o laboratorio e entre nela.
2. Crie `hello.sh` com este conteudo:

   ```bash
   #!/usr/bin/env bash
   echo "Ola, $USER"
   ```

3. Tente executar `./hello.sh` e registre o resultado.
4. Inspecione as permissoes e o proprietario com `ls -l hello.sh`.
5. Execute o arquivo usando `bash hello.sh` e explique por que isso pode
   funcionar mesmo quando `./hello.sh` falha.
6. Adicione permissao de execucao ao proprietario com `chmod u+x hello.sh`.
7. Execute novamente com `./hello.sh`.
8. Remova apenas a permissao de leitura do proprietario, observe o resultado e
   depois restaure-a.

## Perguntas para concluir

Registre as respostas abaixo ou no diario de progresso:

1. Qual era a permissao inicial do arquivo?
2. Por que `bash hello.sh` e `./hello.sh` seguem caminhos diferentes?
3. Quem pode executar o arquivo depois de `chmod u+x`?
4. Em qual situacao `sudo` seria apropriado, e qual risco ele introduz?

## Criterio de conclusao

A atividade esta concluida quando voce consegue olhar uma saida de `ls -l`,
identificar proprietario, grupo e permissoes, e explicar a correcao escolhida.

Nao e necessario decorar a representacao numerica das permissoes nesta aula.
