#Base64

### Yet another Base64 encoder / decoder!

This one is 
 + public domain, 
 + has a natural API
 + idiomatic scala, and 
 + need not add a dependancy to your project.  Just copy the [one source file](https://github.com/marklister/base64/blob/master/src/main/scala/Base64.scala) to your project!  It's around 33 lines of code.
 
#### Natural API

You simply invoke `toBase64` on an `Array[Byte]` or

`toByteArray` on a `String` containing a Base64 representation.

####Imports

`io.github.marklister.base64.Base64.Encoder`

`io.github.marklister.base64.Base64.Decoder`


####REPL example

```scala
[info] Starting scala interpreter...
[info] 
import io.github.marklister.base64.Base64._
Welcome to Scala version 2.10.2 (OpenJDK Server VM, Java 1.7.0_51).
Type in expressions to have them evaluated.
Type :help for more information.

scala> "ABCDEFG".getBytes.toBase64 //Encodes Array[Byte]=>String
res0: String = QUJDREVGRw==

scala> res0.toByteArray //Decodes base64 String=>Array[Byte]
res1: Array[Byte] = Array(65, 66, 67, 68, 69, 70, 71)

scala> res1.sameElements("ABCDEFG".getBytes)
res2: Boolean = true

```
