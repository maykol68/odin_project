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

## Symbols vs. strings

string" == "string"  #=> true

"string".object_id == "string".object_id  #=> false

:symbol.object_id == :symbol.object_id    #=> true





