---
title: callnz bool-PS
description: Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. | callnz bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 793feb1934b86b46f26050a67b5f26d94b9f277e31735c4d1912805374bab903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118516625"
---
# <a name="callnz-bool---ps"></a>callnz bool-PS

Appelez si la valeur n’est pas égale à zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette.

## <a name="syntax"></a>Syntaxe



| callnz l \# , \[ ! \] p\# |
|----------------------|



 

Où :

-   l \# est une [étiquette-PS](label---ps.md) qui marque le début de la sous-routine à appeler.
-   \[!\] est un modificateur de négation facultatif.
-   b \# identifie un [Registre booléen constant](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz bool           |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




