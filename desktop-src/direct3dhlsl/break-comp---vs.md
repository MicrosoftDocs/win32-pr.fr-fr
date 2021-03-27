---
title: break_comp-vs
description: Décomposer de manière conditionnelle de la boucle actuelle à l’instruction ENDLOOP-vs ou endrep-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103841665"
---
# <a name="break_comp---vs"></a>arrêt \_ COMP-vs

Décomposer de manière conditionnelle de la boucle actuelle à l’instruction [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md).

## <a name="syntax"></a>Syntaxe



| arrêter \_ COMP src0, src1 |
|------------------------|



 

Où :

-   \_COMP est une comparaison entre les deux registres sources. Les valeurs possibles sont les suivantes : 

    | Syntaxe | Comparaison            |
    |--------|-----------------------|
    | \_TB   | Supérieur à          |
    | \_terme   | Inférieur à             |
    | \_&   | Supérieur ou égal à |
    | \_WinINSTALL   | Inférieur ou égal à    |
    | \_EQ   | Égal à              |
    | \_ne   | Différent de          |

    

     

-   src0 est un registre source. La réplication de Swizzle est requise pour sélectionner un composant unique.
-   src1 est un registre source. La réplication de Swizzle est requise pour sélectionner un composant unique.

## <a name="remarks"></a>Notes

Cette instruction est prise en charge dans les versions suivantes.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| arrêter la \_ COMP.            |      |      | x    | x     | x    | x     |



 

Lorsque la comparaison a la valeur true, elle est déverrouillée de la boucle en cours, comme indiqué.


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




