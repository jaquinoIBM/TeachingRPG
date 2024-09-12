**Tipos de Declaración de Variables Numéricas en RPG IV**
En RPG IV, las variables numéricas se declaran utilizando la instrucción dcl-s para declarar variables escalares o dcl-ds para estructuras de datos. A continuación, se describen los tipos de datos numéricos más comunes en RPG IV, junto con ejemplos prácticos.

## -ENTERO (Integer):

 *Descripción*: El tipo int se utiliza para almacenar números enteros. Un entero no tiene decimales y puede ser positivo o negativo. En RPG IV, puedes definir el tamaño de un entero con el número de dígitos totales que deseas reservar.

 *Diferencia con otros tipos*: Los enteros no manejan decimales, lo que los diferencia de los tipos decimales (packed y zoned). Son eficientes para operaciones que no requieren fracciones, como contadores o índices.
 

 Ejemplo 1:

  dcl-s miEnteroSigned1 int(5); // Entero de máx 5 dígitos

  miEnteroSigned1 = 123;  // Asignación de un valor positivo


 Ejemplo 2:

  dcl-s miEnteroSigned2 int(5); // Entero de máx 5 dígitos

  miEnteroSigned2 = -123;  // Asignación de un valor negativo



## -DECIMAL (Packed Decimal):

 *Descripción*: El tipo packed-decimal se usa para números con decimales empaquetados. Este formato utiliza menos espacio de almacenamiento que un zoned decimal y permite operaciones más rápidas en términos de cálculos numéricos precisos. Se declara como packed(n : d), donde n es el número total de dígitos y d es la cantidad de decimales.

 *Diferencia con otros tipos*: A diferencia de los enteros, el decimal empaquetado permite el almacenamiento de números con decimales. Se diferencia del zoned en que es más compacto en términos de uso de espacio, ya que empaqueta los dígitos en menos bytes.
 
 Ejemplo 1:

  dcl-s miDecimal1 packed(9 : 2); // Decimal empaquetado de máx 9 dígitos en total, 2 decimales

  miDecimal1 = 12345.67;  // Asignación de valor con 2 decimales


 Ejemplo 2:

  dcl-s miDecimal2 packed(7 : 3); // Decimal empaquetado de máx 7 dígitos en total, 3 decimales

  miDecimal2 = 789.123;   // Asignación de valor con 3 decimales


## -ZONED DECIMAL (Decimal Zonal):

 *Descripción:* El tipo zoned-decimal almacena números con decimales en un formato zonal. Esto significa que cada dígito está almacenado en un byte, con el último byte que contiene el signo. Se declara como zoned(n : d), donde n es el número total de dígitos y d es el número de decimales.

 *Diferencia con otros tipos*: En comparación con packed, el zoned es menos eficiente en el uso de espacio, pero puede ser más legible para ciertos tipos de sistemas. Es comúnmente utilizado cuando se necesita almacenar números para visualización en dispositivos externos.
 
 Ejemplo 1:

  dcl-s miZoned1 zoned(7 : 2); // Decimal zonal de 7 dígitos en total, 2 decimales

  miZoned1 = 543.21;  // Asignación de valor con 2 decimales


 Ejemplo 2:

  dcl-s miZoned2 zoned(9 : 3); // Decimal zonal de 9 dígitos en total, 3 decimales

  miZoned2 = 98765.432;  // Asignación de valor con 3 decimales


## -FLOAT (Número de Punto Flotante):

 *Descripción:* Los números de punto flotante (float) son útiles para almacenar números con decimales largos o con una amplitud muy grande, donde la precisión es menos importante que el rango. Este tipo de dato es adecuado para cálculos científicos o para manejar números extremadamente grandes o pequeños.

 *Diferencia con otros tipos*: A diferencia de packed o zoned, el tipo float utiliza una representación de punto flotante para los decimales, lo que permite almacenar números muy grandes o pequeños pero con una precisión limitada.
 
 Ejemplo 1:

  dcl-s miFloat1 float(8); // Número de punto flotante de 8 bytes

  miFloat1 = 12345.6789;  // Asignación de valor a un número flotante


 Ejemplo 2:

  dcl-s miFloat2 float(4); // Número de punto flotante de 4 bytes

  miFloat2 = 9876.5432;  // Asignación de valor a un número flotante más pequeño


## -BINARY (Binario):

 *Descripción:* Los enteros binarios (binary) almacenan enteros en formato binario, que puede ser unsigned (sin signo) o signed (con signo). Estos números son ideales para manejar grandes volúmenes de datos numéricos que no requieren decimales y donde el uso eficiente de memoria es importante.

 *Diferencia con otros tipos*: Los números binarios son más eficientes en el uso de memoria que los enteros normales, y pueden almacenar valores más grandes con menos bytes. Sin embargo, no permiten manejar decimales como los tipos packed o zoned.
 
 Ejemplo 1:

  dcl-s miBinario1 unsigned(5); // Entero binario sin signo de 5 dígitos

  miBinario1 = 25000;  // Asignación de valor a un entero binario sin signo

 Ejemplo 2:

  dcl-s miBinario2 signed(3); // Entero binario con signo de 3 dígitos

  miBinario2 = -150;  // Asignación de valor a un entero binario con signo
