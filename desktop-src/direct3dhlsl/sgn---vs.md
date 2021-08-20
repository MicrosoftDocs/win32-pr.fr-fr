---
title: SGN-vs
description: Calcule le signe de l’entrée.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1a4994c807ff1df99016aad734edf71e5e1ce6efe59fd53a4fb9bb3ee91a4b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671679"
---
# <a name="sgn---vs"></a>SGN-vs

Calcule le signe de l’entrée.

## <a name="syntax"></a>Syntaxe



| SGN DST, src0, src1, src2 |
|---------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre temporaire qui contient les résultats intermédiaires. Après l’exécution, le contenu n’est pas défini.
-   src2 est un registre temporaire qui contient les résultats intermédiaires. Après l’exécution, le contenu n’est pas défini.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| SGN                    |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme indiqué ci-dessous.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 et src2 doivent être des [registres temporaires](dx9-graphics-reference-asm-vs-registers-temporary.md)différents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




