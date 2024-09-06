**INTRODUCCIÓN A RPG IV**

## -Variables:

 *Numéricas*: Almacenan números enteros o decimales.
 
 Ejemplo:
 
  D   num1   S   5  0    // Número entero sin decimales
  
  D   num2   S   7  2    // Número decimal con 7 dígitos totales, 2 decimales

 *Texto*: Almacenan cadenas.
 
 Ejemplo:
 
  D   nombre   S   10A   // Cadena de 10 caracteres alfanuméricos

 *Lógicas*: Booleanas, verdadero o falso.
 
 Ejemplo:

  D   bandera   S   1N
   
## -Operaciones básicas:

 *Suma*:
 
 Ejemplo:

  C   EVAL   resultado = num1 + num2

 *Resta*:
 
 Ejemplo:

  C   EVAL   resultado = num1 - num2

 *Multiplicación*:
 
 Ejemplo:

  C   EVAL   resultado = num1 * num2

 *División*:
 
 Ejemplo:
 
  C   EVAL   resultado = num1 / num2

## -Control:

 *IF/ELSE:*
 
 Ejemplo:

 

  C   IF   num1 > 50
  
  C      EVAL   resultado = num1 * 2
  
  C   ENDIF

  

 *Bucle DOU:*
 
 Ejemplo:



  C   DOU   num1 > 100
  
  C     EVAL   num1 = num1 + 10
  
  C   ENDDO



## -Archivos:

 *CHAIN:* Leer registro por clave.
 
 Ejemplo:

  C   CHAIN   campoClave   nombreArchivo

## -Funciones:

 *%DEC():* Convierte a decimal.
 
 Ejemplo:

  resultado = %DEC(valor:10:2)

## -Ejemplo completo:

Este programa recibe dos números, los suma, y si el resultado es mayor que 100, lo limita a 100.


  D num1   S   5  0
  
  D num2   S   5  0
  
  C *ENTRY   PLIST
  
  C PARM   num1
  
  C PARM   num2
  
  C EVAL   resultado = num1 + num2
  
  C IF   resultado > 100
  
  C   EVAL   resultado = 100
  
  C ENDIF
  
  C RETURN

 



  

 

