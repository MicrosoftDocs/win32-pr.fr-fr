---
title: LRP-PS
description: Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043064"
---
# <a name="lrp---ps"></a>LRP-PS

Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source.

## <a name="syntax"></a>Syntaxe



| LRP DST, src0, src1, src2 |
|---------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.
-   src2 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| lrp                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




