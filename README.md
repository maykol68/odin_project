# odin_project

## concantenation 

### With the plus operator:
```ruby
"Welcome " + "to " + "Odin!"    #=> "Welcome to Odin!"
```
### With the shovel operator:
```ruby
"Welcome " << "to " << "Odin!"  #=> "Welcome to Odin!"
```
### With the concat method:
```ruby
"Welcome ".concat("to ").concat("Odin!")  #=> "Welcome to Odin!"
```
## Substring

```ruby
"hello"[0]      #=> "h"

"hello"[0..1]   #=> "he"

"hello"[0, 4]   #=> "hell"

"hello"[-1]     #=> "o"
```
## Capitalize
```ruby
"hello".capitalize #=> "Hello"
```
## Include?
```ruby
"hello".include?("lo")  #=> true

"hello".include?("z")   #=> false
```

## Upcase
```ruby
"hello".upcase  #=> "HELLO"
```
## Downcase 
```ruby
"Hello".downcase  #=> "hello"
```
## empty 
```ruby
"hello".empty?  #=> false

"".empty?       #=> true
```
## Length
```ruby
"hello".length  #=> 5
```
## reverse 
```ruby
"hello".reverse  #=> "olleh"
```
## Split
```ruby
"hello world".split  #=> ["hello", "world"]

"hello".split("")    #=> ["h", "e", "l", "l", "o"]
```
## strip
```ruby
" hello, world   ".strip  #=> "hello, world"
```
__*Leerás más sobre estos métodos y otros en la tarea. Los ejemplos a continuación son solo para hacer fluir su creatividad con algunas de las increíbles formas en que puede modificar cadenas*__
```ruby
"he77o".sub("7", "l")           #=> "hel7o"

"he77o".gsub("7", "l")          #=> "hello"

"hello".insert(-1, " dude")     #=> "hello dude"

"hello world".delete("l")       #=> "heo word"

"!".prepend("hello, ", "world") #=> "hello, world!"
```
__*Converting other objects to strings*__
```ruby
5.to_s        #=> "5"

nil.to_s      #=> ""

:symbol.to_s  #=> "symbol"
```
## Create a symbol

_*Para crear un símbolo, coloque dos puntos al principio de algún texto:*_
```ruby
:my_symbol
```
## Symbols vs. strings
```ruby
string" == "string"  #=> true

"string".object_id == "string".object_id  #=> false

:symbol.object_id == :symbol.object_id    #=> true
```
## Case statements
_*Las declaraciones de caso son una manera clara de escribir varias expresiones condicionales que normalmente resultarían en una declaración if...elsif desordenada. Incluso puede asignar el valor de retorno de una declaración de caso a una variable para usarlo más adelante. Las declaraciones de caso procesan cada condición por turno y, si la condición devuelve falso, pasará a la siguiente hasta que se encuentre una coincidencia. Se puede proporcionar una cláusula else para que sirva como valor predeterminado si no se encuentra ninguna coincidencia.*_
 grade = 'F'

did_i_pass = case grade #=> create a variable `did_i_pass` and assign the result of a call to case with the variable grade passed in
```ruby
  when 'A' then "Hell yeah!"
  when 'D' then "Don't tell your mother."
  else "'YOU SHALL NOT PASS!' -Gandalf"
end


grade = 'F'

case grade
when 'A'
  puts "You're a genius"
  future_bank_account_balance = 5_000_000
when 'D'
  puts "Better luck next time"
  can_i_retire_soon = false
else
  puts "'YOU SHALL NOT PASS!' -Gandalf"
  fml = true
end
```
## Unless statements

_*Una declaración a menos que funcione de manera opuesta a una declaración if: solo procesa el código en el bloque si la expresión se evalúa como falsa. No hay mucho más*_

```ruby
age = 19
unless age < 18
  puts "Get a job."
end
```
_*Al igual que con las declaraciones if, puedes escribir una declaración a menos que en una línea y también puedes agregar una cláusula else.*_

```ruby
age = 19
puts "Welcome to a life of debt." unless age < 18

unless age < 18
  puts "Down with that sort of thing."
else
  puts "Careful now!"
end
```
## Ternary operator

_*El operador ternario es una declaración if...else de una línea que puede hacer que su código sea mucho más conciso. ¿Su sintaxis es declaración condicional? <ejecutar si es verdadero> : <ejecutar si es falso>. Puede asignar el valor de retorno de la expresión a una variable.*_

