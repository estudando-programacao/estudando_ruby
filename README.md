# estudando_ruby

iniciando estudos em ruby apos rubyconf 2016

- quase tudo que é declarado em ruby pode ser tratado como um objeto.
- podemos utilizar o IRB para testar códigos simples em ruby, basta difitar `irb` no terminal, e o CLI é iniciado.

## variáveis

- no ruby não precisamos dizer qual o tipo de variável que estamos declarando, apenas declaramos o valor da variável.
- as variáveis podem ser declaradas tanto dentro quanto fora do escopo dos métodoss.
- podemos utilizar variáveis globais.
- variáveis são declaradas no padrão snake_case e não camelCase
- voce pode declarar uma variável como nil, que significa que ela é uma variável especial sem valor definido
```
ruby_var = "primeira variável em ruby"

# variavel com valor nil
ruby_var_dois = nil
```
para verificar o tipo do valor da variável podemos utilizar o comando `var.class` que retorna qual o tipo de dado presente naquela variável, neste caso uma string.

exemplo de variável global

```
# uma variável global "ignora" o escopo de variáveis e fica disponível em todo o escopo do arquivo, como se fosse uma constante
$var_global = "primeira variavel global com ruby"
```

## métodos

definindo métodos

- a palavra def define que vamos declarar um método.
- um método retorna sempre o valor da ultima expressão.

métodos em linha

```
def double(val); val * 2; end
```
métodos indentado

```
def double(val)
    val * 2
end
```

utilizando o método que definimos

```
# conforme a declaração do método, com parametros, apenas chamamos o metódo passando um valor.
double(123)
double("abc")
```

escopo de variáveis - no ruby também existe o escopo de variáveis em uma função. por exemplo, ao declarar uma variável fora do método, esta não é alterada mesmo que seja declarada a mesma variável dentro do método.

```
# declarando variável fora do escopo
var_um = 10

# declarando método
def test()
    # declarando mesma variável dentro do método
    var_um = 5
    # utilizamos o puts (printa e pula uma linha) para printar o valor da var_um dentro do escopo
    puts var_um
# finalizamos o método
end

# chamamos o método
test

# printamos o valor de var_um fora do escopo
puts var_um
```

note que no exemplo acima é printado o valor da variável dentro e fora do escopo, ambas com os valores diferentes.


## condições

condição if-else

operadores de comparação: > | < | >= | <= | == | !=
operadores lógicos: ! (not) | && (and) | || (or)

```
# declaramos a variável
var_um = 10

# criamos uma variável chamada message e nela geramos a verificaçã da condição
message = if var_um > 1
    # se sim
    "primeira condição verdadeira em ruby."
else
    # se não
    "primeira condição falsa."
end

# printamos a variavel message com o resultado da condição
puts message
```

