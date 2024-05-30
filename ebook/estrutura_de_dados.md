# <h1 align = "Center">**Estruturas de Dados**</h1>

Neste capítulo, exploraremos algumas das estruturas de dados mais fundamentais em Ruby. As estruturas de dados são essenciais para organizar e manipular coleções de dados de forma eficiente.

### **Arrays**
Arrays são coleções ordenadas de objetos, que podem ser acessados por indice.

#### *Criando Arrays*

```ruby
# *Acessando elementos do array*
frutas = ["maça", "banana", "laranja"]
puts frutas[0]  # Saída: maça
puts frutas[1]  # Saída: "banana"

# *Adicionando elementos ao array*
frutas << "uva"
puts frutas # Saída: ["maça", "banana", "laranja", "uva"]

# *Removendo elementos do array*
frutas.delete("banada")
puts frutas # Saída: ["maça", "laranja", "uva"]
```

### **Hashes**
Hashes são coleções de pares chave-valor, onde cada chave é única.

#### Criando um hash

```ruby
pessoa = {nome: "João", idade: 30, cidade: "São Paulo" }

#### Acessando valores do hash
puts pessoa[:nome]  # Saída: João
puts pessoa[:idade] # Saída: 30

#### Adicionando novos pares chave-valor
pessoa[:profisscao] = "Engenherio"
puts pessoa # Saída: { nome: "João", idade: 30, cidade: "São Paulo", profissão: "Engenheiro" }
```

### **Conjuntos (Sets)**
Sets são coleções de elementos não ordenados e únicos. Para usar sets, é necessário requerer a biblioteca 'set'.

```ruby
require 'set'

# Criando um set
conjunto = Set.new([1, 2, 3, 4])

# Adicionando elementos ao set
conjunto.add(5)
puts conjunto  # Saída: #<Set: {1, 2, 3, 4, 5}>

# Removendo elementos do set
conjunto.delete(3)
puts conjunto  # Saída: #<Set: {1, 2, 4, 5}>
```

### **Pilhas(Stacks)**
Pilhas são coleções de elementos que seguem o princípio LIFO (Last In, First Out).

```ruby
# Criando uma pilha
pilha = []

# Adicionando elementos à pilha
pilha.push(1)
pilha.push(2)
pilha.push(3)
puts pilha  # Saída: [1, 2, 3]

# Removendo elementos da pilha
puts pilha.pop  # Saída: 3
puts pilha  # Saída: [1, 2]
```

### **Filas(Queues)**
Filas são coleções de elementos que seguem o princípio FIFO (First In, First Out).

```ruby
# Criando uma fila
fila = []

# Adicionando elementos à fila
fila.push(1)
fila.push(2)
fila.push(3)
puts fila  # Saída: [1, 2, 3]

# Removendo elementos da fila
puts fila.shift  # Saída: 1
puts fila  # Saída: [2, 3]
```

---

Entender como trabalhar com arrays, hashes, conjuntos, pilhas e listas em Ruby é crucial para o desenvolvimento eficaz de programas. Nos próximos capítulos, exploraremos estruturas de repetições em Ruby.

<a href ="https://github.com/OsirisMariano/lab-natty-or-not/blob/main/ebook/estrutura_de_repeticao.md">
  <p align = "right">Próximo</p>
</a>
