Antes de entrar a ver otros apartados de CSS como puede ser el responsive, vamos a ver una serie de trucos que nos pueden ser de gran ayuda a la hora de centrar elementos en CSS, tanto horizontal como verticalmente.

## CENTRANDO ELEMENTOS HORIZONTALMENTE

Uno de los retos que nos solemos encontrar a la hora de estilar una página web es la de centrar elementos horizontalmente. Hay muchas formas de llevarlos a cabo, vamos a ver unas cuantas:

### CENTRADO HORIZONTAL PARA BLOCKS

En caso de tener bloques podemos alinearlos de manera horizontal jugando con la propiedad margin y el valor auto del elemento. 

Puede ser de gran ayuda también a la hora de trabajar con imágenes siempre y cuando le añadamos la propiedad display:block;

 

```html
<div>
  <img src="https://ca-times.brightspotcdn.com/dims4/default/c3f4b96/2147483647/strip/true/crop/1970x1108+39+0/resize/1200x675!/quality/80/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2F12%2Fa5%2F79e097ccf62312d18a025f22ce48%2Fhoyla-recuento-11-cosas-aman-gatos-top-001">
</div>
```

   

```css
div {
  width: 1000px;
  heigth: 200px;
  background-color: red;
}

img{
  display: block;
  width: 100px;
  margin: 0 auto;
}
```

 

### CENTRADO HORIZONTAL PARA INLINE-BLOCKS

En caso de tener inline-block podemos alinearlos de manera horizontal jugando con la propiedad text-align, que aplica a multitud de elementos, no solo a texto. Lo que haremos será asignar esta propiedad al elemento padre:

 

```html
<div>
  <img src="https://ca-times.brightspotcdn.com/dims4/default/c3f4b96/2147483647/strip/true/crop/1970x1108+39+0/resize/1200x675!/quality/80/?url=https%3A%2F%2Fcalifornia-times-brightspot.s3.amazonaws.com%2F12%2Fa5%2F79e097ccf62312d18a025f22ce48%2Fhoyla-recuento-11-cosas-aman-gatos-top-001">
</div>
```

   

```css
div {
  width: 1000px;
  heigth: 200px;
  background-color: red;
  text-align: center;
}

img{
  width:100px;
}
```

 

## CENTRANDO ELEMENTOS VERTICALMENTE

Le toca el turnos al centrado vertical de elementos. Por lo general, no tendremos problemas con este tipo de centrados ya que normalmente cuando una página crece lo hace a lo ancho no a lo largo.

### MARGIN, PADDING

La forma más fácil de alinear elementos verticalmente es añadir un margin-top / margin-bottom al elemento central. Si lo preferimos podemos hacerlo añadiendo padding-top / padding-bottom al elemento padre.

 

```html
<div>
  <h1>HOLA</h1>
</div>
```

   

```css
div {
  background-color: red;
  width: 1000px;
  padding-top: 50px;
  padding-bottom: 50px;
}
```

 

## CENTRANDO ELEMENTOS VERTICALMENTE Y HORIZONTALMENTE

### POSITION

En muchas circunstancias necesitamos centrar tanto vertical como horizontalmente un elemento dentro de otro con medidas especificas, para ello, necesitamos especificar al padre el estilo postion:relative y agregar al hijo que queremos centrar estilos de posicionamiento absoluto:

```html
<div class="padre">
  <div class="hijo">
  </div>
</div>
```

```css
.padre {
  width: 1000px;
  height: 200px;
  position: relative;
  background-color: red;
}

.hijo {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  width: 100px;
  height: 100px;
  background-color: green;
}
```
