---
title: Journal-PS
description: Full Precision log ₂ (x). | Journal-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974387"
---
# <a name="log---ps"></a>Journal-PS

Full Precision log ₂ (x).

## <a name="syntax"></a>Syntaxe



| DST du journal, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués ; autrement dit, exactement l’un des composants. x,. y,. z et. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| journal                   |      |      |      |      | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre les opérations effectuées.


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

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




