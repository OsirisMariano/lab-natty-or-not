# <h1 align = "Center">**Programação Orientada a Objetos**</h1>

A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o software em "objetos", cada um encapsulando dados e comportamentos relacionados. Em Ruby, tudo é um objeto, o que torna o uso deste paradigma natural e intuitivo. Vamos explorar os principais conceitos da POO em Ruby, incluindo classes, objetos, herança, encapsulamento, polimorfismo e mixins.

#### *Classes e Objetos*

Uma classe é um modelo que define atributos e métodos comuns para os objetos que pertencem a essa classe. Um objeto é uma instância de uma classe.

```ruby
class Pessoa
  attr_accessor :nome, :idade

  def initialize(nome, idade)
    @nome = nome
    @idade = idade
  end

  def saudar
    puts "Olá, meu nome é #{@nome} e eu tenho #{@idade} anos."
  end
end

# Criando um objeto da classe Pessoa
pessoa1 = Pessoa.new("Alice", 30)
pessoa1.saudar  # Saída: Olá, meu nome é Alice e eu tenho 30 anos.
```

#### *Herança*

Herança é um mecanismo pelo qual uma classe (subclasse) pode herdar atributos e métodos de outra classe (superclasse).

```ruby
class Pessoa
  attr_accessor :nome, :idade

  def initialize(nome, idade)
    @nome = nome
    @idade = idade
  end

  def saudar
    puts "Olá, meu nome é #{@nome} e eu tenho #{@idade} anos."
  end
end

class Funcionario < Pessoa
  attr_accessor :cargo

  def initialize(nome, idade, cargo)
    super(nome, idade)  # Chama o método initialize da superclasse
    @cargo = cargo
  end

  def detalhes_funcionario
    puts "Cargo: #{@cargo}"
  end
end

# Criando um objeto da classe Funcionario
funcionario1 = Funcionario.new("Bob", 45, "Gerente")
funcionario1.saudar            # Saída: Olá, meu nome é Bob e eu tenho 45 anos.
funcionario1.detalhes_funcionario  # Saída: Cargo: Gerente
```

#### *Encapsulamento*

Encapsulamento é o conceito de restringir o acesso a certos detalhes de um objeto, expondo apenas o necessário através de métodos públicos.

```ruby
class ContaBancaria
  def initialize(saldo)
    @saldo = saldo
  end

  def depositar(valor)
    @saldo += valor
  end

  def sacar(valor)
    @saldo -= valor if valor <= @saldo
  end

  def mostrar_saldo
    puts "Saldo: #{@saldo}"
  end

  private

  def ajustar_saldo(valor)
    @saldo += valor
  end
end

# Criando um objeto da classe ContaBancaria
conta = ContaBancaria.new(1000)
conta.depositar(500)
conta.sacar(300)
conta.mostrar_saldo  # Saída: Saldo: 1200
# conta.ajustar_saldo(100)  # Isso gerará um erro: NoMethodError
```

#### *Polimorfismo*

Polimorfismo permite que métodos com o mesmo nome em classes diferentes possam ter comportamentos diferentes. Em Ruby, isso é frequentemente conseguido através de herança e implementação de métodos em classes derivadas.

```ruby
class Animal
  def fazer_som
    puts "Som do animal"
  end
end

class Cachorro < Animal
  def fazer_som
    puts "Latido"
  end
end

class Gato < Animal
  def fazer_som
    puts "Miau"
  end
end

animais = [Cachorro.new, Gato.new]

animais.each do |animal|
  animal.fazer_som
end

# Saída:
# Latido
# Miau
```

### *Mixins (Módulos)*
Mixins são módulos que podem ser incluídos em classes para adicionar funcionalidade sem usar herança. Eles são uma forma poderosa de reutilização de código em Ruby.

```ruby
module Caminhavel
  def caminhar
    puts "Estou caminhando."
  end
end

class Pessoa
  include Caminhavel
end

class Cachorro
  include Caminhavel
end

pessoa = Pessoa.new
pessoa.caminhar  # Saída: Estou caminhando.

cachorro = Cachorro.new
cachorro.caminhar  # Saída: Estou caminhando.
```

Em Python, as classes são definidas usando a palavra-chave `class`, seguida pelo nome da classe.

```python
class Pessoa:
    def __init__(self, nome, idade):
        self.nome = nome
        self.idade = idade

    def saudacao(self):
        print("Olá, meu nome é", self.nome, "e tenho", self.idade, "anos.")
```
---

A Programação Orientada a Objetos em Ruby oferece um conjunto poderoso e intuitivo de ferramentas para organizar e reutilizar código. Ruby suporta múltiplos paradigmas de programação, permitindo aos desenvolvedores escolher o estilo que melhor se adapta ao problema em questão. Com classes, herança, encapsulamento, polimorfismo e mixins, Ruby torna a POO acessível e eficiente, ao mesmo tempo em que permite a incorporação de técnicas de programação funcional e procedural.

<a href = "">
  <p align = "right">Próximo</p>
</a>