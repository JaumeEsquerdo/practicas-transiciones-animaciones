# practicas-transiciones-animaciones

## Transiciones

Ejemplo básico

```css

.Body{
    transition: background 300ms linear 0; 
    /* el 0 es del delay */ /* animación final */
    }

.Body:hover{
    background: blue;
    transition-duration: 500ms; /* primera animación*/
}

``` 

Con `KEYFRAMES`

```css
.pulser{
    width: 55px;
    position:relative;
    animation: move;
    animation-duration: 2s;
}

.pulser::after{
    position: absolute;
    top: 0;
    left:0;
    width: 100%;
    animation: pulse 1s ease;
    animation-delay: 5s;
    animation-iteration-count: 5; /* para repetir la animacion, en este caso 5 veces */

    /* animation-iteration-count: infinite; */
}

@keyframes move {
    from {
        transform: translateY(0px);
    }
    to {
        transform: translateY(100px);
    }
}


@keyframes pulse {
    0% {
        opacity : 0;

    }
    50%{
        scale: 1.4;
        opacity: .4;
    }
}


animation-fill-mode:forwards; /* PARA QUE SE QUEDE EN SU POSICIÓN FINAL QUE LE HEMOS MANDADO, AL ACABAR LA ANIMATION */

animation-fill-mode: both; /* Para que se al principio esté en el sitio inicial y al final en la del final. ESTE SE UTILIZA MUCHO */

/*  ejemplo de animations */

.main{
    animation: pulse 1s steps(10) infinite both,
    mover 1s linear 2s both; /*  le ponemos un delay para que no lo haga todo a la vez */
}


```
