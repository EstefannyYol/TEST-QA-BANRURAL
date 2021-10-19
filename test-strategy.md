Identificación de errores y correción de los mismos 
linea 41 se detecto que el cierre del body se encuentra en la linea 41 lo cual causa un error a la hora de la ejecución del código
la correción de este error se encuentra en la linea 118 donde se establecio el cierre del body. 

linea 44 let randomNumber = Math.random() * 10; 
en este error de linea se detecto que el evento random se encuentra incompleto, le falta el math floor y la indicación que los números deben ser del 1 al 100.
Solución let randomNumber = Math.floor(Math.random() * 100)+1;

linea 46 const ATTEMPS = 5;
Acá nos indica que los turnos seran 5 pero lo requerido son 10 
Solución const ATTEMPS = 10;

linea 55 esta linea se encuentra vacia se establecion que aca debe ir el boton con su escuchardor de eventos click y realizar la llamada de la función que hara todas las comparaciones
guessSubmit.addeventListener('click', checkGuess);

linea 58 let userGuess = guessField.value;
se identifico que el valor del campo no se convirtio a número, aunque el código javascript es no tipado y puede que no sea necesario indicar el tipo de dato
Solución let userGuess = number(guessField.value);

linea 66     if(userGuess === randomNumber) {
              lastResult.textContent = '!!!Pérdistes!!!';
              lastResult.style.backgroundColor = 'black';
Se logra observar que este if identifica cuando el nuemro es ganador pero el texto indica que perdio, el color que lo identifica también es erroneo 
Solución     if(userGuess === randomNumber) {
              lastResult.textContent = 'Felicitaciones! adivinaste el número!';
              lastResult.style.backgroundColor = 'green';
  
linea 70     } else if(guessCount === ATTEMPS) {
              lastResult.textContent = 'Felicitaciones! adivinaste el número!';
              lastResult.style.backgroundColor = 'red';
Se observo que este else if identifica cuando el jugador completa sus 10 intentos y si perdio pero el texto a mostrar inidca que gano
Solución     } else if(guessCount === ATTEMPS) {
              lastResult.textContent = '!!!Pérdistes!!!';
              lastResult.style.backgroundColor = 'red';
              
Linea 72 se encuentra vacia pero hace falta indicar que el mensaje de si es mayor o menor este en blanco. 
solución lowOrHi.textContent = '';

Linea 78       if(userGuess < randomNumber) {
                lowOrHi.textContent = 'El número es mayor!';
el error detectado es que el if indica que el nuemro es menor (<) pero en la linea 78 del código en el texto a mostrar indica que es mayor. 
solucción lowOrHi.textContent = 'El número es menor!';

Linea 80       } else if(userGuess > randomNumber) {
                lowOrHi.textContent = 'El número es menor!';
en el else if nos indica que el numero a identificar es mayor pero el texto que muestra en la linea 80 no dice que es menor. 
solución lowOrHi.textContent = 'El número es mayor!';

linea 115 randomNumber = Math.floor(Math.random()) + 1;
el error presentado muestra que no esta indicando cuantos son los numeros para el evento random 
solución randomNumber = Math.floor(Math.random()*100) + 1;

linea 118 aca se cierra el body 
