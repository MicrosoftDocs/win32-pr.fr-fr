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
ms.openlocfilehash: a02bf34844918255086b318d9a13feeabbd6e75bdecca03684adaba70b420626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626559"
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

## <a name="remarks"></a>Remarques

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

 

 




