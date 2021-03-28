---
title: exp-vs
description: Fournit une valeur double exponentielle de précision complète. | exp-vs
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992077"
---
# <a name="exp---vs"></a>exp-vs

Fournit une précision complète de 2<sup>x</sup>.

## <a name="syntax"></a>Syntaxe



| exp heure d’été, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié. Consultez [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| exp                    | x    | x    | x    | x     | x    | x     |



 

Cette instruction fournit au moins 21 bits de précision.

Le fragment de code suivant montre les opérations effectuées :


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




