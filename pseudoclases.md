Una **pseudo-clase CSS** es una palabra clave que se añade a los selectores y que especifica un estado especial del elemento seleccionado. 

Las pseudo-clases hacen referencia a los comportamientos que pueden tener algunos elemento del HTML y nos sirven para darles estilos según su estado o comportamiento en cada momento, por ejemplo, cuando pasamos por encima de cierto elemento con el ratón, hacemos click o visitamos un enlace. 

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

Aplica estilos cuando un elemento es activado, es decir, cuando se pulsa sobre él. Se suele utilizar al clickar botones y enlaces.

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

Para aplicar estilos cuando hacemos foco en un elemento del formulario.

```css
/* El campo ha ganado el foco */
input:focus {
  border: 10px solid pink;
}
```

### :checked

Se suele utilizar también en formularios para aplicar estilos cuando la casilla esté seleccionada

```css
input:checked + span {
  color: green;
}
```

### :enabled | :disabled

También se usa en formularios. Con HTML tenemos la opción de añadir el atributo disabled a un elemento y así lo inhabilitamos.

```css
input:enabled {
  border: 10px solid pink;
}

input:disabled {
  border: 10px solid blue;
}
```

### :required | :optional

Del mismo modo, tenemos el atributo required para inputs obligatorios, si no lo añadimos, por defecto son opcionales. Con esta pseudo clase podemos aplicar estilos para diferenciar estos dos tipos de inputs.

```css
input:required {
  border: 10px solid pink;
}

input:optional {
  border: 10px solid blue;
}
```

### :invalid | :valid

Sirve para aplicar estilos cuando se cumple o no se cumple una determinada condición del input.

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

Para aplicar estilos cuando estén fuera o dentro de un rango.

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

Para seleccionar todos los elementos que no cumplen con el argumento (lo que hay entre paréntesis) de la pseudo-clase.

 
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
