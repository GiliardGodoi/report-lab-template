# Organização do projeto

Instruções gerais sobre a organização da escrita de relatório no Overleaf.

Os diretórios e arquivos foram estruturados de maneira a organizar em um único projeto do Overleaf a escrita diversos relatórios conforme a necessidade.

```
.\project
    .\figuras               # -> todas as figuras vão nesta pasta
        .\relatorio01       # -> as figuras de cada relatório são organizadas em subpastas
        .\relatorio02       # assim temos a possibilidade de utilizar também uma figura de um relatório em outro
        .\relatorio03       # sem a necessidade de especificar um caminho para fora do diretório atual utilizando o marcador ..
    .\referencias           
        bibliografia.bib    # O projeto suporta somente um arquivo de referências
    .\relatorios            # Os relatórios podem ficar separados por arquivos
        01-relatorio.tex
        02-relatorio.tex
        03-relatorio.tex
        template.tex        # arquivo base que serve para todos os relatórios
    .\tabelas               # -> tabelas muito grandes podem ser colocadas 
        .\relatorio02       # tabelas podem ser organizadas por diretorios que representam relatórios
            01-tabela.tex   # a inclusão de uma tabela pode ser feita pelo comando \input{tabelas/relatorio03/nome-do-arquivo}
            02-tabela.tex
            03-tabela.tex
    .\temporario            # pasta para organizar arquivos temporários
    algorithm2e.sty         # arquivo necessário para a customização do pacote para escrita de algoritmos
    main.tex                # Arquivo inicial que fará referência a qual arquivo queremos importar
                            # para imprimir e trabalhar com um relatório específico é necessário referênciar o arquivo do relatório
                            # no arquivo main.tex como o comando \input{relatorios/nome-do-arquivo}                         
```

## Dica para nomeação de labels

O comando ```\label{}``` define labels para facitar a referência e numeração de objetos no texto: tabelas, figuras, seções, algoritmos e até mesmo suas linhas.

O Ovearleaf no entanto parece manter o registro de todos os labels de todos os documentos ```.tex``` do projeto e isso pode levar alguma confusão de referências.
Então nesse projeto recomendamos que seja adotada a seguinte padronização dos labels

    - tipo:
        - sec: ->  para seções
        - tab: ->  para tabelas
        - fig: ->  para figuras
        - alg: ->  para algoritmos
    - seguido pelo número do relatório: 02, 03, etc.
    - seguido pela descricao das palavras chaves que identifica os objetos.
    - cada um desses elementos deve ser  separado pelo caracter :
    
Exemplos:

```
    \label{sec:03:metodologia}
    \label{fig:03:boxplot:iteracoes}
    \label{tab:03:ga:binario:resultados}
```

## Autor 

Criado por Giliard Almeida de Godoi <giliardgodoi@alunos.utfpr.edu.br>. Atualizado em 05 de maio de 2020.





