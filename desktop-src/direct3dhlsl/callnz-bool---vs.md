---
title: callnz bool-vs
description: Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. | callnz bool-vs
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a6d5a7646670d182b0b685ab742fb5b2094a89a717a31019165054bcbc4816b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287257"
---
# <a name="callnz-bool---vs"></a>callnz bool-vs

Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.

## <a name="syntax"></a>Syntaxe



| callnz l \# , \[ ! \] p\# |
|----------------------|



 

où :

-   où l \# est une [étiquette, et](label---vs.md) qui marque le début de la sous-routine à appeler.
-   \[!\] est le modificateur Boolean facultatif facultatif.
-   b \# identifie un [Registre booléen constant](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| callnz bool            |      | x    | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :


```
if (specified boolean register is not zero)
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

 

 




