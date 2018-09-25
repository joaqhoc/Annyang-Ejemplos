# 📃Annyang Ejemplos 📃

> Web Oficial: https://www.talater.com/annyang/

> GitHub Oficial: https://github.com/TalAter/annyang


¿Que es Annyang?
- Annyang es una pequeña biblioteca de JavaScript que permite a los visitantes controlar su sitio con comandos de voz.
Annyang soporta múltiples idiomas, no tiene dependencias, pesa solo 2kb y es de uso gratuito.


================================================================



# Codigo Ejemplo 🌐

> Ejemplo 1

```javascript
	<script>
		  if (annyang) {
		    // Definimos nuestro primer comando. Primero escribimos el comando y posteriormente la función a ejecutar.
		    var commandos = {
		      'hola': function() {
		        document.getElementById("ejemplo1").value = "Estado: OK!";
		        document.getElementById("ejemplo1").className = "btn btn-lg btn-success btn-block";
		      }
		    };

		    // Agregamos nuestros comandos a annyang.
		    annyang.addCommands(commandos);

		    //Establecemos el lenguaje, en mi caso es español de México.
		    annyang.setLanguage("es-MX");

		    // Empezamos a escuchar.
		    annyang.start();
		 }
	</script>
```

> Ejemplo 2

```javascript
	<script>
		  if (annyang) {
		    // Definimos nuestro primer comando. Primero escribimos el comando y posteriormente la función a ejecutar.
		    var commandos = {
		      'reproducir': function() {
      
			    var waitTime = 150;
			    setTimeout(function () {      
			        if ($('#reproductor').get(0).paused) {
			          $('#reproductor').get(0).play();
			        }
			      }, waitTime);
			    console.log("reproducir");
			    },
			   'pausar': function() {
			      $('#reproductor').get(0).pause();
			    console.log("pausar");
			    }
		    };

		    // Agregamos nuestros comandos a annyang.
		    annyang.addCommands(commandos);

		    //Establecemos el lenguaje, en mi caso es español de México (puedes ver la lista completa de lenguajes soportados aquí).
		    annyang.setLanguage("es-MX");

		    // Empezmaos a escuchar.
		    annyang.start();
		 }
	</script>
```



> Ejemplo 3

```javascript
	<script>
		  if (annyang) {
		    // Definimos nuestro primer comando. Primero escribimos el comando y posteriormente la función a ejecutar.
		    var commandos = {
		      'facebook': function() {
		        window.location.href = "https://facebook.com";
		      	}
		    };

		    // Agregamos nuestros comandos a annyang.
		    annyang.addCommands(commandos);

		    //Establecemos el lenguaje, en mi caso es español de México (puedes ver la lista completa de lenguajes soportados aquí).
		    annyang.setLanguage("es-MX");

		    // Empezmaos a escuchar.
		    annyang.start();
		 }
	</script>
```
