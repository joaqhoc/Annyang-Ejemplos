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
		    	'redes': function() {
		        document.getElementById("ejemplo3").value = "Redes:";
		        document.getElementById("ejemplo3").className = "btn btn-lg btn-success btn-block";
		        document.getElementById("ejemplo3").hidden = "";
		        document.getElementById("facebook").style.display = 'block';
		        document.getElementById("facebook").className = "btn btn-lg btn-primary btn-block";
		        document.getElementById("twitter").style.display = 'block';
		        document.getElementById("twitter").className = "btn btn-lg btn-danger btn-block";
		        document.getElementById("youtube").style.display = 'block';
		        document.getElementById("youtube").className = "btn btn-lg btn-info btn-block";
		      },
			    'facebook': function() {
		        window.location.href = "https://facebook.com/joaquincentu";
		        document.getElementById("facebook").value = "Redireccionando";
		        document.getElementById("facebook").className = "btn btn-lg btn-success btn-block";
		      },
		      	'twitter': function() {
		        window.location.href = "https://twitter.com/joaqho";
		        document.getElementById("twitter").value = "Redireccionando";
		        document.getElementById("twitter").className = "btn btn-lg btn-success btn-block";
		      },
		      	'youtube': function() {
		        window.location.href = "https://youtube.com/channel/UC96eVw3k0EXT3q6ruaW_pJA";
		        document.getElementById("youtube").value = "Redireccionando";
		        document.getElementById("youtube").className = "btn btn-lg btn-success btn-block";
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

> Ejemplo 4

```javascript
    <script>
      "use strict";
      if (annyang) {
        // Definimos nuestro primer comando. Primero escribimos el comando y posteriormente la función a ejecutar.
        //api google AIzaSyCer2C9iE2qvsnCOm6cjGlEuYJRvqw18y0
        //buscador facebook: https://www.facebook.com/search/top/?q=
        //buscador google: https://www.google.com/search?q=
        var commandos = {

            'abajo': function() {
             window.location.href = "#abajo";

          },
            'arriba': function() {
            window.location.href = "#";

          },
            'siguiente': function() {
            document.getElementById("siguiente").click();

          },
            'anterior': function() {
            document.getElementById("anterior").click();

          },
          'cabecera': function() {
            window.location.href = "#cabecera_1";

          },
          'foto uno': function() {
            window.location.href = "#foto_1";

          },
          'foto dos': function() {
            window.location.href = "#foto_2";

          },
          'foto tres': function() {
            window.location.href = "#foto_3";

          },
          'enlace uno': function() {
            document.getElementById("enlace_1").click();

          },
          'enlace dos': function() {
            document.getElementById("enlace_2").click();

          },
          'enlace tres': function() {
            document.getElementById("enlace_3").click();

          },
          'buscar': function() {
            document.getElementById("buscador").select();
            document.getElementById("start-record-btn").click();

          },
          'buscar texto': function() {
            document.getElementById("enviar").click();

          },
          'eliminar texto': function cambiaValores() {
            document.getElementById("buscador").value = "";
          }

        }

        // OPCIONAL: active el modo de depuración para un registro detallado en la consola
        annyang.debug();

        // Agregamos nuestros comandos a annyang.
        annyang.addCommands(commandos);

        //Establecemos el lenguaje, en mi caso es español de México (puedes ver la lista completa de lenguajes soportados aquí).
        annyang.setLanguage("es-MX");

        // Empezmaos a escuchar.
        annyang.start();
     } else {
    $(document).ready(function() {
      $('#unsupported').fadeIn('fast');
    });
  }

     var scrollTo = function(identifier, speed) {
    $('html, body').animate({
        scrollTop: $(identifier).offset().top
    }, speed || 1000);
  }
  </script>
```
