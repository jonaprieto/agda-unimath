# Products of binary relataions

```agda
module foundation.products-binary-relations where
```

<details><summary>Imports</summary>

```agda
open import foundation.binary-relations

open import foundation-core.cartesian-product-types
open import foundation-core.dependent-pair-types
open import foundation-core.propositions
open import foundation-core.universe-levels
```

</details>

## Idea

Given two relations `R` and `S`, their product is given by
`(R × S) (a , b) (a' , b')` iff `R a a'` and `S b b'`.

## Definition

### The product of two relations

```agda
module _
  {l1 l2 l3 l4 : Level}
  {A : UU l1} (R : Rel-Prop l2 A)
  {B : UU l3} (S : Rel-Prop l4 B)
  where

  prod-Rel-Prop :
    Rel-Prop (l2 ⊔ l4) (A × B)
  prod-Rel-Prop (a , b) (a' , b') =
    prod-Prop
      ( R a a')
      ( S b b')
```
