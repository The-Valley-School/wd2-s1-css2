Al igual que las pseudoclases, los pseudoelementos se añaden a los selectores. Estos no hacen referencia a un estado especial si no que sirven para añadir estilos a una parte concreta del documento.

La sintaxis es la siguiente:

```css
CLASE::PSEUDOELEMENTO {
    PROPIEDAD: VALOR;
}
```

Mediante esta sintaxis estamos creando y dando estilo a un elemento virtual en el DOM.

A lo largo del vídeo hemos tratado los pseudoelementos más importantes:

- ::after
- ::before

También os dejamos una lista completa de todos:

> https://developer.mozilla.org/es/docs/Web/CSS/Pseudoelementos


### ::after

La propiedad **::after** creará un  pseudoelemento que  se posicionará como el **último hijo** del elemento al que apliquemos dicha propiedad, pudiendo así añadir estilos justo después del elemento.

### ::before

La propiedad **::bejore** creará un  pseudoelemento que  se posicionará como el **primer hijo** del elemento al que apliquemos dicha propiedad, pudiendo así añadir estilos justo antes del elemento.

### **PROPIEDAD CONTENT**

Utilizaremos la propiedad content para añadir contenido sobre los pseudoelementos que hemos creado.

Podemos usarlo para indicar el inicio y final de una cita, poner emoticonos en listas…

**Ejemplo lista**

```html
<ul>
  <li>Peras</li>
  <li>Huevos</li>
  <li>Leche</li>
  <li>Carne</li>
  <li>Pescado</li>
</ul>
```

 

```css
ul {
  list-style: none;
}

li::before{
  content: '✅ ';
}
```

 

**Ejemplo cita**

 

```html
Rambo dijo <span>no siento las piernas.</span>
```

 

```css
span::before {
  content: "«";
}

span::after {
  content: "»";
}
```
