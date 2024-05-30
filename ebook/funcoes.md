# <h1 align = "Center">**Funções**</h1>

Funções em Ruby (chamadas de métodos) são blocos de código que podem ser definidos uma vez e chamados várias vezes em diferentes partes de um programa.

### **Definindo Métodos**

Para definir um método em Ruby, usamos a palavra-chave `def`, seguida pelo nome do método e um bloco de código que o método executará. A definição do método é encerrada com a palavra-chave `end`.

```ruby
def saudacao
  puts "Olá, mundo!"
end

```

### **Chamand Métodos**

Para chamar um método, simplesmente usamos o nome do método seguido por parênteses (os parênteses são opcionais se não houver argumentos).

```ruby
saudacao  # Saída: Olá, mundo!
```

### **Métodos com Argumentos**

Métodos podem aceitar argumentos, que são valores passados para o método para serem usados dentro do seu bloco de código.

```ruby
def saudacao(nome)
  puts "Olá, #{nome}!"
end

saudacao("Alice")  # Saída: Olá, Alice!
```

### **Valores de Retorno**

Por padrão, métodos em Ruby retornam o valor da última expressão avaliada. Você pode usar a palavra-chave `return` para retornar explicitamente um valor e terminar a execução do método.

```ruby
def soma(a, b)
  return a + b
end

resultado = soma(2, 3)
puts resultado  # Saída: 5
```

### **Valores Padrão para Argumentos**

Você pode definir valores padrão para argumentos. Se nenhum valor for fornecido ao chamar o método, o valor padrão será usado.

```ruby
def saudacao(nome = "Mundo")
  puts "Olá, #{nome}!"
end

saudacao         # Saída: Olá, Mundo!
saudacao("Alice")  # Saída: Olá, Alice!

```

### **Argumentos com Nome (Named Arguments**

Ruby suporta argumentos com nome, que podem tornar a chamada de métodos mais clara e flexível.

```ruby
def criar_usuario(nome:, idade:, cidade:)
  puts "Nome: #{nome}, Idade: #{idade}, Cidade: #{cidade}"
end

criar_usuario(nome: "Alice", idade: 30, cidade: "São Paulo")
```

## **Argumentos Variáveis**

Você pode usar um argumento de array (*args) para capturar um número variável de argumentos.

```ruby
def soma(*numeros)
  numeros.reduce(0) { |soma, numero| soma + numero }
end

puts soma(1, 2, 3, 4, 5)  # Saída: 15
```

## **Blocos**
Métodos em Ruby podem receber blocos, que são pedaços de código que podem ser passados para métodos e executados dentro deles.

```ruby
def executar_bloco
  puts "Antes do bloco"
  yield  # Executa o bloco passado para o método
  puts "Depois do bloco"
end

executar_bloco { puts "Dentro do bloco" }
# Saída:
# Antes do bloco
# Dentro do bloco
# Depois do bloco
```

### **Métodos com Blocos Explícitos**
Você pode usar parâmetros &block para capturar blocos passados para o método e chamá-los explicitamente com block.call.

```ruby
def executar_bloco_explicitamente(&block)
  puts "Antes do bloco"
  block.call if block_given?
  puts "Depois do bloco"
end

executar_bloco_explicitamente { puts "Dentro do bloco" }
# Saída:
# Antes do bloco
# Dentro do bloco
# Depois do bloco
```
### **Métodos Privados e Públicos**
Os métodos em Ruby podem ser definidos como públicos ou privados dentro de uma classe. Métodos públicos são acessíveis de fora da classe, enquanto métodos privados só podem ser chamados de dentro da própria classe.

```ruby
class Pessoa
  def initialize(nome, idade)
    @nome = nome
    @idade = idade
  end

  def mostrar_informacoes
    puts "Nome: #{@nome}, Idade: #{@idade}"
  end

  private

  def metodo_privado
    puts "Este é um método privado"
  end
end

pessoa = Pessoa.new("Alice", 30)
pessoa.mostrar_informacoes  # Saída: Nome: Alice, Idade: 30
# pessoa.metodo_privado  # Isso gerará um erro: NoMethodError
```

---

Essas são apenas algumas das principais funções integradas em Ruby que são amplamente utilizadas em muitos programas. Ao longo de sua jornada em Ruby, você encontrará e aprenderá a usar muitas dessas funções para realizar uma variedade de tarefas.

<a href = "">
  <p align = "right">Próximo</p>
</a>