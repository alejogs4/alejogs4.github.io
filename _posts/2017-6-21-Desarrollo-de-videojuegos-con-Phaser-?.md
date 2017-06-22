Desde que empecé en la programación he escuchado a personas que quieren aprender a programar, por que quieren desarrollar
videojuegos y personalmente ese es mi caso, desde que era pequeño siempre que veía un juego pensaba yo le pondría esto o le modificaría esto,
entonces desde hace unos meses que me quise iniciar en el desarrollo de videojuegos, mi  primera tarea fue buscar un motor o librería que me ayudara
para tal fin y a continuación se las presento.

# Phaser

En mi [primer post](https://alejogs4.github.io/Que-lenguaje-aprender-primero/) ya habia hablado un poco sobre [Phaser](http://phaser.io/),
el cual es un Framework para el desarrollo de videojuegos que usa HTML y JavaScript y donde el juego que hagas se va poner en el Canvas de
HTML5 o en WebGL dependiendo del navegador donde te encuentres, además  de esto las principales características de Phaser son que permite
 la precarga de archivos (Imágenes, JSON), manejo de Sprites, grupos,animación,partículas, cámara, entradas (Teclado, Mouse, Multi-touch y Gamepad),
 sonido (Codecs como ogg, wav, mp3 según el navegador), tilemaps, escalamiento (Device Scaling), un sistema de plugins y navegador móvil.
 
 ![Phaser]({{ site.baseurl }}/images/phaser.PNG "Phaser")
 
 Ahora, puedes empezar a utilizar Phaser de una manera muy fácil como te muestro a continuación:
 ## HTML
 ```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Flights and ships</title>
    <script src="js/phaser.js"></script>
    <script src="js/game.js"></script>
</head>
<body>
    <div class="juego"></div>
</body>
</html>
```
En la parte de HTML no hay mayor misterio solo se adjuntan los scripts que vayamos a utilizar (Phaser.js y game.js) y después un div
que servirá como contenedor para nuestro juego.

## Javascript
```
var game=new Phaser.Game(1110,600,Phaser.AUTO,'game');

var primerMundo={

    preload:function(){
        //Aqui se cargan todos los archivos del juego(Imagenes,audio,etc..)
    },
    create:function(){
        //Aqui se ponen en pantalla todos los elementos anteriormente cargados

    },
    update:function(){
        //Aqui se desarrolla la logica del juego: Colisiones,movimiento entre otros

    }
};
game.state.add('primerMundo',primerMundo);
game.state.start('primerMundo');
```
En JavaScript se declaran se declaran objetos que en Phaser son llamados estados, en el ejemplo anterior esta el estado primerMundo,
cabe destacar que puedes tener todos los estados que quieras y que cada estado debe tener como mínimo los métodos preload,create y update.

# Llevar nuestro juego a moviles

Phaser además de permitir que nuestro juego sea reproducido en navegadores Web, también  nos permite que nuestro juego sea llevado a 
plataformas móviles como android y ios, mediante la herramienta de [Crosswalk](https://crosswalk-project.org/), la cual puede funciona de
una manera parecida a Phonegap pero tiene un mejor performance lo cual permite que la experiencia de usuario se bastante mejor teniendo en cuenta
que es un juego lo cual siempre sera mas demandante que una apliacion normal.

Por ultimo te dejo tres paginas para que descargues recursos para tus indie games y aprendas mas sobre Phaser.
+ [Open Game Art](https://opengameart.org/)

 ![Game Art]({{ site.baseurl }}/images/openGame.png "Open Game Art")

+ [Untamed](http://untamed.wild-refuge.net/rmxpresources.php?characters)

![Untamed]({{ site.baseurl }}/images/sithjester.png "Untamed")

+ [Curso de phaser](https://www.youtube.com/playlist?list=PLGy53JXEnxNYqR8DqITaFmDU1v9g6dYz6)

