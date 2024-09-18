# Ejemplo Servlet con pasos de parámetros por Get

## Página index.html

![image](https://github.com/user-attachments/assets/77665391-86b5-4522-a3f2-2e78ca8da99b)

## Diferentes páginas html resultado

**Si el código es superior a 100:**

![image](https://github.com/user-attachments/assets/1656e969-404e-46dc-9932-d23f4e52a41f)

**Si el código no es superior a 100:**

![image](https://github.com/user-attachments/assets/6cd252ef-1a1a-4b6d-9a51-df2a244eb56d)


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
    <p><a href="url-get?saludo=Hola caracola">Ejecutar el ParamsGetServlet (url-get?saludo=Hola caracola)</a></p>
    <p><a href="url-get?saludo=Hola&nombre=melola&codigo=666">Ejecutar el ParamsGetServlet con 3 params(url-get?saludo=Hola&nombre=melola&codigo=666)</a></p>
    <p><a href="url-get?saludo=Hola&nombre=melola&codigo=66">Ejecutar el ParamsGetServlet con 3 params(url-get?saludo=Hola&nombre=melola&codigo=66)</a></p>
```

## Ampliación

Añadir el código necesario al sevlet para gestionar recibir un nuevo parámetro llamado codigo que contendrá un valor numérico.

**Pista:** observa la diferencia entre los métodos parseInt y valueOf de Integer

### Página html de prueba (cliente)

![image](https://github.com/user-attachments/assets/78e7f914-5aa0-4e48-b7aa-406b3af458e1)

¿Qué es url-get2?

### Página html (respuesta del servlet)

![image](https://github.com/user-attachments/assets/2bb4e36f-368c-41df-a891-7a930659c768)





