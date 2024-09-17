# Ejemplo Servlet con pasos de parámetros por Get

![image](https://github.com/user-attachments/assets/1b69c449-e8c6-4c98-a3a4-ac0f7554de89)

## Código de ayuda:

**En el servlet:**

```
  // Entrada
  String param = request.getParameter("saludo");

  // Salida
  out.println("       <h2>El saludo enviado es:"+param+"</h2>");
```

**En la página html**

```
    <h1>Mi primera app web</h1>
    <p>Ejemplo 1: <a href="hola-mundo">Ejecutar el Servlet Hola Mundo</a></p>
    <p>Ejemplo 2: <a href="url-get?saludo=Hola caracola">Ejecutar el ParamsGetServlet (url-get?saludo=Hola caracola)</a></p>

```

## Ampliación

Añadir el código necesario al sevlet para gestionar recibir un nuevo parámetro llamado codigo que contendrá un valor numérico.

**Pista:** observa la diferencia entre los métodos parseInt y valueOf de Integer

### Página html de prueba (cliente)

![image](https://github.com/user-attachments/assets/78e7f914-5aa0-4e48-b7aa-406b3af458e1)

¿Qué es url-get2?

### Página html (respuesta del servlet)

![image](https://github.com/user-attachments/assets/2bb4e36f-368c-41df-a891-7a930659c768)





