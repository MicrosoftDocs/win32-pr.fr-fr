---
title: break_comp-PS
description: Sortir de la boucle actuelle au ENDLOOP-PS ou endrep-PS le plus proche, en fonction d’une comparaison par composant.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fa79b7aa50bc734ddc1f9fb1fd54e4130c48518dd47ed429b4177b8fb867d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794457"
---
# <a name="break_comp---ps"></a>arrêter \_ COMP-PS

Sortir de la boucle actuelle au [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)le plus proche, en fonction d’une comparaison par composant.

## <a name="syntax"></a>Syntaxe



| arrêter \_ COMP src0, src1 |
|------------------------|



 

Où :

-   \_COMP est une comparaison scalaire (ou unique) entre les deux registres sources. Les valeurs possibles sont les suivantes : 

    | Syntaxe | Comparaison            |
    |--------|-----------------------|
    | \_TB   | Supérieur à          |
    | \_terme   | Inférieur à             |
    | \_&   | Supérieur ou égal à |
    | \_WinINSTALL   | Inférieur ou égal à    |
    | \_EQ   | Égal à              |
    | \_ne   | Différent de          |

    

     

-   src0 est un registre source. La réplication de Swizzle est requise si vous sélectionnez un seul composant.
-   src1 est un registre source. La réplication de Swizzle est requise si vous sélectionnez un seul composant.

## <a name="remarks"></a>Remarques

Cette instruction est prise en charge dans les versions suivantes.



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| arrêter la \_ COMP.           |      |      |      |      |      | x    | x     | x    | x     |



 

Lorsque la comparaison a la valeur true, elle est déverrouillée de la boucle en cours, comme indiqué.


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




