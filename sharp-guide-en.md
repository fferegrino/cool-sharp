Yet another style guid for C#
==================

## Why?
I'm sure you are wondering why do you need a style guide if you already know how to program. True that, but let me tell you something (and I don't mean to be rude): **Anyone can write code**. Anyone with some months of experience, maybe a lecture or even an internet video can write a functional app in little time. Writing code that works is easy, writing good code that works is way harder.

### The Good Code
About The Good Code, everyone seems to have a distinct opinion, yet there are some points where those opinions come together, based on those I dare to say that The Good Code is:

 - Efficient
 - Maintainable
 - Well organized
 - Legible

Writing The Good Code is an art that you must learn, practice and encourage. To adopt an style (or create your own) could help you to achieve that.

### About style guides
Contrary to what it might seem, this guide (and any other you may happen to find) isn't a rulebook that you must follow strictly, there may be things that simply you cant integrate into your organization due philosophical reasons, compatibility with legacy systems or complicated errors in The Matrix. So, take this kind of guides as suggestions that, if applied to your organization, might help to keep an standardized code, easily legible and maintainable for everyone in your dev team.

## The Guide
### My name is Asdflkj, James Asdflkj
Incredibly, choosing the right names for your variables, methods and classes could make the difference between wanting to use an old code or write the same code from scratch. You may not want to find out for what you were using that `c` variable inside the `buysomething` method and prefer to write the `muysomething2` method instead. Think about it.

#### Recommendations about naming

 - Use comprehensible names for classes, methods, variables, etc. 

 - In case of class properties, unless another logic is needed, always use Auto-Implemented properties.  
 `int Property { get; set; }`  
 
 - Use an `_` before a member variable, then write the name using *camel casing*.  
`private int _clientId`  
`private string _name;`  

 - When using boolean variables, use prefix words like "can", "is", or "has", depending on what they represent.  
 `public bool IsCool { get; set; }`  
 `private bool _hasChildren;`  
 
 - Avoid using variable names that look like C# (or any other language) reserved keywords.

 - Usa nombres completos siempre que sea posible, es deir, evita abreviaturas. Si se está trabajando con siglas o acrónimos debes mantener todos sus caractéres en mayúsculas.  
`string addr; // incorrecto`  
`string address; // correcto`  
`void PublishHTML() { ... // correcto`  
`void PublishHypertextTrans... // incorrecto`  

 - Usa nombres de variables de una sola letra solo en caso de bucles, siempre y cuando no se usa más que para contador de iteraciones.
`for(int i = 0; i < value; i++) {`  

 - Usa *pascal casing* para nombrar clases,  métodos y estructuras.
 `class SharpGuide { ...`  
 `void FixMatrix(int matrixId) { ...`  

 - Usa *camel casing* para los nombres de variables y parámetros de método.
 `string awesomeProgrammingLanguage = "C#";`  
 `void SetLanguage(string someLanguage) { ...`  

 - Para las interfaces antepón una `I` al nombre que debe estar escrito usando *camel casing*  
 `interface IStyleGuide { ...`  
 
 - En cuanto a los espacios del nombre, la convención es bastante clara, utiliza un formato como este  `<company name>.<product name>.<top module>.<bottom module>`

 - Los archivos deben llamarse como la clase o interfaz pública que contienen.
 
### ¿Comentarios? ¿en serio?
Hay algunas organizaciones que requieren que comentes tu código o puede que aún después de escribir una poesía con tu código (y los nombres de variables y métodos) tu programa no sea tan entendible debido a alguna lógica necesaria del negocio o algún truco para eficientar la ejecución, ese es el momento de usar los comentarios.

 - No narres tu código a través de los comentarios, o en otras palabras, no escribas un comentario por cada línea de código que escribas.  

 - Escribe los comentarios en líneas que no contengan código y siempre antes de la sección a la que te quieres referir. Una excepción son las declaraciones o inicializaciones de variables.

 - Usa `//` o `///` para escribir comentarios. Evita `/* ... */` (y evita escribir comentarios de más de una línea).  
 
 
 - Tus comentarios son hermosos sin necesidad de que les hagas una cajita de `********` al rededor, así que también evita hacerlo.

 - Revisa la ortografía de tus comentarios y asegurate de que sean claros al momento de leerlos.

 - Hay un comentario muy especial que debes usar cada vez que dejes código sin finalizar, ese es el comentario `// TODO: [descripción]` ya que el entorno de desarrollo, si usas Visual Studio, identificará ese comentario como una funcionalidad pendiente de acabar y esta aparecerá en la lista de tareas pendientes.  

 - En caso de que un método o clase no sea autodocumentable o necesites proveer de infromación específica para su uso, emplea los comentarios XML con  `///` para que, en caso de que el IDE lo permita, esta documentación se muestre cuando alguien más (o tu mismo) haga uso del elemento documentado.  

 - Recuerda que C# permite crear documentación en XML, para lo cual es necesario que esté bien formado.