age = 19
response = age < 18 ? "You still have your entire life ahead of you." : "You're all grown up."
puts response #=> "You're all grown up."

_*Aquí, debido a que la expresión se evaluó como falsa, el código después de : se asignó a la variable respuesta. Escribir esto como una declaración if...else sería mucho más detallado:*_

## Loop

_*El bucle de bucle (digamos qué ????) es el bucle de Ruby que simplemente no lo dejará. Es un bucle infinito que continuará a menos que usted solicite específicamente que se detenga, usando el comando break. Lo más habitual es que break se utilice con una condición, como se ilustra en el siguiente ejemplo.*_

```ruby
i = 0
loop do
  puts "i is #{i}"
  i += 1
  break if i == 10
end
```
_*No verás que este bucle se use mucho en Ruby. Si utiliza un bucle, sepa que probablemente exista un bucle mejor para usted, como uno de los bucles más específicos a continuación. Mientras bucle*_

## While loop
_*Un bucle while es similar al bucle excepto que usted declara la condición que saldrá del bucle desde el principio.*_

```ruby
i = 0
while i < 10 do
 puts "i is #{i}"
 i += 1
end
```
_*Este es un ejemplo del uso de un bucle while con un conteo. Debido a que usted declara la condición que rompe el bucle desde el principio, la intención de su código es mucho más clara, lo que hace que este código sea más fácil de leer que nuestro bucle anterior._*

_*También puede utilizar bucles while para hacer repetidamente una pregunta al usuario hasta que dé la respuesta deseada:*_

```ruby
while gets.chomp != "yes" do
  puts "Are we there yet?"
end
```
_*Este ejemplo muestra la ventaja de flexibilidad de un bucle while: se ejecutará hasta que se cumpla su condición de interrupción, lo que podría ser para un número variable de bucles o un número de bucles inicialmente desconocido. ¿Quién sabe si has llegado a tu destino la primera, cuarta o septuagésima novena vez que lo preguntas?*_

## Until loop
_*El bucle Until es lo opuesto al bucle while. Un bucle while continúa mientras la condición sea verdadera, mientras que un bucle hasta continúa mientras la condición sea falsa. Por lo tanto, estos dos bucles se pueden utilizar de forma prácticamente intercambiable.*_

_*En última instancia, cuál sea su condición de interrupción determinará cuál es más legible. En la medida de lo posible, debes evitar negar tus expresiones lógicas usando ! (no). En primer lugar, puede resultar difícil notar el signo de exclamación en su código.*_ 

_*En segundo lugar, el uso de la negación hace que la lógica sea más difícil de razonar y, por lo tanto, hace que el código sea más difícil de entender. En estas situaciones es donde hasta brilla. Podemos reescribir nuestros ejemplos de bucle while usando Until.*_
```ruby
i = 0
until i >= 10 do
 puts "i is #{i}"
 i += 1
end
```
_*Puede ver aquí que usar hasta significa que el bucle continuará ejecutándose hasta que la condición i >= 10 sea verdadera*_

_*El siguiente ejemplo muestra cómo puedes usar hasta para evitar la negación. que el bucle while anterior tuvo que usar.*_

```ruby
until gets.chomp == "yes" do
  puts "Do you like Pizza?"
end
```

## Ranges

_*¿Qué pasa si sabemos exactamente cuántas veces queremos que se ejecute nuestro bucle? Ruby nos permite usar algo llamado rango para definir un intervalo. Todo lo que tenemos que hacer es darle a Ruby el valor inicial, el valor final y si queremos que el rango sea inclusivo o exclusivo.*_

```ruby
(1..5)      # inclusive range: 1, 2, 3, 4, 5
(1...5)     # exclusive range: 1, 2, 3, 4
```

## We can make ranges of letters, too!
```ruby
('a'..'d')  # a, b, c, d
```
### For loop
_*Un bucle for se utiliza para iterar a través de una colección de información, como una matriz o un rango. Estos bucles son útiles si necesita hacer algo un número determinado de veces y al mismo tiempo utilizar un iterador.*_
```ruby
for i in 0..5
  puts "#{i} zombies incoming!"
end
```

