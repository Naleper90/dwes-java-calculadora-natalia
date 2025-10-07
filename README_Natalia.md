# Calculadora DWES – Reto: Añadir `tan(x)`

## 📘 Descripción del reto
Este reto consistía en ampliar la calculadora del proyecto añadiendo un reto elegido por un compañero (la función trigonométrica **`tan(x)`**, siguiendo el mismo esquema que `sin(x)` y `cos(x)`).  
Parece una modificación sencilla pero me ha servido para entender cómo se organiza el programa por capas: Lexer → Parser → Evaluator.

---

##  Cambios realizados

### En el **Evaluator**
Dentro del bloque `switch` donde se evalúan las funciones matemáticas, añadí un nuevo caso para la tangente:



Con este cambio, la calculadora ya reconoce tan(x) y devuelve el valor correcto usando Math.tan() de Java.

No fue necesario modificar el Lexer ni el Parser, ya que ambos reconocen cualquier palabra (como tan) como identificador.

### En el **Main**
Actualicé el texto de ayuda (HELP) para que aparezca la nueva función entre las opciones disponibles:


## Por qué elegí este reto
Elegí esta mejora porque parecía simple, pero me obligaba a comprender bien la estructura interna del código.
El ejercicio me ayudó a identificar en qué parte realmente se realiza el cálculo (Evaluator) y qué partes solo preparan la expresión (Lexer y Parser).

Aunque el cambio sea solo una línea de código, detrás hay varios conceptos importantes:

- Entender que el Lexer no necesita cambios porque ya reconoce la palabra “tan”.

- Saber que las funciones trigonométricas de Java trabajan en radianes, no en grados.

- Modificar correctamente el HELP del Main para mostrar la nueva función al usuario.

- Probar la expresión en consola para verificar que devuelve los resultados esperados.

Por eso, aunque el cambio de código es corto, la comprensión detrás no lo es.

## Conclusión
Aunque la modificación fue pequeña, me permitió entender cómo se amplía una aplicación Java modular y cómo interactúan sus componentes internos.
Ahora la calculadora muestra correctamente la nueva función tan(x) tanto en los cálculos como en el texto de ayuda.

Autora: Natalia
Asignatura: Desarrollo Web en Entorno Servidor
