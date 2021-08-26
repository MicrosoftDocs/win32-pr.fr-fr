---
title: expp-vs
description: Fournit une précision partielle 2x x2.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8717edc045f50cc572d675dbec405b01fda49503349e9716210dfcae23fb277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982449"
---
# <a name="expp---vs"></a>expp-vs

Fournit une précision partielle 2<sup>x</sup>.

## <a name="syntax"></a>Syntaxe



| expp DST, SRC. x|y|Lettre|s |
|----------------------------|



 

Où :

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.
-   {x \| y \| z \| w} est le Swizzle répliqué requis sur le registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| expp                   | x    | x    | x    | x     | x    | x     |



 

### <a name="vs_1_1"></a>vs \_ 1 \_ 1

L’instruction [exp-vs](exp---vs.md) fonctionne différemment selon les versions de nuanceur de sommets.

Dans vs \_ 1 \_ 1, l’instruction expp donne les résultats suivants :


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



Dans vs \_ 2 \_ 0 et vers le haut, l’instruction expp donne les résultats suivants :


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a>vs \_ 2 \_ 0

Dans vs \_ 2 \_ 0 et vers le haut, l’instruction fonctionne comme suit :


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



L’instruction fournit au moins 10 bits de précision.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




