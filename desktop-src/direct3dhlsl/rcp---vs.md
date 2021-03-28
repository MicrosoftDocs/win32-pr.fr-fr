---
title: RCP-vs
description: Calcule la réciproque du scalaire source. | RCP-vs
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974383"
---
# <a name="rcp---vs"></a>RCP-vs

Calcule la réciproque du scalaire source.

## <a name="syntax"></a>Syntaxe



| RCP DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| rcp                    | x    | x    | x    | x     | x    | x     |



 

Le fragment de code suivant montre les opérations effectuées.


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



La sortie doit être exactement 1,0 si l’entrée est exactement 1,0. Une source de 0,0 donne l’infini.

La précision doit être d’au moins 1,0/(2 ² ²) erreur absolue sur la plage (1,0, 2,0), car les implémentations courantes séparent la mantisse et l’exposant.

Si la source n’a aucun sous-script, le composant x est utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




