---
title: SinCos,-PS
description: Calcule le sinus et le cosinus, en radians. | SinCos,-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95f61c3a1cfc15f699e0e637dce8d58b9517ffe58ef36e529ec297661bff6a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671569"
---
# <a name="sincos---ps"></a>SinCos,-PS

Calcule le sinus et le cosinus, en radians.

## <a name="syntax"></a>Syntaxe

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 et PS \_ 2 \_ x



| SinCos, DST. x|y|XY}, src0. x|y|Lettre|w}, src1, src2 |
|------------------------------------------------------|



 

Où :

-   l’heure d’été est le registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.
-   src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] . {x \| y \| z \| w} est le Swizzle de réplication requis.
-   src1 et src2 sont des registres sources et doivent être deux [registres de type flottant](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) différents. Les valeurs de src1 et src2 doivent être celles des macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) et [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) , respectivement.

### <a name="ps_3_0"></a>PS \_ 3 \_ 0



| SinCos, DST. x|y|XY}, src0. x|y|Lettre|s |
|------------------------------------------|



 

Où :

-   l’heure d’été est un registre de destination et doit être un [Registre temporaire](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ). Le registre de destination doit avoir exactement l’un des trois masques suivants :. x. \| y. \| XY.
-   src0 est un registre source qui fournit l’angle d’entrée, qui doit être compris entre \[ -pi, + pi \] . {x \| y \| z \| w} est le Swizzle de réplication requis.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| SinCos,                |      |      |      |      | x    | x    | x     | x    | x     |



 

### <a name="ps_2_0-and-ps_2_x"></a>PS \_ 2 \_ 0 et PS \_ 2 \_ x

Pour PS \_ 2 \_ 0 et PS \_ 2 \_ x, SinCos, peut être utilisé avec un prédicat, mais avec une seule restriction au Swizzle du [Registre de prédicats](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0) : la seule réplication de Swizzle (. x.y. \| \| z \| ) est autorisée.

Pour PS \_ 2 \_ 0 et PS \_ 2 \_ x, l’instruction fonctionne comme suit (V = la valeur scalaire de src0 avec un Swizzle de réplication) :

-   Si le masque d’écriture est. x :
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. y :
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. XY :
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a>PS \_ 3 \_ 0

Pour PS \_ 3 \_ 0, SinCos, peut être utilisé avec un prédicat sans aucune restriction. Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).

Pour PS \_ 3 \_ 0, l’instruction fonctionne comme suit (V = la valeur scalaire de src0 avec un Swizzle de réplication) :

-   Si le masque d’écriture est. x :
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. y :
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   Si le masque d’écriture est. XY :
    ```
    dest.x = cos(V)
    dest.y = sin(V)
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

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
