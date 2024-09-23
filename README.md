# GRAMATICA_CALCULADORA_BISON
 *Manuel Cardenas
 *Juan Wilches
 *Bryan Ariza
 *Andres Toledo
 
Descripción: En este problema, se busca utilizar BISON, una herramienta para la generación de analizadores sintácticos, para implementar y ejecutar una calculadora que pueda realizar operaciones matemáticas básicas y manejar errores.
1. Precedencia con Gramática Normal -> +, - , * /
2. Precedencia con Gramática Inversa -> /, *, -, +
3. Dejar de menor precedencia los parentesis.

Instalacion de Bison en linux:

-Actualiza la lista de paquetes para hace eso necesitas Abrir tu terminal de linux y ejecutar:

         sudo apt update
         
-Luego de eso Instala Bison y Flex para eso usa el siguiente comando para instalarlo 

         sudo apt install bison
         sudo apt-get install bison flex
         
-Para asegurarte de que Bison se ha instalado correctamente puedes verificar su versión
                
        bison --version
        flex  --version

COMPILACION Y EJECUCION

Para compilar y ejecutar esta calculadora generada por bison debes seguir esta linea de pasos

-Generar el código C con Flex y Bison:

         flex calculadora.l
         bison -d calculadora.y

Esto genera lex.yy.c, calculadora.tab.c, y calculadora.tab.h.

-Luego compila el codigo C generado:

         gcc lex.yy.c calculadora.tab.c -o calculadora -lm
El flag -lm es necesario para vincular la biblioteca matemática estándar.

-Ejecutar la calculadora:
             ./calculadora 

Una vez que la calculadora esté en ejecución, puedes ingresar expresiones matemáticas. Por ejemplo, al introducir la cadena 9*9+9/3, la calculadora evaluará la expresión y mostrará el resultado.


