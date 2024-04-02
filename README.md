# odin_project

## concantenation 

### With the plus operator:
"Welcome " + "to " + "Odin!"    #=> "Welcome to Odin!"

### With the shovel operator:
"Welcome " << "to " << "Odin!"  #=> "Welcome to Odin!"

### With the concat method:
"Welcome ".concat("to ").concat("Odin!")  #=> "Welcome to Odin!"

## Substring

"hello"[0]      #=> "h"

"hello"[0..1]   #=> "he"

"hello"[0, 4]   #=> "hell"

"hello"[-1]     #=> "o"

## Capitalize

"hello".capitalize #=> "Hello"

## Include?

"hello".include?("lo")  #=> true

"hello".include?("z")   #=> false

## Upcase
"hello".upcase  #=> "HELLO"

## Downcase 
"Hello".downcase  #=> "hello"

## empty 

"hello".empty?  #=> false

"".empty?       #=> true

## Length

"hello".length  #=> 5

## reverse 

"hello".reverse  #=> "olleh"

## Split

"hello world".split  #=> ["hello", "world"]

"hello".split("")    #=> ["h", "e", "l", "l", "o"]

## strip

" hello, world   ".strip  #=> "hello, world"

__*Leerás más sobre estos métodos y otros en la tarea. Los ejemplos a continuación son solo para hacer fluir su creatividad con algunas de las increíbles formas en que puede modificar cadenas*__

"he77o".sub("7", "l")           #=> "hel7o"

"he77o".gsub("7", "l")          #=> "hello"

"hello".insert(-1, " dude")     #=> "hello dude"

"hello world".delete("l")       #=> "heo word"

"!".prepend("hello, ", "world") #=> "hello, world!"

__*Converting other objects to strings*__

5.to_s        #=> "5"

nil.to_s      #=> ""

:symbol.to_s  #=> "symbol"

## Create a symbol

_*Para crear un símbolo, coloque dos puntos al principio de algún texto:*_

:my_symbol

## Symbols vs. strings

string" == "string"  #=> true

"string".object_id == "string".object_id  #=> false

:symbol.object_id == :symbol.object_id    #=> true

## Case statements
_*Las declaraciones de caso son una manera clara de escribir varias expresiones condicionales que normalmente resultarían en una declaración if...elsif desordenada. Incluso puede asignar el valor de retorno de una declaración de caso a una variable para usarlo más adelante. Las declaraciones de caso procesan cada condición por turno y, si la condición devuelve falso, pasará a la siguiente hasta que se encuentre una coincidencia. Se puede proporcionar una cláusula else para que sirva como valor predeterminado si no se encuentra ninguna coincidencia.*_
 grade = 'F'

did_i_pass = case grade #=> create a variable `did_i_pass` and assign the result of a call to case with the variable grade passed in
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

## Unless statements

_*Una declaración a menos que funcione de manera opuesta a una declaración if: solo procesa el código en el bloque si la expresión se evalúa como falsa. No hay mucho más*_

age = 19
unless age < 18
  puts "Get a job."
end

_*Al igual que con las declaraciones if, puedes escribir una declaración a menos que en una línea y también puedes agregar una cláusula else.*_

age = 19
puts "Welcome to a life of debt." unless age < 18

unless age < 18
  puts "Down with that sort of thing."
else
  puts "Careful now!"
end

## Ternary operator

_*El operador ternario es una declaración if...else de una línea que puede hacer que su código sea mucho más conciso. ¿Su sintaxis es declaración condicional? <ejecutar si es verdadero> : <ejecutar si es falso>. Puede asignar el valor de retorno de la expresión a una variable.*_

age = 19
response = age < 18 ? "You still have your entire life ahead of you." : "You're all grown up."
puts response #=> "You're all grown up."

_*Aquí, debido a que la expresión se evaluó como falsa, el código después de : se asignó a la variable respuesta. Escribir esto como una declaración if...else sería mucho más detallado:*_

## Loop

_*El bucle de bucle (digamos qué ????) es el bucle de Ruby que simplemente no lo dejará. Es un bucle infinito que continuará a menos que usted solicite específicamente que se detenga, usando el comando break. Lo más habitual es que break se utilice con una condición, como se ilustra en el siguiente ejemplo.*_

i = 0
loop do
  puts "i is #{i}"
  i += 1
  break if i == 10
