---
title: journalisation-vs
description: Full Precision log ₂ (x). | journalisation-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104211524"
---
# <a name="log---vs"></a>journalisation-vs

Full Precision log ₂ (x).

## <a name="syntax"></a>Syntaxe



| DST du journal, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| journal                    | x    | x    | x    | x     | x    | x     |



 

Le fragment de code suivant montre les opérations effectuées.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Cette instruction accepte une source scalaire dont le bit de signe est ignoré. Le résultat est répliqué sur les quatre canaux.

Cette instruction fournit 21 bits de précision.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




