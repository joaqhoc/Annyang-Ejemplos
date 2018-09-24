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
<script src="//cdnjs.cloudflare.com/ajax/libs/annyang/2.6.0/annyang.min.js"></script>
<script>
if (annyang) {
  // Let's define our first command. First the text we expect, and then the function it should call
  var commands = {
    'show tps report': function() {
      $('#tpsreport').animate({bottom: '-100px'});
    }
  };

  // Add our commands to annyang
  annyang.addCommands(commands);

  // Start listening. You can call this here, or attach this call to an event, button, etc.
  annyang.start();
}
</script>
```