## Times loop
_*Si necesita ejecutar un bucle una cantidad específica de veces, no busque más que el confiable bucle #times. Funciona iterando a través de un bucle un número específico de veces e incluso ofrece la ventaja de acceder al número por el que se está iterando actualmente*_
```ruby
5.times do
  puts "Hello, world!"
end

5.times do |number|
  puts "Alternative fact number #{number}"
end
```
_*Recuerde, los bucles comenzarán a contar desde un índice cero a menos que se especifique lo contrario, por lo que la primera iteración del bucle generará el hecho alternativo número 0*_

## Upto and Downto loops

_*Los métodos Ruby #upto y #downto hacen exactamente lo que uno pensaría que hacen por sus nombres. Puede utilizar estos métodos para iterar desde un número inicial hasta otro número, respectivamente.*_
```ruby
5.upto(10) { |num| print "#{num} " }     #=> 5 6 7 8 9 10

10.downto(5) { |num| print "#{num} " }   #=> 10 9 8 7 6 5
```

## Creating arrays
_*Aquí hay dos matrices básicas:*_

```ruby
num_array = [1, 2, 3, 4, 5]
str_array = ["This", "is", "a", "small", "array"]
```

_*Ambas matrices tienen cinco elementos separados por comas. La primera matriz contiene números enteros, mientras que la segunda matriz contiene cadenas.*_


_*Las matrices se crean comúnmente con un literal de matriz, que es una sintaxis especial que se utiliza para crear instancias de un objeto de matriz. Para crear una nueva matriz usando un literal de matriz, use corchetes ([]).*_


_*También se puede crear una matriz llamando al método Array.new. Cuando llamas a este método, también puedes incluir hasta 2 argumentos opcionales (tamaño inicial y valor predeterminado):*_

```ruby
Array.new               #=> []
Array.new(3)            #=> [nil, nil, nil]
Array.new(3, 7)         #=> [7, 7, 7]
Array.new(3, true)      #=> [true, true, true]
```

## Accessing elements

_*Cada elemento de una matriz tiene un índice, que es una representación numérica de la posición del elemento en la matriz. Como la mayoría de los otros lenguajes de programación, las matrices Ruby utilizan indexación de base cero, lo que significa que el índice del primer elemento es 0, el índice del segundo elemento es 1, y así sucesivamente. El acceso a un elemento específico dentro de una matriz se realiza llamando a my_array[x], donde x es el índice del elemento que desea. Llamar a una posición no válida resultará en cero. Ruby también permite el uso de índices negativos, que devuelven elementos comenzando desde el final de una matriz, comenzando en [-1].*_

```ruby
str_array = ["This", "is", "a", "small", "array"]

str_array[0]            #=> "This"
str_array[1]            #=> "is"
str_array[4]            #=> "array"
str_array[-1]           #=> "array"
str_array[-2]           #=> "small"
```
_*Finalmente, Ruby proporciona los métodos de matriz #first y #last, que deberían explicarse por sí solos. Además, estos métodos pueden tomar un argumento entero, por ejemplo, my_array.first(n) o my_array.last(n), que devolverá una nueva matriz que contiene los primeros o últimos n elementos de my_array, respectivamente.*_

```ruby
str_array = ["This", "is", "a", "small", "array"]

str_array.first         #=> "This"
str_array.first(2)      #=> ["This", "is"]
str_array.last(2)       #=> ["small", "array"]
```
## Adding and removing elements
_*Agregar un elemento a una matriz existente se realiza utilizando el método #push o el operador pala <<. Ambos métodos agregarán elementos al final de una matriz y devolverán esa matriz con los nuevos elementos. El método #pop eliminará el elemento al final de una matriz y devolverá el elemento que se eliminó.*_

```ruby
num_array = [1, 2]

num_array.push(3, 4)      #=> [1, 2, 3, 4]
num_array << 5            #=> [1, 2, 3, 4, 5]
num_array.pop             #=> 5
num_array                 #=> [1, 2, 3, 4]
```

_*Los métodos #shift y #unshift se utilizan para agregar y eliminar elementos al comienzo de una matriz. El método #unshift agrega elementos al comienzo de una matriz y devuelve esa matriz (muy parecido a #push). El método #shift elimina el primer elemento de una matriz y devuelve ese elemento (muy parecido a #pop).*_

