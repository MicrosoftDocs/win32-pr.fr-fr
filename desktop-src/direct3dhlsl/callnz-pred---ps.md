---
title: callnz prédit-PS
description: Appelez avec un prédicat, si différent de zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103940565"
---
# <a name="callnz-pred---ps"></a>callnz prédit-PS

Appelez avec un prédicat, si différent de zéro. Effectue un appel conditionnel à l’instruction marquée par l’index d’étiquette. La prédicat utilise une valeur booléenne pour déterminer si l’instruction ne doit pas être exécutée.

## <a name="syntax"></a>Syntaxe



| callnz l \# , \[ ! \] P0. x|y|Lettre|s |
|----------------------------------|



 

Où :

-   où l \# est une [étiquette-PS](label---ps.md) marque le début de la sous-routine à appeler.
-   \[!\] est un modificateur de négation facultatif.
-   P0 correspond au registre de prédicat. Consultez [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} est le Swizzle de réplication requis sur P0.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| callnz prévu           |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction effectue les opérations suivantes :


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




