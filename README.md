# apontamentoHoras

Linguagem : Python3.6+

Proposito : Seja um projeto de software A. Este projeto se constitui de uma lista de pacotes de trabalho L. Para cada elemento de L, existe um número de horas estimadas. Este repositorio tem por objetivo criar git hooks e toda infra necessaria(talvez fuse??) para que não seja necessario apontar horas manualmente, ou seja, no ato de commitar o hook descobrirá quais pacotes(na forma de issues) foram atacados e logará automaticamente essas horas.

Restrições : o projeto deve rodar em Gnu, não sendo em absoluto necessario pensar em roda-lo no Windows.

Projeto : um sistema fuse de log (provavelmente será apenas utilizado um apropriado) logará as mudanças de arquivos realizadas. Quando ocorrer um commit, um hook será invocado e descobrirá qual issue foi trabalhada nesse commit. Se mais de uma issue foi trabalhada, ele não deixa o commit ocorrer, pois cada commit deve endereçar um único problema.

Como o hook descobrirá qual issue foi trabalhada? Deve existir um arquivo de configuração com o seguinte conteudo :

"
bugtracker = github

  


#comentarios são bem-vindos, eles vão do '#' até
#o fim da linha
"

Neste arquivo esta discriminado que as relações entre issues e testes serão obtidas do bugtracker correspondente.


Isso significa que a descrição das issues deve mudar para :

"
lorem-ipsum ...

testes/a
testes/b
testes/c.py
etc, etc, etc
"
