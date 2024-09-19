# Jakarta Sever Pages. JSP

![image](https://github.com/user-attachments/assets/fd2fe72d-70bc-471f-91c2-828f78814445)

https://jakarta.ee/specifications/pages/

## 1. Directivas
Las directivas proporcionan información sobre el contenido de la página JSP y afectan el procesamiento de la página.

### Page Directive: Define atributos que afectan el comportamiento de la página completa.

```
<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8" %>
```

- language: El lenguaje utilizado, típicamente "java".
- contentType: El tipo de contenido de la respuesta, por ejemplo, "text/html".
- pageEncoding: La codificación de caracteres usada en la página.

### Include Directive: Incluye el contenido de un archivo en la página actual en tiempo de compilación.

```
<%@ include file="header.jsp" %>
```

### Taglib Directive: Declara bibliotecas de etiquetas personalizadas.

```
<%@ taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core" %>
```

## 2. Scripting Elements
Son fragmentos de código Java que se insertan en una página JSP.

### Declarations: Definen variables y métodos que pueden ser usados en toda la página.

<%! 
  int add(int a, int b) {
    return a + b;
  }
%>

### Scriptlets: Código Java que se ejecuta en tiempo de solicitud.

```
<% 
  String name = "Mundo"; 
  out.println("Hola, " + name);
%>
```

### Expressions: Expresiones Java que se evalúan y se insertan directamente en el flujo de salida.

```
<%= new java.util.Date() %>
```

## 3. Declaración de Objetos Implicitos: JSP proporciona objetos implícitos para interactuar con la solicitud, respuesta, sesión y contexto de aplicación:

- **request:** Representa la solicitud del cliente.
- **response:** Representa la respuesta al cliente.
- **session:** Representa la sesión del usuario.
- **application:** Representa el contexto de la aplicación.
- **out:** Representa el objeto de escritura de la respuesta.
- **config:** Representa la configuración del servlet.
- **pageContext:** Proporciona un contexto de página más amplio.