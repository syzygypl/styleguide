# Using `id`s to reference DOM nodes

Nie używamy `id` jako hooków w JS bo:

1. Nie możemy zagwarantować, że id się nie zmieni - *bardziej w przypadku sekcji, itp. gdzie klient chce mieć kotwice i nie podobają się mu teksty*. Ale jako, że wartości `id` nie są wyłącznie po naszej stronie to dla zasady nie używamy ich w JS.

2. Nie widać na pierwszy rzut oka w templatce, że jest ona powiązana z jakimś JS-em.

3. Ograniczamy nasz JS w ten sposób do jednego konkretnego Use Case'u — nie jesteśmy w stanie użyć danego komponentu w wielu różnych miejscach.

--- 

Zamiast id jako hooków w JS używamy atrybutów data-*. Czyli np.

```html
<div class="modal" id="newletter-form" data-auto-modal>…</div>
```
