# <h1 align = "Center">**Estruturas de Repetição**</h1>

Neste capítulo, vamos explorar as estruturas de repetição em RUby, que permitem executar um bloco de código repetidamente até que uma condição específica seja atendida ou até que todos os itens em uma coleção tenham sido processados.

### **`while`**

A estrutura `while` executa um bloco de código repetidamente enquanto a condição for verdadeira.

```ruby
contador = 0

while contador < 5
  puts "Contador é #{contador}"
  contador += 1
end

```

### **`until`**

A estrutura `until` é o inverso do while. Ela executa o bloco de código repetidamente até que a condição seja verdadeira.

```ruby
contador = 0

until contador == 5
  puts "Contador é #{contador}"
  contador += 1
end
```

### **for**

A estrutura `for` itera sobre uma faixa ou uma coleção. Ela é menos comum em Ruby devido ao uso mais prevalente de iteradores como `each`.

```ruby
for i in 0..4
  puts "i é #{i}"
end
```

### **Iteradores (each, times, map, etc.)**

Ruby oferece vários métodos de iteração que são usados com mais frequência do que `for` ou `while`.

`each`
O método `each` é usado para iterar sobre elementos de uma coleção (como um `array` ou um `hash`).

```ruby
# Usando `each` com um array
[1, 2, 3, 4, 5].each do |numero|
  puts "Número é #{numero}"
end

# Usando `each` com um hash
{nome: "Alice", idade: 30}.each do |chave, valor|
  puts "#{chave}: #{valor}"
end

```

### **times**
O método `times` executa um bloco de código um número específico de vezes.

```ruby
5.times do |i|
  puts "Iteração número #{i}"
end
```

### **map**
O método map cria um novo array contendo os resultados do bloco de código aplicado a cada elemento da coleção original.

```ruby
numeros = [1, 2, 3, 4, 5]
quadrados = numeros.map { |numero| numero ** 2 }
puts quadrados  # Saída: [1, 4, 9, 16, 25]

```
### **Loop infinito com loop**
O método loop cria um loop infinito. Você pode usar break para sair do loop.

```ruby
contador = 0

loop do
  puts "Contador é #{contador}"
  contador += 1
  break if contador >= 5
end
```
---

Essas estruturas são fundamentais para executar operações repetitivas de maneira eficiente e flexível em Ruby. Nos próximos capítulos, exploraremos funções e orientada a objetos em Ruby.

<a href = "">
  <p align = "right">Próximo</p>
</a>