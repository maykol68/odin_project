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



