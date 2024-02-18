# At-rules

* Está relacionado ao comportamento do CSS
* Começa com o sinal de `@` seguido do identificador e o valor

## Exemplos comuns

- @import /* incluir um CSS externo */
- @media /* regras condicionais para dispositivos */
- @font-face /* fontes externas */
- @keyframes /* animation */

```CSS
@import url("http://local.com/style.css");

@media (min-width:500px) {
    /* rules here */
}

@fonte-face {
    /* rules here */
}

@keyframes nameofanimation {
    /* rules here */
}
```