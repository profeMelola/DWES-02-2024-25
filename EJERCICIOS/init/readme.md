# Ciclo de vida: método init de un servlet

1. Crea un servlet y siguiendo el siguiente código haz la prueba realizando diferentes peticiones para ver el valor de la variable *peticiones*.

2. Mejora el código del método doGet utilizando *try con recursos.*

```
	//variable estara compartida por todas las peticiones
	private int peticiones;
   
	@Override
	public void init(ServletConfig config) throws ServletException {
		
		//configurar nuestro servlet con un valor inicial de 5
		peticiones= Integer.parseInt(config.getInitParameter("inicio"));
		
	}


	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		PrintWriter pw= response.getWriter();
		pw.println(peticiones);
		peticiones++;
		pw.close();
	}
```
