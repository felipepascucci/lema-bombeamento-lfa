# Lema do Bombeamento — Linguagens Formais e Autômatos

Script em Python que aplica o **Lema do Bombeamento** para demonstrar que a linguagem L = { aⁿ bⁿ | n ≥ 0 } **não é regular**, testando todas as divisões possíveis de uma cadeia.

**Tecnologias:** Python 3 (sem dependências externas)

## Como executar

```bash
python bombeamento.py
```

## Relatório da atividade

Trabalho em grupo — integrantes:

Felipe Rafael Tancredi Pascucci  
Giovanna Santos da Silva  
Leonardo Annunciação Rodrigues  
Luan Gabriel Melo da Rocha  
Isabelle Rosa Moura Ferreira  
Kauã da Silva Ferreira  

Disciplina: Linguagens Formais e Autômatos

Professor(a): Sthephany Oliveira

## Definição da Linguagem

A linguagem escolhida é:  
<br/>L = { aⁿ bⁿ | n ≥ 0 }  
<br/>Essa linguagem contém todas as cadeias compostas por uma sequência de 'a's seguida pela mesma quantidade de 'b's. Exemplos válidos incluem: 'ab', 'aabb', 'aaabbb', etc.

## Objetivo

Aplicar o Lema do Bombeamento para verificar se a linguagem L é ou não regular. Isso é feito dividindo uma cadeia w ∈ L em partes x, y, z, testando se ao repetir y, a cadeia ainda pertence à linguagem.

## Cadeia Testada

Cadeia w: "aaaabbbb"  
Comprimento: 8  
Valor de bombeamento p: 4  
Observa-se que |w| ≥ p, portanto é válida para o teste.

## Print/Output do Teste

Analisando cadeia: aaaabbbb, com p = 4

Testando divisao: x='', y='a', z='aaabbbb'
Com i=0: 'aaabbbb' -> NAO pertence a L
Com i=2: 'aaaaabbbb' -> NAO pertence a L

Testando divisao: x='a', y='a', z='aabbbb'
Com i=0: 'aaabbbb' -> NAO pertence a L
Com i=2: 'aaaaabbbb' -> NAO pertence a L

Testando divisao: x='aa', y='a', z='abbbb'
Com i=0: 'aaabbbb' -> NAO pertence a L
Com i=2: 'aaaaabbbb' -> NAO pertence a L

Testando divisao: x='aaa', y='a', z='bbbb'
Com i=0: 'aaabbbb' -> NAO pertence a L
Com i=2: 'aaaaabbbb' -> NAO pertence a L

QUEBRA DO LEMA: A linguagem NAO é regular

## Conclusão

A partir da simulação do lema do bombeamento:  
<br/>\- Encontramos uma divisão da cadeia w = xyz, com |xy| ≤ p e |y| ≥ 1, tal que, ao repetir y, a nova cadeia resultante não pertence à linguagem.  
\- Isso viola a condição do lema do bombeamento, que só se aplica a linguagens regulares.  
<br/>Portanto, concluímos que a linguagem L = { aⁿ bⁿ | n ≥ 0 } não é regular.

## Contexto

Atividade da disciplina Linguagens Formais e Autômatos — Ciência da Computação, UNIP (2025).