```ruby
num_array = [2, 3, 4]

num_array.unshift(1)      #=> [1, 2, 3, 4]
num_array.shift           #=> 1
num_array                 #=> [2, 3, 4]
```

_*También es útil saber que tanto #pop como #shift pueden tomar argumentos enteros:*_
```ruby
num_array = [1, 2, 3, 4, 5, 6]

num_array.pop(3)          #=> [4, 5, 6]
num_array.shift(2)        #=> [1, 2]
num_array                 #=> [3]
```

## Adding and subtracting arrays
_*¿Cuál crees que será el resultado de [1, 2, 3] + [3, 4, 5]?*_

_*Si adivinaste [1, 2, 3, 3, 4, 5], ¡felicidades! Agregar dos matrices devolverá una nueva matriz creada al concatenarlas, similar a la concatenación de cadenas. El método concat funciona de la misma manera.*_

```ruby
a = [1, 2, 3]
b = [3, 4, 5]

a + b         #=> [1, 2, 3, 3, 4, 5]
a.concat(b)   #=> [1, 2, 3, 3, 4, 5]
```
_*Para encontrar la diferencia entre dos matrices, puedes restarlas usando -. Este método devuelve una copia de la primera matriz, eliminando cualquier elemento que aparezca en la segunda matriz.*_
```ruby
[1, 1, 1, 2, 2, 3, 4] - [1, 4]  #=> [2, 2, 3]
```

## Basic methods
_*Ruby le brinda muchos métodos para manipular matrices y su contenido (¡más de 150!), muchos de los cuales están fuera del alcance de esta lección. Para conocer otros métodos, vaya a la documentación oficial (docs.ruby-lang.org) y explore la página Array, donde puede encontrar métodos enumerados alfabéticamente (desplazándose por la barra lateral izquierda) o resumidos y agrupados por propósito (leyendo en "Que hay aquí").*_

_*Llamar al método #methods en una matriz también generará una larga lista de métodos disponibles.*_

```ruby
num_array.methods       #=> A very long list of methods
```

_*A continuación se ofrece un breve vistazo a algunos otros métodos de matriz comunes con los que podría encontrarse:*_

```ruby
[].empty?               #=> true
[[]].empty?             #=> false
[1, 2].empty?           #=> false

[1, 2, 3].length        #=> 3

[1, 2, 3].reverse       #=> [3, 2, 1]

[1, 2, 3].include?(3)   #=> true
[1, 2, 3].include?("3") #=> false

[1, 2, 3].join          #=> "123"
[1, 2, 3].join("-")     #=> "1-2-3"
```

## Creating hashes
Let’s dive in and create a hash!

```ruby
my_hash = {
  "a random word" => "ahoy",
  "Dorothy's math test score" => 94,
  "an array" => [1, 2, 3],
  "an empty hash within a hash" => {}
}
```
_*Este ejemplo muestra la forma más básica de crear un hash, que consiste en utilizar el literal hash de llaves ({}). 
El hash anterior tiene cuatro claves que apuntan a cuatro valores diferentes. Por ejemplo, la primera clave, "una palabra aleatoria", apunta al valor "ahoy". 
Como puedes ver, los valores de un hash pueden ser un número, una cadena, una matriz o incluso otro hash. 

Las claves y los valores están asociados con un operador especial llamado hash rocket: =>. Al igual que con una matriz, también puedes crear un nuevo hash llamando al antiguo método ::new en la clase Hash.*_
```ruby
my_hash = Hash.new
my_hash               #=> {}
```

_*Por supuesto, los hashes no sólo toman cadenas como claves y valores. Ruby es un lenguaje bastante flexible, por lo que puedes insertar cualquier elemento antiguo y funcionará bien.*_

```ruby
hash = { 9 => "nine", :six => 6 }
```
### Accessing values
_*Puede acceder a los valores en un hash de la misma manera que accede a los elementos en una matriz. Cuando llamas al valor de un hash por clave, la clave va dentro de un par de corchetes, al igual que cuando llamas a una matriz por índice.*_
```ruby
shoes = {
  "summer" => "sandals",
  "winter" => "boots"
}

shoes["summer"]   #=> "sandals"
```

Si intenta acceder a una clave que no existe en el hash, devolverá cero:
```ruby
shoes["hiking"]   #=> nil
```

