# extractLinksFromMd

* **Track:** _Common Core_
* **Curso:** _JS Deep Dive: Crea tu propia librería usando JavaScript_
* **Unidad:** _Producto final_

***

## SEMANA 1
Formar equipo.  [X]
Elegir reto.    [X]
Hacer fork de reto modelo o crear nuevo repo si has propuesto un reto no propuesto por Laboratoria. [X]
Escribir primera versión del README.md con una descripción general de la librería así como ejemplos (snippets) de uso y configuración (si fuera necesario). [X]
Crear issues y milestones que sirvan como hoja de ruta (roadmap) 
Inicializar proyecto con npm init y git init.
Crear index.html con ejemplo principal de uso.
## SEMANA 2
Agregar tests que describan la API de tu librería y los casos de uso esperados.
Implementar funcionalidad esencial.
Hacer code review con tus compañeras e instructorxs.
## SEMANA 3
Completar implementación de librería y ejemplo principal (usando la librería).
Hacer code review con tus compañeras e instructorxs.
Preparar tu demo/presentación.
Publicar el ejemplo principal (index.html) en GitHub pages.


***

Implementar un módulo de Node.js que reciba un string (en formato Markdown) y
extraiga todos los links encontrados. La implementación debe ser una función que
recibe un string y devuelve un arreglo de objetos como se muestra en el este
ejemplo:

```js
const extractLinksFromMd = require('extract-links-from-md');
const str = `# Lorem ipsum

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
incididunt ut [labore](https://en.wiktionary.org/wiki/labore) et
[dolore](https://en.wiktionary.org/wiki/dolore) magna aliqua. Ut enim ad minim
veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat.

[foo](http://foo.com)

Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu
fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
culpa qui officia deserunt mollit anim id est laborum.`;

const links = extractLinksFromMd(str);

console.log(links);
// [
//   { href: 'https://en.wiktionary.org/wiki/labore', text: 'labore' },
//   { href: 'https://en.wiktionary.org/wiki/dolore', text: 'dolore' },
//   { href: 'http://foo.com', text: 'foo' },
// ]
```