end

_*No verás que este bucle se use mucho en Ruby. Si utiliza un bucle, sepa que probablemente exista un bucle mejor para usted, como uno de los bucles más específicos a continuación. Mientras bucle*_

## While loop
_*Un bucle while es similar al bucle excepto que usted declara la condición que saldrá del bucle desde el principio.*_

i = 0
while i < 10 do
 puts "i is #{i}"
 i += 1
end
_*Este es un ejemplo del uso de un bucle while con un conteo. Debido a que usted declara la condición que rompe el bucle desde el principio, la intención de su código es mucho más clara, lo que hace que este código sea más fácil de leer que nuestro bucle anterior._*

_*También puede utilizar bucles while para hacer repetidamente una pregunta al usuario hasta que dé la respuesta deseada:*_

while gets.chomp != "yes" do
  puts "Are we there yet?"
end

_*Este ejemplo muestra la ventaja de flexibilidad de un bucle while: se ejecutará hasta que se cumpla su condición de interrupción, lo que podría ser para un número variable de bucles o un número de bucles inicialmente desconocido. ¿Quién sabe si has llegado a tu destino la primera, cuarta o septuagésima novena vez que lo preguntas?*_

## Until loop
_*El bucle Until es lo opuesto al bucle while. Un bucle while continúa mientras la condición sea verdadera, mientras que un bucle hasta continúa mientras la condición sea falsa. Por lo tanto, estos dos bucles se pueden utilizar de forma prácticamente intercambiable.*_

_*En última instancia, cuál sea su condición de interrupción determinará cuál es más legible. En la medida de lo posible, debes evitar negar tus expresiones lógicas usando ! (no). En primer lugar, puede resultar difícil notar el signo de exclamación en su código.*_ 

_*En segundo lugar, el uso de la negación hace que la lógica sea más difícil de razonar y, por lo tanto, hace que el código sea más difícil de entender. En estas situaciones es donde hasta brilla. Podemos reescribir nuestros ejemplos de bucle while usando Until.*_

i = 0
until i >= 10 do
 puts "i is #{i}"
 i += 1
end

_*Puede ver aquí que usar hasta significa que el bucle continuará ejecutándose hasta que la condición i >= 10 sea verdadera*_

_*El siguiente ejemplo muestra cómo puedes usar hasta para evitar la negación. que el bucle while anterior tuvo que usar.*_


until gets.chomp == "yes" do
  puts "Do you like Pizza?"
end


## Ranges

_*¿Qué pasa si sabemos exactamente cuántas veces queremos que se ejecute nuestro bucle? Ruby nos permite usar algo llamado rango para definir un intervalo. Todo lo que tenemos que hacer es darle a Ruby el valor inicial, el valor final y si queremos que el rango sea inclusivo o exclusivo.*_

(1..5)      # inclusive range: 1, 2, 3, 4, 5
(1...5)     # exclusive range: 1, 2, 3, 4

## We can make ranges of letters, too!
('a'..'d')  # a, b, c, d
### For loop
_*Un bucle for se utiliza para iterar a través de una colección de información, como una matriz o un rango. Estos bucles son útiles si necesita hacer algo un número determinado de veces y al mismo tiempo utilizar un iterador.*_

for i in 0..5
  puts "#{i} zombies incoming!"
end


## Times loop
_*Si necesita ejecutar un bucle una cantidad específica de veces, no busque más que el confiable bucle #times. Funciona iterando a través de un bucle un número específico de veces e incluso ofrece la ventaja de acceder al número por el que se está iterando actualmente*_

5.times do
  puts "Hello, world!"
end

5.times do |number|
  puts "Alternative fact number #{number}"
end
_*Recuerde, los bucles comenzarán a contar desde un índice cero a menos que se especifique lo contrario, por lo que la primera iteración del bucle generará el hecho alternativo número 0*_

## Upto and Downto loops

_*Los métodos Ruby #upto y #downto hacen exactamente lo que uno pensaría que hacen por sus nombres. Puede utilizar estos métodos para iterar desde un número inicial hasta otro número, respectivamente.*_

5.upto(10) { |num| print "#{num} " }     #=> 5 6 7 8 9 10

10.downto(5) { |num| print "#{num} " }   #=> 10 9 8 7 6 5