A veces, este comportamiento puede resultar problemático si devolver silenciosamente un valor nulo podría causar estragos en su programa. Afortunadamente, los hashes tienen un método de recuperación que generará un error cuando intentes acceder a una clave que no está en tu hash.

```ruby
shoes.fetch("hiking")   #=> KeyError: key not found: "hiking"
```

_*Alternativamente, este método puede devolver un valor predeterminado en lugar de generar un error si no se encuentra la clave proporcionada.*_

```ruby
shoes.fetch("hiking", "hiking boots") #=> "hiking boots"
```

## Adding and changing data
_*Puede agregar un par clave-valor a un hash llamando a la clave y estableciendo el valor, tal como lo haría con cualquier otra variable.*_

```ruby
shoes["fall"] = "sneakers"

shoes     #=> {"summer"=>"sandals", "winter"=>"boots", "fall"=>"sneakers"}
```

_*También puede utilizar este enfoque para cambiar el valor de una clave existente.*_

```ruby
shoes["summer"] = "flip-flops"
shoes     #=> {"summer"=>"flip-flops", "winter"=>"boots", "fall"=>"sneakers"}
```
## Removing data
_*La eliminación de datos de un hash se realiza con el método #delete del hash, que proporciona la interesante funcionalidad de devolver el valor del par clave-valor que se eliminó del hash*_
```ruby
shoes.delete("summer")    #=> "flip-flops"
shoes                     #=> {"winter"=>"boots", "fall"=>"sneakers"}
```

## Methods
_*Los hashes responden a muchos de los mismos métodos que las matrices, ya que ambos emplean el módulo Enumerable de Ruby. En la próxima lección, entraremos en muchos más detalles sobre el módulo Enumerable, incluidas las diferencias en cómo se comportan los métodos Enumerable para matrices y hashes.*_

_*Un par de métodos útiles que son específicos de los hashes son los métodos #keys y #values, que, como era de esperar, devuelven las claves y los valores de un hash, respectivamente. Tenga en cuenta que ambos métodos devuelven matrices.*_

```ruby
books = {
  "Infinite Jest" => "David Foster Wallace",
  "Into the Wild" => "Jon Krakauer"
}

books.keys      #=> ["Infinite Jest", "Into the Wild"]
books.values    #=> ["David Foster Wallace", "Jon Krakauer"]
``` 
## Merging two hashes
_*De vez en cuando, te encontrarás con una situación en la que dos hashes desean unirse en santa unión. Afortunadamente, existe un método para ello. (¡No se requiere ministro ordenado!)*_
```ruby
hash1 = { "a" => 100, "b" => 200 }
hash2 = { "b" => 254, "c" => 300 }
hash1.merge(hash2)      #=> { "a" => 100, "b" => 254, "c" => 300 }
```

_*Observe que los valores del hash que se fusionan (en este caso, los valores en hash2) sobrescriben los valores del hash que se fusionan en (hash1 aquí) cuando los dos hashes tienen una clave que es la misma.*_

## Symbols as hash keys
_*En esta lección, usamos principalmente cadenas para claves hash, pero en el mundo real, casi siempre verás símbolos (como :this_guy) usados ​​como claves. Esto se debe principalmente a que los símbolos tienen mucho más rendimiento que las cadenas en Ruby, pero también permiten una sintaxis mucho más limpia al definir hashes. He aquí la belleza:*_
```ruby
# 'Rocket' syntax
american_cars = {
  :chevrolet => "Corvette",
  :ford => "Mustang",
  :dodge => "Ram"
}
# 'Symbols' syntax
japanese_cars = {
  honda: "Accord",
  toyota: "Corolla",
  nissan: "Altima"
}
```
_*Ese último ejemplo hace que se te salten las lágrimas, ¿no? Observe que el cohete hash y los dos puntos que representan un símbolo se han combinado. Desafortunadamente, esto solo funciona para símbolos, así que no intentes { 9: "valor" } o obtendrás un error de sintaxis.*_

_*Cuando usas la sintaxis más limpia de "símbolos" para crear un hash, aún necesitarás usar la sintaxis de símbolo estándar cuando intentas acceder a un valor. En otras palabras, independientemente de cuál de las dos opciones de sintaxis anteriores utilice al crear un hash, ambas crean claves de símbolos a las que se accede de la misma manera.*_

```ruby
american_cars[:ford]    #=> "Mustang"
japanese_cars[:honda]   #=> "Accord"
```
