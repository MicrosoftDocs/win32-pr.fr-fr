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
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524856"
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

## <a name="remarks"></a>Notes



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

 

 




