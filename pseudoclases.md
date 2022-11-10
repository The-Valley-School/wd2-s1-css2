Una **pseudo-clase CSS** es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. Las pseudo-clases hacen referencia a los comportamientos que pueden tener algunos elementos de HMTL y nos sirven para darles estilos respecto según el comportamiento en cada momento (pasar por encima de cierto elemento con el ratón, hacer click, visitar un enlace…) 

En este video vamos a hablar de pseudo-clases. Las pseudo-clases hacen referencia a los comportamientos que pueden tener algunos elementos de HMTL y nos sirven para darles estilos respecto según el comportamiento en cada momento (pasar por encima de cierto elemento con el ratón, hacer click, visitar un enlace…) 

La sintaxis es la siguiente:

 

```css
CLASE:PSEUDOCLASE {
    PROPIEDAD: VALOR;
}
```

 

### :link

Se trata de una pseudo-clase para enlaces la cual aplica estilos a enlaces que todavía no se han visitado.

 

```css
a:link {
  color: green;
}
```

  

### :visited

Si la pseudo-clase link hacía referencia a enlaces no visitados, la pseudo-clase visited hace referencia a aquellos que sí se han visitado.

 

```css
a:visited {
  color: red;
}
```

  

### :hover

La pseudo-clase hover nos sirve para poder aplicar estilos cuando pasamos con el ratón por encima de un elemento.

 

```css
a:hover {
	font-weigth: bold;
	font-size: 25px;
}
```

 

### :active

La pseudo-clase active nos sirve para poder aplicar estilos cuando un elemento es activado, es decir, cuando se pulsa sobre él. Suele ser aplicado a botones y enlaces.

```css
button {
	padding: 5px;
	background-color: blue;
	color:white;
}

button:active {
	background-color: red;
}
```

 

### :focus

La pseudo-clase focus aplica estilos cuando hacemos foco en el elemento.

```css
/* El campo ha ganado el foco */
input:focus {
  border: 10px solid pink;
}
```

 

### :checked

Utilizado también en formularios, podemos aplicar estilos cuando la casilla esté seleccionada

```css
input:checked + span {
  color: green;
}
```

### :enabled | :disabled

Los utilizamos en formularios. En HTML tenemos la opción de añadir el atributo disabled a un elemento y así lo desactivamos.

```css
input:enabled {
  border: 10px solid pink;
}

input:disabled {
  border: 10px solid blue;
}
```

### :required | :optional

Del mismo modo, tenemos el atributo de required en formularios, por defecto si no son opcionales.

```css
input:required {
  border: 10px solid pink;
}

input:optional {
  border: 10px solid blue;
}
```

### :invalid | :valid

Para aplicar estilos cuando cumplen o no cumplen la condición

```html
<input type="text" name="edad" pattern="[0-9]+">
```

```css
input:invalid {
	color:red;
}

input:valid {
	color:green;
}
```

### :**out-of-range** | :**in-range**

Para aplicar estilos cuando estén fuera o dentro de rango

 

```html
<input type="number" name="edad" min="0" max="18">
```

```css
input:out-of-range {
	color:red;
}

input:in-range {
	color:green;
}
```

### :not

Para seleccionar todos los elementos que no cumplan lo que hay entre paréntesis.

 

```html
<p class="parrafo-principal">Párrafo principal</p>
<p>Párrafo</p>
<p>Párrafo</p>

```

```css
p:not(.parrafo-principal) {
 color:grey;
}
```