# FASE I: Recoger datos de un formulario (Servlet + salida html con PrintWriter)

Vamos a aprender a leer los parámetros enviados desde un formularios.

Usaremos nuestra primera página JSP.

Llamaremos a nuestro proyecto **webapp-form1**

Viendo la página index.jsp ¿Cómo debe llamarse el servlet?

## Cliente

Se proporciona la página index.jsp

![image](https://github.com/user-attachments/assets/ed4c8243-d89f-42e0-a943-df594ad64ca2)

## Servidor

Debemos de realizar las siguientes validaciones en el servidor (no el el cliente vía javascript o html5):

- el username es requerido.
- el password no puede ser vacío.
- el email es requerido y debe tener un formato de correo.
- debe seleccionar un idioma.

Debemos devolver una página html para informar al usuario.

![image](https://github.com/user-attachments/assets/72b6f8b9-8d71-4bab-bfc1-5ae4e821d4c0)

Si se ha rellenado correctamente el formulario, el servlet debe devolver esta página html:

![image](https://github.com/user-attachments/assets/c5fa1216-f499-4fb5-9758-9494aa1b40a9)

# FASE II: Recoger datos de un formulario (Servlet + JSP)

Vamos a mejorar la aplicación separando la creación del html de salida del código java del Servlet.

Java Server Pages (JSP) es una tecnología que se utiliza para desarrollar páginas web insertando Java código en las páginas HTML mediante la creación de etiquetas JSP especiales. 

Las etiquetas JSP que permiten java El código que se incluirá en él es <% —-java código—-%>

