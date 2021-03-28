---
title: callnz prédit-vs
description: Appelez si la valeur est différente de zéro, avec un prédicat. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104030580"
---
# <a name="callnz-pred---vs"></a>callnz prédit-vs

Appelez si la valeur est différente de zéro, avec un prédicat. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.

## <a name="syntax"></a>Syntaxe



| callnz l \# , \[ ! \] P0. x|y|Lettre|s |
|----------------------------------|



 

où :

-   l \# est une [étiquette, vs](label---vs.md) marquant le début de la sous-routine à appeler.
-   \[!\] est un modificateur de négation facultatif.
-   P0 correspond au [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} est le Swizzle de réplication requis sur P0.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| callnz prévu            |      |      | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



Cette instruction consomme un emplacement d’instruction de nuanceur de sommets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




