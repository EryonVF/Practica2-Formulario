# Practica2-Formulario
1. Explique el funcionamiento de la etiqueta input en HTML, indicando los diferentes argumentos que puede tener.
La etiqueta <input> en HTML es un elemento utilizado para crear campos de entrada en un formulario web. Puede tener varios atributos que controlan su comportamiento y apariencia. etiqueta <input>:
type: Este es uno de los atributos más importantes y define el tipo de campo de entrada que se creará. Algunos valores comunes para type incluyen text (para campos de texto), password (para contraseñas), radio (botones de selección única), checkbox (casillas de verificación), submit (botones de envío de formulario), file (para cargar archivos), entre otros.
-name: Este atributo se utiliza para asignar un nombre al campo de entrada, lo que permite identificarlo y procesar su valor en el lado del servidor cuando se envía el formulario.
-value: Este atributo establece un valor predeterminado para el campo de entrada. Cuando el usuario interactúa con el campo, puede editar este valor.
-placeholder: Este atributo proporciona un texto de marcador de posición que se muestra en el campo antes de que el usuario ingrese cualquier dato. Es útil para proporcionar una breve descripción o ejemplo de lo que se espera en el campo.
-required: Este atributo, cuando está presente, indica que el campo es obligatorio y el usuario debe completarlo antes de enviar el formulario.
-disabled: Cuando se establece como disabled, el campo se desactiva y el usuario no puede interactuar con él.
-readonly: Cuando se establece como readonly, el campo se vuelve de solo lectura, lo que significa que el usuario puede ver su contenido pero no editarlo.
  

2. Explique como puede configurarse la etiqueta button
Se puede configurar la etiqueta <button> en HTML de la siguiente manera:
-Contenido interno: El contenido interno del botón define el texto o contenido visible para el usuario.
-Atributo type: Determina la función del botón, con opciones como submit para enviar un formulario, reset para restablecer campos, o button para acciones personalizadas en JavaScript.
-Atributo name: Asigna un nombre al botón, útil cuando tienes múltiples botones en un formulario para identificar cuál se hizo clic.
-Atributo value: Establece un valor que se envía junto con el formulario cuando se hace clic en el botón, lo que puede ser útil para enviar información adicional.
-Atributo disabled: Desactiva el botón al establecerlo como disabled, impidiendo que el usuario haga clic en él.
-Atributo onclick: Permite ejecutar una función JavaScript personalizada cuando se hace clic en el botón, lo que es útil para acciones específicas en respuesta al clic del usuario.
Estos atributos y configuraciones te permiten personalizar la apariencia y el comportamiento de un botón HTML según tus necesidades específicas en tu página web.

3. Explique el método addEventlistener y como se utiliza en este proyecto
Permite la detección y respuesta a eventos en elementos HTML. Este método se utiliza para vincular funciones que se ejecutarán cuando ocurran ciertos eventos, como clics, envíos de formularios, movimientos del mouse, entre otros. En resumen, addEventListener permite la interacción dinámica y la respuesta del código JavaScript a las acciones del usuario en una página web, mejorando así la experiencia del usuario y la funcionalidad de la aplicación web.
El método addEventListener En este proyecto del formulario se utiliza para realizar acciones cuando el formulario se envía.
En el primer uso, addEventListener se utiliza para esperar a que el documento HTML se haya cargado completamente. Cuando eso sucede, se ejecuta la función que contiene todo el código relacionado con el formulario.
Luego se utiliza addEventListener nuevamente para escuchar el evento de envío del formulario, que se desencadena cuando el usuario hace clic en el botón "Enviar". se ejecuta la función de manejo de eventos que incluye la validación de los campos y el manejo de errores.

4. Explique la forma en que son validadas cada una de las entradas. 
-ID (5 dígitos exactos):
Validación: Se utiliza una expresión regular /^\d{5}$/ para asegurarse de que se ingresen exactamente 5 dígitos.
Mensaje de error: Si no se dan los valores correctos, aparece el error "El ID debe tener 5 dígitos exactos."

-Nombre:
Validación: Se verifica si el campo de nombre está en blanco utilizando nombre.trim() === "".
Mensaje de error: Si el campo está en blanco,aparece el error "El nombre no puede estar vacío."

Apellidos:
Validación: Similar a la validación del nombre, se verifica si el campo de apellidos está en blanco con apellidos.trim() === "".
Mensaje de error: Si el campo está en blanco,aparece el error "Los apellidos no pueden estar vacíos."

Teléfono (###)###-####:
Validación: Se utiliza una expresión regular /^\(\d{3}\)\d{3}-\d{4}$/ para asegurarse de que el valor ingresado tenga el formato correcto de un número de teléfono.
Mensaje de error: Si no se dan los valores correctos, aparece el error "El teléfono debe tener el formato (###)###-####."

Correo Electrónico:
Validación: Se utiliza una expresión regular para verificar si el valor ingresado se ajusta a un formato de correo electrónico válido.
Mensaje de error: Si no se dan los valores correctos, aparece el error "El correo electrónico no es válido."

Edad (Número positivo):
Validación: Se convierte el valor de edad en un número entero y se verifica si es un número positivo utilizando isNaN(edadNum) || edadNum <= 0.
Mensaje de error: Si la validación falla, aparece el error "La edad debe ser un número positivo."

Fecha de Nacimiento (AAAA-MM-DD):
Validación: Se utiliza una expresión regular /^\d{4}-\d{2}-\d{2}$/ para asegurarse de que el valor ingresado tenga el formato correcto de una fecha.
Mensaje de error: Si no se dan los valores correctos, aparece el error "La fecha de nacimiento debe tener el formato AAAA-MM-DD."
