# Clase 3

### Ejercicios

**1 -** Diseña un programa que nos confirme si un [año es bisiesto](https://es.wikipedia.org/wiki/A%C3%B1o_bisiesto) o no.
- Caracteristicas de un año bisiesto:
	- Tiene que ser divisible entre 4 y no tiene que ser divisible entre 100
	- O puede ser divisble entre 100 y entre 400
```
	Proceso esBisiesto
		
		Escribir "Dime el Año:"
		Leer year
		
		Si year % 4 = 0 & year % 100 <> 0 Entonces
			Escribir "Amigo, el año " year " es bisiesto!"
		Sino
			Si year % 400 = 0 & year % 100 = 0 Entonces
				Escribir "Amigo, el año " year " es bisiesto!"
			Sino
				Escribir "Amigo, el año " year " NO es bisiesto!"
			Fin Si
		Fin Si
		
	FinProceso
```

**2 -** Diseña un programa que imprima los numeros del 1 al 100.
```
	Proceso contadorPositivo
		
		controlador = 1
		
		Escribir "Empieza la cuenta!"
		
		Mientras controlador <= 100 Hacer
			Escribir controlador
			controlador = controlador +1
		Fin Mientras
		
		Escribir "Terminó la cuenta mágica..."
		
	FinProceso
```

**3 -** Diseña un programa que imprima los numeros del 100 al 0.
```
	Proceso contadorNegativo
		
		controlador = 100
		
		Escribir "Empieza la cuenta!"
		
		Mientras controlador >= 0 Hacer
			Escribir controlador
			controlador = controlador -1
		Fin Mientras
		
		Escribir "Terminó la cuenta mágica..."
		
	FinProceso
```

**4 -** Diseña un programa que imprima los numeros pares entre 0 y 100.
```
	Proceso contadorPares
		
		controlador = 2
		
		Escribir "Empieza la cuenta!"
		
		Mientras controlador <= 100 Hacer
			Escribir controlador
			controlador = controlador +2
		Fin Mientras
		
		Escribir "Terminó la cuenta mágica..."
		
	FinProceso 
```

**5 -** Diseña un programa que imprima los números impares entre un número dado por el usuario y los siguientes 50 números.
```
	Proceso contador50Impares
		Escribir "Dame un número:"
		Leer numero
		
		controlador = 1
		
		Escribir "Empieza la cuenta!"
		
		Mientras controlador <= 50 Hacer
			
			Si numero % 2 = 0 Entonces
				numero <- numero + 1
				controlador <- controlador + 1
			Sino
				Escribir numero
				controlador <- controlador + 1
				numero <- numero + 1
			Fin Si
			
		Fin Mientras
		
		Escribir "Terminó la cuenta mágica..."
		
	FinProceso
```

**6 -** Diseña un programa que imprima la suma de los 50 primeros numeros pares y el total de números impares partiendo de un número dado por el usuario
```
 	Proceso contadorEspecial
 		Escribir "Dame un número:"
 		Leer numero
 		
 		controlador = 1
 		Totalimpares = 0
 		totalImpares = 0
 		
 		Escribir "Empieza la cuenta!"
 		
 		Mientras controlador <= 50 Hacer
 			
 			Si numero % 2 = 0 Entonces
 				controlador <- controlador + 1
 				totalPares<- totalPares + numero
 				numero <- numero + 1
 			Sino
 				totalImpares<- totalImpares + 1
 				numero <- numero + 1
 			Fin Si
 			
 		Fin Mientras
 		
 		Escribir "Total de suma de pares ", totalPares
 		Escribir "Total de impares ", totalImpares
 		Escribir "Terminó la cuenta mágica..."
 		
 	FinProceso
```


**7 -** Diseña un programa que cuente las veces que aparece una determinada letra en una frase que introduciremos por teclado.
```
	Proceso cuantasVeces
		Escribir "Dame una letra:"
		Leer letra
		
		Escribir "Dame un texto:"
		Leer texto
		
		controlador <- 0
		longitudTexto <- Longitud(texto)
		totalVeces <- 0
		
		Mientras controlador <= longitudTexto Hacer
			letraActual <- SubCadena(texto,controlador,controlador)
			controlador <- controlador + 1
			
			// Escribir "letra actual .... " letraActual
			Si letraActual = letra Entonces
				totalVeces = totalVeces +1
			Fin Si
			
		Fin Mientras
		
		Escribir letra "se ha repetido un total de " totalVeces
	FinProceso
```

**8 -** Diseña un programa que simula el lanzamiento de una moneda al aire e imprimir si ha salido cara o cruz.
```
	Proceso azarMoneda
		valor <- azar(2)
		
		Si valor = 1 Entonces
			Escribir "Salio Cara!"
		Sino
			Escribir "Salio Cruz!"
		Fin Si
		
	FinProceso
```

**9 -** Diseña un programa que  simula cien tiradas de dos dados y contar las veces que entre los dos suman 10.
```
	Proceso azarMoneda
	
		coincidencias <- 0
		controlador <- 0
		
		Mientras controlador <= 100 Hacer
			
			dado1 <- azar(7)
			dado2 <- azar(7)
			tirada <- dado1 + dado2
	
			Si tirada = 10 Entonces
				coincidencias = coincidencias +1
			Fin Si
			
			controlador = controlador + 1
			
		Fin Mientras
		
		Escribir "El azar ... sumó 10 un total de " coincidencias " veces"
	
	FinProceso
```


### JSHint
- [JSHint Online](http://jshint.com/)
- [JSHint About](http://jshint.com/about/)
- [JSHint Repository](https://github.com/jshint/jshint)

### Consola

- [@ChromeDevTools en Twitter](https://twitter.com/chromedevtools?lang=es)
- [Chrome DevTools](https://developer.chrome.com/devtools)

**Métodos:**
- .assert() *Aparece un mensaje de error en la consola si la afirmación es falsa.*:
```javascript
 var controlador = false;
 console.assert(controlador, "\"controlador\" es igual a \"false\"");
```

- .clear() *Limpia la consola*:
```javascript
 console.clear()
```


- .dir() *Retorna una lista interactiva de las propiedades de un objeto*:
```javascript
 console.dir(document.body);
```

- .dirxml() *Retorna una representación HTML del objeto*:
```javascript
 console.dirxml(document.body);
```


- Agrupadores:
 - .group() *Crea un grupo de mensajes de consola*:
 ```javascript
     console.group("bucleFor");
     for(var i=100; i>0; i--){
         console.info("Iteración numero %i", i)
     }
     console.groupEnd();
 ```
 - .groupCollapsed() *Crea un grupo de mensajes de consola minimizados (por defecto)*:
 ```javascript
     console.groupCollapsed("bucleFor");
     for(var i=100; i>0; i--){
         console.info("Iteración numero %i", i)
     }
     console.groupEnd();
 ```
 - .groupEnd() *Cierra el grupo de mensajes*:
 ```javascript
     console.group("bucleFor");
     for(var i=100; i>0; i--){
         console.info("Iteración numero %i", i)
     }
     console.groupEnd();
 ```


- Tablas:
 - .table() *Muestra los datos dentro de una tabla*:
 ```javascript
 var lenguajes = [
     { nombre: "JavaScript", extension: ".js" },
     { nombre: "TypeScript", extension: ".ts" },
     { nombre: "CoffeeScript", extension: ".coffee" }
 ];
 
 console.table(lenguajes);
 
 console.table(lenguajes, "extension");
 ```

- Gestión del tiempo:
 - .time() *Inicia un contador en ms*:
 - .timeEnd() *Para el contador y devuelve el resutlado*:
 ```javascript
  console.time("Medición de miArray");
  var miArray = new Array(1000000);
  for (var i = miArray.length - 1; i >= 0; i--) {    
   miArray[i] = new Object();
  };
  console.timeEnd("Medición de miArray");
 ```

- Notificadores:
 - .log() *Saca un mensaje por consola*:
 ```javascript
  console.log("Hola en formato clásico");
 ```
 - .info() *Similar a console.log*:
 ```javascript
  console.info("Hola en formato informativo");
 ```
 - .warn() *Similar a Console.log*:
 ```javascript
  console.warn("Hola en formato alerta");
 ```
 - .error() *Similar a console.log, invcluye *:
 ```javascript
  console.error("Hola en formato error");
 ```

- Formateadores:

Formato | Descripción
------------ | -------------
%s | Cadena
%d o %i | Número entero
%f | Decimal
%o | DOM
%O | Objeto js
%c | CSS

- Ejemplos:
 - *%o* para estrcuturas del DOM
 ```javascript
  var parrafos = document.getElementsByTagName("p");
  console.log("DOM: %o", parrafos);
 ```
 - *%O* para objectos JS
 ```javascript    
  var objeto = {"nombre":"Yo","Apellido":"Mismo"};
  console.log("Objeto: %O", objeto);
 ```
 - usando CSS:
 ```javascript
  console.log('Esto es aburrido...');
  console.log('%c Pero se puede mejorar fácilmente! ', 'background: #3EBDFF; color: #FFF; font-size:25px;');
 ```
