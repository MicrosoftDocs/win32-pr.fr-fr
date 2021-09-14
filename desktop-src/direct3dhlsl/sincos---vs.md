---
title: SinCos,-vs
description: Calcule le sinus et le cosinus, en radians. | SinCos,-vs
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232254"
---
# <a name="sincos---vs"></a>SinCos,-vs

Calcule le sinus et le cosinus, en radians.

## <a name="syntax"></a>Syntaxe

### <a name="vs_2_0-and-vs_2_x"></a>vs \_ 2 \_ 0 et vs \_ 2 \_ x



| SinCos, DST. x|y|XY}, src0. x|y|Lettre|w}, src1, src2 |
|------------------------------------------------------|



 

Où :

-   l’heure d’été est le registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.
-   src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] . {x \| y \| z \| w} est le Swizzle de réplication requis.
-   src1 et src2 sont des registres sources et doivent être des registres à [virgule flottante constantes](dx9-graphics-reference-asm-vs-registers-constant-float.md) différents (c \# ). Les valeurs de src1 et src2 doivent être celles des macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) et [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivement.

### <a name="vs_3_0"></a>vs \_ 3 \_ 0



| SinCos, DST. x|y|XY}, src0. x|y|Lettre|s |
|------------------------------------------|



 

Où :

-   l’heure d’été est un registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ). Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.
-   src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] . {x \| y \| z \| w} est le Swizzle de réplication requis.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| SinCos,                 |      | x    | x    | x     | x    | x     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a>Remarques sur vs \_ 2 \_ 0 et vs \_ 2 \_ x

Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, SinCos, peut être utilisé avec un prédicat, mais avec une restriction au Swizzle du registre de [prédicats](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0) : seule la réplication de Swizzle (. x.y. \| \| z \| ) est autorisée.

Pour vs \_ 2 \_ 0 et vs \_ 2 \_ x, l’instruction fonctionne comme suit : (V = la valeur scalaire de src0 avec un Swizzle de réplication) :

-   Si le masque d’écriture est. x :
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. y :
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. XY :
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a>Remarques sur vs \_ 3 \_ 0

Pour vs \_ 3 \_ 0, SinCos, peut être utilisé avec un prédicat sans aucune restriction. Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).

Pour vs \_ 3 \_ 0, l’instruction fonctionne comme suit : (V = la valeur scalaire de src0 avec un Swizzle de réplication)

-   Si le masque d’écriture est. x :
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. y :
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. XY :
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

L’application peut mapper un angle arbitraire (en radians) à la plage \[ -pi, + pi \] en utilisant le pseudocode de nuanceur suivant :


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
