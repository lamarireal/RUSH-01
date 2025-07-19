Hola, aquí están todas las cosas necesarias para preparar y comenzar el rush01:

    Antes que nada, hay que entender cómo se juega al juego “Skyscrapers”. Puedes encontrarlo aquí:
    👉 https://www.puzzle-skyscrapers.com

    La lógica que he creado es bastante simple para poder terminar la tarea, y luego hacer los “extras” sin problemas ni dolores de cabeza 😄.
    Ahora voy a explicar mi lógica.
    (Para mí, pensar en cómo hacer este proyecto fue divertido. Por eso, si quieres, puedes intentar imaginar tu propia versión de cómo hacerlo antes de leer la mía. Tal vez tu idea sea mejor y más simple 😊)

Explicación de la lógica:

a. Main: Solo sirve para ejecutar el código principal y recoger los números del usuario.

b. El usuario debe introducir 16 números, por eso vamos a crear 4 arrays, uno para cada lado del tablero.

c. map_variation: Esta función genera todas las posibles variaciones del tablero 4x4.
(Sí, podríamos escribirlas todas a mano, pero en el caso de 4x4 hay 576 tableros únicos, así que no creo que sea una buena idea escribirlos uno por uno jajajajaja 😅)

d. left_side: Toma el array de ese lado (izquierdo) y todas las variaciones del tablero, y busca cuáles cumplen con los números de ese lado.

e. right_side: Toma el array del lado derecho y las variaciones filtradas por left_side.

f. top_side: Hace lo mismo con el array superior y las variaciones filtradas por right_side.

g. bottom_side: Igual que los anteriores, pero con el lado inferior y las variaciones que quedan después de top_side.

h. En cada función, hay que añadir una condición (if) para comprobar si todavía quedan variaciones posibles.
Si ya no hay ninguna, hay que mostrar un mensaje de error.

i. Al final, se debe imprimir el tablero con la única variación válida.

El código va a ser bastante fácil de entender y también fiable, ya que comprobamos todas las combinaciones posibles.
Claro, este enfoque también tiene una desventaja, y es la velocidad: la máquina primero tiene que generar todas las combinaciones y luego revisar cada una.
Pero al menos todo es simple y claro 😊
