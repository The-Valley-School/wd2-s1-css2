Llega el momento de poner en práctica lo aprendido, para ello, vamos a hacer un menú que podríamos usar en cualquier web:

![gif1.gif](recursos/gif1.gif)

Empezamos creando la estructura HTML:

```html
<header class="header">
    <nav class="menu">
        <ul class="menu-list">
            <li><a href="#">Sección 1</a></li>
            <li><a href="#">Sección 2</a></li>
            <li><a href="#">Sección 3</a></li>
            <li><a href="#">Sección 4</a></li>
        </ul>
    </nav>
</header>
```

Tras ello, diseñamos la clase header, utilizando el `hover` para cambiar el tamaño.

```css
body{
    background-color: linen;
    font-family: sans-serif;
    letter-spacing: 2px;
    margin: 0;
    padding: 0;
}

.header{
    position: fixed;
    bottom: 0;
    width: 85px;
    height: 100%;
    background-color: darkslateblue;
}

.header:hover{
    width: 300px;
}
```

A continuación maquetamos los elementos del listado para adaptarlos al estilo:

```css
.menu-list{
    padding: 0;
    list-style: none;
    font-weight: lighter;
    font-size:22px;
    overflow: hidden;
}

.menu-list a{
    color: white;
    text-decoration: none;
    padding: 10px;
    display: flex;
    align-items: center;
}

.menu-list li{
    min-width: 300px;
    padding: 0 10px;
}

.menu-list li:hover{
    background-color: lightgreen;
    font-weight: normal;
}
```

Y por último añadimos el icono usando el pseudo-elemento ::before:

```css
.menu-list a::before{
    content: url("https://img.icons8.com/ios/30/ffffff/checked--v1.png");
    margin-right: 35px;
}
```

---

[Solución Ejercicio](recursos/menu.zip)
