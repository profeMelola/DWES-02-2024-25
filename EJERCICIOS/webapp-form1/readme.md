# FASE I: Recoger datos de un formulario (Servlet + salida html con PrintWriter)

Vamos a aprender a leer los parámetros enviados desde un formularios.

Usaremos nuestra primera página JSP que se proporciona en este repositorio.

Creamos nuestro proyecto desde **Eclipse Starter** y llamaremos a nuestro proyecto **webapp-form1**:

![image](https://github.com/user-attachments/assets/ffa107a3-6d16-49eb-94e1-a21c9518ff45)

Viendo la página index.jsp ¿Cómo debe llamarse el servlet?

La estructura del proyecto completa, con el jsp y servlet debería quedar así:

![image](https://github.com/user-attachments/assets/352ef533-6af8-4561-8883-eab8674cee27)

## Cliente

Se proporciona la página index.jsp

![image](https://github.com/user-attachments/assets/ed4c8243-d89f-42e0-a943-df594ad64ca2)


Para poder acceder a dicha página JSP a través del navegador necesito indicar en la url la ruta completa porque si no da el siguiente error:

![image](https://github.com/user-attachments/assets/c2901b64-dbc3-42a2-8e12-373d5d64fce6)

La ruta completa sería: http://localhost:8080/webapp-form1/index.jsp

Esto es debido, a que los proyectos generados con el Eclipse Starter tienen una directiva de bienvenida en el **archivo de configuración web.xml**

![image](https://github.com/user-attachments/assets/dd44f77c-5066-4f3f-aca6-767bfac31783)


En Jakarta EE 10, el uso del archivo web.xml no es obligatorio gracias a las anotaciones, pero sigue siendo una opción válida si prefieres centralizar configuraciones o si tienes necesidades específicas.


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

# FASE II: Recoger datos de un formulario (Servlet + JSP) -> Práctica guiada

Vamos a mejorar la aplicación separando la creación del html de salida del código java del Servlet.

Java Server Pages (JSP) es una tecnología que se utiliza para desarrollar páginas web insertando Java código en las páginas HTML mediante la creación de etiquetas JSP especiales. 

Las etiquetas JSP que permiten java El código que se incluirá en él es <% —-java código—-%>

En el caso de que haya errores en el formulario, se redigirá la salida desde el servlet a una página JSP:

```
  req.setAttribute("errores", errores);
  getServletContext().getRequestDispatcher("/index.jsp").forward(req, resp);
```

Utilizaremos en el Sevlet una colección Map para indicar el campo del formulario y la descripción del error. Por ejemplo:

```
  Map<String, String> errores = new HashMap<>();

  if (username == null || username.isBlank()) {
      errores.put("username", "el username es requerido!");
  }
```

Ese Map lo utilizaré en la página jsp para pintar los errores. Esta será la página html resultado:

![image](https://github.com/user-attachments/assets/0a67533c-6896-4ffb-88d1-3fd5f634376e)

Haz una copia de la página index.html y guárdala como index.jsp. Sigue las instrucciones del profesor para añadir las etiquetas JSP pertinentes.


