---
title: ENDLOOP-vs
description: Fin d’une boucle... bloc ENDLOOP.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cdd9158d12ecc29073526833a7a4ca5eec03100558a9ebdc711822c7ca74c9bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949889"
---
# <a name="endloop---vs"></a>ENDLOOP-vs

Fin d’une [boucle](loop---vs.md)... bloc ENDLOOP.

## <a name="syntax"></a>Syntaxe



| ENDLOOP |
|---------|



 

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| ENDLOOP                |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme indiqué ici.


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



ENDLOOP doit suivre la dernière instruction d’un bloc [Loop-vs](loop---vs.md) .

## <a name="example"></a>Exemple


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




