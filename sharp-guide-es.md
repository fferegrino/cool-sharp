Guía de estilo para C#
======
## ¿Por qué?
Seguramente te estarás preguntando para qué necesitas una guía de estilo si tu ya sabes programar. Cierto, pero déjame decirte algo esperando no sonar ofensivo: **Cualquiera puede programar**. Cualquiera con unos cuantos meses de experiencia, alguno que otro curso o vídeo en internet puede escribir una aplicación funcional en poco tiempo. Hacer código que funcione es sencillo, hacer un buen código que funcione es lo complicado.
### El Buen Código
Respecto al buen código, todos pueden tener una opinión distinta sin embargo hay temas my mencionados en cualquier definición de El Bbuen Código, basándonos en eso podemos decir que es:

 - Eficiente
 - Mantenible
 - Organizado
 - Legible

Escribir El Buen Código es un arte que tu debes aprender, practicar y fomentar. Adoptar un estilo (o crear uno propio) te puede ayudar a conseguirlo.

### Sobre las guías de estilo
A diferencia de lo que podría parecer, esta guía (y todas las demás que te encuentres) no son mandamientos que debes seguir estrictamente, porque tal vez haya aspectos que no se puedan integrar a tu organización por cuestiones filosóficas de la empresa, compatibilidad con sistemas antiguos o complicados errores en la Matrix. Así que toma estas guías como sugerencias que si son adoptadas por tu organización te ayudarán a mantener un código estandarizado, que sea fácilmente legible por todos miembros del equipo de desarrollo y, en caso de ser requerido, sea mantenible.
## La guía
### Te voy a cambiar el nombre...
Increíblemente, escoger buenos nombres para tus variables de programa, métodos y clases puede ser la diferencia entre querer revisar un código viejo o rehacer todo de nuevo. Tal vez no quieras buscar para qué usas esa variable `c` dentro del método `compraalgo` y prefieras reescribir todo. No sé, piénsalo.

 - Usa nombres comprensibles que se autodocumenten para clases, métodos, variables, etc.
 - En caso de variables de método, a menos que se requiera otra lógica, procura siempre usar las propiedades autoimplementadas  
 `int Property { get; set; }`  
 
 - En caso de ser necesarias, utiliza un `_` antepuesto al nombre de una variable miembro, escrita con *Camel Casing*
`private int _clientId`  
`private string _name;`  
 - Para el caso de variables tipo booleanas, además del usa un prefijo como "can"(puede), "is"(es) o "has"(tiene)  
 `public bool IsCool { get; set; }`  
 `private bool _hasChildren;`  
 
 - No uses nombres de variables que se puedan parecer a palabras reservadas de C#

 - Usa nombres completos siempre que sea posible, es deir, evita abreviaturas. Si se está trabajando con siglas o acrónimos debes mantener todos sus caractéres en mayúsculas  
`string addr; // incorrecto`  
`string address; // correcto`  
`void PublishHTML() { ... // correcto`  
`void PublishHypertextTrans... // incorrecto`  

 - Usa nombres de variables de una sola letra solo en casod e bucles, siempre y cuando no se usa más que para contador de iteraciones
`for(int i = 0; i < value; i++) {`  

 - Usa *Pascal Casing* para nombrar clases y métodos
 `class SharpGuide { ...`  
 `void FixMatrix(int matrixId) { ...`  

 - Usa *Camel Casing* para los nombres de variables y parámetros de método
 `string awesomeProgrammingLanguage = "C#";`  
 `void SetLanguage(string someLanguage) { ...`  

 - Para las interfaces antepón una `I` al nombre que debe estar escrito usando *Camel Casing*  
 `interface IStyleGuide { ...`  
 
 - En cuanto a los espacios del nombre, la convención es bastante clara, utiliza un formato como este `<company name>.<product name>.<top module>.<bottom module>`
 - Los archivos deben llamarse como la clase pública que contienen.
 
### ¿Comentarios? ¿en serio?
Hay algunas organizaciones que requieren que comentes tu código o puede que aún después de escribir una poesía con tu código (y los nombres de variables y métodos) tu programa no sea tan entendible debido a alguna lógica necesaria del negocio o algún truco para eficientar la ejecución, ese es el momento de usar los comentarios.

 - No narres tu código a través de los comentarios, o en otras palabras no escribas un comentario por cada línea de código que escribas  

 - Escribe los comentarios en líneas que no contengan código y siempre antes de la sección a la que te quieres referir. Una excepción son las declaraciones o inicializaciones de variables.
 - Usa `//` o `///` para escribir comentarios. Evita `/* ... */` (y evita escribir comentarios de más de una línea)  
 
 - Tus comentarios son hermosos sin necesidad de que les hagas una cajita de `********` al rededor, así que también evita eso

 - Revisa la ortografía de tus comentarios y asegurate de que sean claros al momento de leerlos
 - Comentarios en XML, C# ofrece la posibilidad de escribir comentarios 
