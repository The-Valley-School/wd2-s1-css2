Hemos visto en anteriores videos, que a un elemento se le pueden aplicar estilos de diferentes maneras y como consecuencia de ello, puede darse el caso en que se apliquen las mismas propiedades a través de diferentes selectores. Por ejemplo:

 

```html
<h1 class="titulo-especial">Título</h1>
```

   

```css
h1{
	color:green;
}

h1 .titulo-especial{
	color:red;
}
```

  

Para saber que  propiedad prevalecerá sobre el título utilizamos la **ESPECIFICIDAD** y así determinaremos el peso o fuerza que tiene cada una de estas reglas.

La especificidad de un selector se determina en base a un cálculo matemático de 4 componentes a los que asignamos un valor dependiendo del tipo de selector que tenga la regla.

> ESPECIFICIDAD ( A , B , C , D )
> 

- **A:** Estilos en línea, estilos aplicados mediante el atributo **style.** Suman 1000 (por desgracia)
- **B:** Cada **selector de ID.** Suman 100.
- **C**: Cada **selector de clase, pseudoclase** o atributo. Suman 10.
- **D**: Cada **selector de elemento o pseudoelemento.** Suman 1.

En el ejemplo anterior, la especificidad quedaría de la siguiente manera:

 

```css
h1 {}                        /* ESPECIFICIDAD: 0,0,0,1 */
h1 .titulo-especial {}       /* ESPECIFICIDAD: 0,0,1,1 */
```

  

Otros ejemplos:

 

```css
footer {}                    /* ESPECIFICIDAD: 0,0,0,1 */
footer a {}                  /* ESPECIFICIDAD: 0,0,0,2 */
#principal footer {}         /* ESPECIFICIDAD: 0,1,0,1 */
#principal footer:hover {}   /* ESPECIFICIDAD: 0,1,1,1 */
#principal footer:hover a{}  /* ESPECIFICIDAD: 0,1,1,2 */
```

 

Visual Studio Code nos proporciona también información sobre la especificidad y nos ayuda con ello.