### Estructura de un archivo y una clase
También hay recomendaciones con respecto a los archivos, su estructura y su contenido.

 - Procura que un archivo contenga una sola clase, habrá casos en los que tal vez no se pueda, pero en general es posible.

 - El archivo de una clase debe llamarse igual que la clase que contiene.

 - Usa `tab` con tamaño de 4 para indentar el código en lugar de espacios

 - Siempre escribe los corchetes `{ }` en líneas nuevas.

 - Agrupa líneas de código de acuerdo a la labor que realizan, separa dichos grupos por una línea en blanco.

 - Separa por una sola línea los métodos definidos en una clase.

 - La estructura general de un archivo es:
	 - Sentencias *using*
	 - *namespace*
	 - Declaración de la clase
	 -  Variables privadas
	 - Propiedades privadas
	 - Métodos privados
	 - Constructores
	 - Propiedades públicas
	 - Métodos publicos  

 - La usa las directivas `#region` y `#endregion` para agrupar todas las categorías  anteriores y sea fácil navegar entre ellas.

### Algunas buenas prácticas

 - Evita los métodos muy largos, procura conservar de 1 ~ 30 líneas de código. Si se pasa tal vez sea necesario revisarlo para ver si se puede separar en dos o varios métodos.

 - Nuevamente, **autodocumenta** tus métodos, si el nombre es claro no hay necesidad de explicar demasiado mediante los comentarios.

 - No mezcles varias tareas en un solo método. Un solo método debe hacer una sola acción.

 - Prefiere el uso de los alias de tipos de dato conocidos para declarar variables. Es decir, prefiere `string awesome = "awesome!";` a `String awesome = "awesome!"`.

 - Por el contrario, utiliza los tipos definidos en el `namespace System` para hacer referencia a constantes o métodos de clase: `int t = Int32.ParseInt("0");` mucho mejor que `int t = int.ParseInt("0");`.

 - No todo dentro de una clase tiene que ser público o privado, usa el modificador de acceso `internal` para propiedades y métodos si solo se accede a ellos dentro del mismo ensamblado.

 - Si un método recibe más de 5 o 6 parámetros considera reemplazarlos por una estructura o una clase.

 - **NUNCA, nunca** *hardcodees*[^1] números, cadenas o cualquier otro valor. Usa fuentes externas de datos (archivos, baess de datos, línea de comandos...).

 - Utiliza `String.Empty` en lugar de las comillas vacías `""`.

 - Cuando sea necesario comprobar si una cadena está vacía utiliza los métodos del framework: `String.IsNullOrEmpty` o `String.IsNullOrWhiteSpace`.

 - Procura sobreescribir el método `Equals` en las clases definidas por el usuario.  

## Contribuciones
Soy solo un ser humano que gusta de programar, especialmente en C#, así que como bien dije, este no es un libro de reglas, solo algunas cuantas cosas que yo considero buenas prácticas. Si quieres hacer algún comentario, queja o sugerencia con respecto a esta guía, puedes hacerlo en [https://github.com/fferegrino/cool-sharp/issues](https://github.com/fferegrino/cool-sharp/issues), o antonio.feregrino@hotmail.es

[^1]: Mala práctica del en el desarrollo de software que consiste en incrustar datos relacionados con la lógica de la aplicación directamente en el código fuente de un programa.


