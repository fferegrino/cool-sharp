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
### Convención sobre nombres

 - Usa nombres comprensibles que se autodocumenten para clases, métodos, variables, etc.
 - En caso de variables de método, a menos que se requiera otra lógica, procura siempre usar las propiedades autoimplementadas `int Property { get; set; }`  
 
 - En caso de ser necesarias, utiliza un `_` antepuesto al nombre de una variable miembro, escrita con *Camel Casing*
`private int _clientId`
`private string _name;`  

 - Usa nombres completos siempre que sea posible, es deir, evita abreviaturas. Si se está trabajando con siglas o acrónimos debes mantener todos sus caractéres en mayúsculas  
`string addr; // incorrecto`
`string address; // correcto`
`void PublishHTML() // correcto`
`void PublishHypertexTrans... // incorrecto`  

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
 
  

