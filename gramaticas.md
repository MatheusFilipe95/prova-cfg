# Gramáticas EBNF


Considere as gramáticas no formato EBNF abaixo onde símbolos em letras minúsculas são considerados não-terminais e os símbolos em letra maiúsculas são considerados terminais e o símbolo inicial é representado pela letra "s". Produções vazias são representadas por ε.

**G1**
```
s : A s B
  | A B
```

**G2**
```
s : A B s
  | ε
```

**G3**
```
s : r A
r : A B r
  | ε
```

**G4**
```
s : A
  | s s B
```

**G5**
```
s : r 
  | t

t : r A
  | ε

r : t B
  | ε
```

**G6**
```
s : A
  | B
  | r

r : s s
  | ε
```

**Parte I (competência: cfg 4 pts)**

Classifique as sequências de símbolos abaixo de acordo com qual gramática elas pertencem. Uma sequência pode pertencer a mais de uma gramática. Deixamos a letra (a) resolvida no formato esperado para cada resposta.

Mantenha o ε como resposta das strings que não obedecem a nenhuma gramática.

a) AB: G1, G2, G5, G6
b) B: G5, G6
b) ABA: G3, G5, G6
c) ABBA: G5, G6
d) ABABAB: G2, G5, G6
e) BABA: G5, G6
f) AABB: G1, G5, G6
h) AABAB: G4, G5, G6

**Parte II (medalha cfg, se acertar todas)**

Resuma todas as gramáticas acima com uma descrição informal que diga intuitivamente o que cada linguagem representa. Você pode atribuir significados específicos aos símbolos terminais A e B, se necessário.

G1: Sequencia: A seguido de B, quantidade de A = quantidade de B.
G2: Sequência: AB(s).
G3: Sequência: AB(s) com A no final.
G4: Sequência: Elemento inicial A e final B ou sequência com A.
G5: vazio e ou combinação: A(s) e B(s)   
G6: vazio e ou combinação: A(s) e B(s)   
