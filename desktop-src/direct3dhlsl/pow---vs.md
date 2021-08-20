---
title: Pow-vs
description: Src0 (Full Precision ABS) src1. | Pow-vs
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3fd6c40ef133782990cc8f10517d51a723a21e0730bfabd83feca4c7e294cb7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088665"
---
# <a name="pow---vs"></a>Pow-vs

Src0 (Full Precision ABS)<sup>src1</sup>.

## <a name="syntax"></a>Syntaxe



| Pow DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre de la source d’entrée. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.
-   src1 est un registre de la source d’entrée. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| pow                    |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme indiqué ici.


```
dest = pow(abs(src0), src1);
```



Il s’agit d’une instruction scalaire. par conséquent, les registres source doivent avoir répliqué Swizzles pour indiquer les canaux qui sont utilisés.

Le résultat scalaire est répliqué sur les quatre canaux de sortie.

Cette instruction peut être développée en tant que exp (src1 \* log (src0)).

La précision n’est pas inférieure à 15 bits.

Le registre de dest doit être un registre temporaire et ne doit pas être le même que src1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




