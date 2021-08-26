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
ms.openlocfilehash: 2b5b27067e83cbfd7604165ec1191d3371634aac15781a719377c92c69e29e6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067949"
---
# <a name="exp---vs"></a>exp-vs

Fournit une précision complète de 2<sup>x</sup>.

## <a name="syntax"></a>Syntaxe



| exp heure d’été, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié. Consultez [Registre source Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).

## <a name="remarks"></a>Remarques



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

 

 




