En anteriores vídeos hemos visto una serie de selectores básicos que nos ayudaban a aplicar estilos a nuestro HTML. 

- Selectores de ID
- Selectores por clase
- Selectores por elemento
- ….

En este video vamos a segur avanzando con ellos y profundizando en la relación entre etiquetas.

### *

Este selector hace referencia a todos los elementos y puede combinarse con el resto de selectores. Por ejemplo, si queremos seleccionar todos los elementos que contentan una clase específica, lo haríamos de la siguiente manera:

  

```css
* .clase-especifica {
	/* estilos que queramos aplicar */
}
```

 

### ADYACENTES

Seleccionamos el elemento adyacente. 

  

```css
.titulo-a + .titulo-b{
	/* estilos que queramos aplicar */
}
```

En el ejemplo propuesto seleccionaríamos el elemento con la clase **.titulo-b** que se encuentre justamente después de la clase **.titulo-a**

### TODOS LOS POSTERIORES

Seleccionamos todos los posteriores

  

```css
.titulo-a ~ .titulo-b{
	/* estilos que queramos aplicar */
}
```

En el ejemplo propuesto seleccionaríamos todos los elementos con la clase **.titulo-b** que se encuentren  después de la clase **.titulo-a**

### COMPUESTOS

Si por ejemplo ponemos dos clases sin espacio entre ellas estaremos haciendo referencia a clases hermanas que se encuentran en un mismo elemento.

 

```css
.titulo-a.titulo-b{
	/* estilos que queramos aplicar */
}
```

 

### HIJOS DIRECTOS

Lo usamos para seleccionar todos los hijos directos

 

```css
div > h1{
	/* estilos que queramos aplicar */
}
```

 

En este caso estaríamos seleccionando todos títulos h1 dentro de un contenedor div.

### PRIMER HIJO, ÚLTIMO HIJO….

Existen también reglas y selectores para poder modificar ciertos elementos dentro de una jerarquía, por ejemplo dentro de un listado:

 

```css
li:lastChild{
	/* estilos que queramos aplicar */
}

li:nthChild(3){
	/* estilos que queramos aplicar */
}
```

 

> https://developer.mozilla.org/es/docs/Web/CSS/:nth-child

### ATRIBUTOS

También podemos usar selectores CSS basados en atributos HTML.

```css
a[href="https://www.thevalley.es"] {
  color: green;
}
```

Os dejamos también acceso a la documentación donde podréis ampliar conocimientos de cara a los selectores:

> https://developer.mozilla.org/es/docs/Web/CSS/CSS_Selectors