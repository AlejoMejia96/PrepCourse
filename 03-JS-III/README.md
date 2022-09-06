![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)

<table class="hide" width="100%" style='table-layout:fixed;'>
  <tr>
    <td>
      <a href="https://airtable.com/shrSzEYT4idEFGB8d?prefill_clase=03-JS-II">
        <img src="https://static.thenounproject.com/png/204643-200.png" width="100"/>
        <br>
        Haz click acá para dejar tu feedback sobre esta clase.
      </a>
    </td>
  </tr>
</table>

# JavaScript III

En esta lección cubriremos:

* Bucles
* Arrays y sus métodos

## Bucles

![loop](./img/loops.png)

La mayoría del software se ejecuta en bucles, evaluando expresiones una y otra vez hasta que devuelve lo que estamos buscando o se detiene después de cierto tiempo. Javascript tiene dos expresiones de bucle incorporadas: `for` y `while`.

### Bucle *`for`*

Los bucles `for` tienen una sintaxis única, similar a la instrucción `if`, pero un poco más compleja. Primero tenemos la palabra clave `for`, seguida de paréntesis y luego abrimos y cerramos llaves. Dentro de los paréntesis, necesitaremos tres cosas: primero, debemos declarar una variable sobre lo que se iterará o repetirá el bucle, después tendremos una expresión condicional, el ciclo continuará sucediendo hasta que esta declaración no se cumpla, ,esto es, sea `false` y, finalmente, incrementaremos nuestra variable de iteración. Las tres declaraciones están separadas por un punto y coma ( `;` )

```javascript
for (var i = 0                 ; i < 10                 ; i++          ) {
// | Declaramos una variable | Expresión condcicional | Incrementamos la variable |
    console.log(i);
}
```

En este ejemplo, vemos que inicialmente establecemos nuestra variable `i` en 0, el ciclo se ejecutará y cada vez que llegue al final, aumentará el contador en uno. El bucle `for` evaluará la expresión condicional. Si es `true`, se ejecutará nuevamente, si es `false` dejará de funcionar.

¿Recuerdas el método .length de los datos de tipo "String"? Podemos usarlo para realizar ciclos for para un string, al igual que acceder a cada caracter de este:

```javascript
function encontrarVocalA(string){
  for(var i = 0; i < string.length; i++){
    if(string[i] === 'a'){
      return "Encontramos la vocal"
    }
  }
   return "El string no tiene ninguna letra a"
}
```
En este ejemplo, la variable `i` estará recorriendo cada caracter del string y accediendo a su valor con `string[i]` para verificar si esta coincide con la vocal `a`. Cuando llega al último valor y este no coincide, el ciclo for se termina y finalmente la función retorna "El string no tiene ninguna letra a", pues no encontró ninguna letra `a` en el string. 

Debemos tener cuidado con la condición del bucle. Si esta condición es siempre `true`, entonces el ciclo nunca terminará dando lugar al llamado *Bucle infinito*, como en el siguiente ejemplo:

```javascript
for (let i = 0; i >= 0; i++) {
    console.log(i);
}
```
Debido a que nuestra expresión condicional SIEMPRE será true (i nunca será menor que 0), este ciclo se ejecutará esencialmente para siempre. Esto interrumpirá su programa y puede bloquear su navegador web o computadora.

### Bucle *`while`*

Al igual que el bucle `for`, el `while` es una manera de iterar, pero en esta declaramos una sentencia que va a ejecutar nuestro código mientras que sea verdadera.

```javascript
var n = 0;

while (n < 3) {
  n++;
}
console.log(n); //3
```
En este caso, le estamos indicando que mientras que `n` sea menor a 3, itere aumentando su valor en uno. Cuando `n` pasa a ser 3 va a dejar de iterar ya que la condición `n < 3` va a ser `false`.

¡Ten cuidado igualmente con la condición que no genere un bucle infinito!


## Homework

Realiza los ejercicios propuestos en el archivo `homework.js` de esta misma carpeta, el cual tiene test. Si no recuerdas cómo debes correr el test, revisa el archivo `README` que se encuentra al final del repositorio.

## Recursos adicionales

* [MDN: for Loops](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/for)
* [Codecademy: Learn Javascript](https://www.codecademy.com/learn/learn-javascript)
* [Udacity: Intro to Javascript](https://www.udacity.com/course/intro-to-javascript--ud803)
* [MDN: Official Javascript Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

