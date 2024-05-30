# <h1 align = "Center">**Estruturas de Seleção**</h1>

Neste capítulo, exploraremos como utilizar estruturas de seleção em Ruby para tomar decisões com base em condições específicas. As estruturas de seleção permitem que o seu programa escolha diferentes caminhos de execução com base nas condições fornecidas.

#### *Declaração if*

As declarações `if`, `elsif`, `else` permite que você execute um bloco de código apenas se uma condição específica for verdadeira.

```ruby
idade = 18

if idade < 18
  puts "Menor de idade"
elsif idade == 18
  puts "Acabou de se tornar adulto"
else
  puts "Maior de idade"
end
```

#### *Declaração unless*

A estrutura `unless` é o inverso do `if`. Ela executa o bloco de código se a condição for falsa

```ruby
idade = 20

unless idade < 18
  puts "Maior de idade"
else
  puts "Menor de idade"
end
```

#### *Declaração case / when*

A estrutura `case` é usada para testar uma variável ou expressão contra uma série de valores diferentes.

```ruby
nota = 'B'

case nota
when 'A'
  puts "Excelente!"
when 'B'
  puts "Bom trabalho!"
when 'C'
  puts "Pode melhorar!"
else
  puts "Nota não reconhecida"
end
```

### **Modigicadores condicionais**
Em Ruby, você pode usar modificadores condicionais para tornar o código mais conciso. Eles permitem que você coloque a condição no final da instrução.

```ruby
# Usando `if` como modificador condicional
puts "Maior de idade" if idade >= 18

# Usando `unless` como modificador condicional
puts "Menor de idade" unless idade >= 18
```

### **Operador ternário**
O operador ternário é uma forma compacta de escrever uma declaração `if-else`.

```ruby
idade = 20
mensagem = idade >= 18 ? "Maior de idade" : "Menor de idade"
puts mensagem
```

---

Essas estruturas são fundamentais para tomar decisões dentro do seu código e são amplamente usadas em todos os tipos de programas Ruby.
Nos próximos capítulos, exploraremos estruturas de repetição e funções em Ruby.

<a href = "">
  <p align = "right">Próximo</p>
</a>