# A Cascata (cascading)

A escolha do broweser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* Seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo

inline > tag style > tag link

### Especificidade

É um cálculo matemática, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados (forças).

```
0. Universal selector, combinators e negation pseudo-class (:not())
1. Element type selector e pseudo-elements (::before, ::after)
10. Classes e atribbute selectors ([type="radio"])
100. ID Selector
1000. Inline
```

Exemplo:

```HTML
<h1 class="title" id="my-title">
    Título <strong>Teste</strong>
</h1>
```

```CSS
#my-title, #my,title strong {
    color: gray;
}
#my-title{
    color: gray; /* Força 100 */
}

.title {
    color:red; /* Força 10 */
}

body h1.title#my-title{
    color: blue; /* Força 112 */
}

* {
    color: green; /* Força 0 */
}
```

### A regra !important

* Evitar o uso
* Não é considerado uma boa prática
* Quebra o fluxo natural da cascata

Exemplo

```CSS
h1 {
    color: blue !important;
}
```