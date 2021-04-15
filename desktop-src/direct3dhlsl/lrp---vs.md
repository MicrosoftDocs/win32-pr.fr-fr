---
title: LRP-vs
description: Interpole de manière linéaire entre les deuxième et troisième registres sources d’une proportion spécifiée dans le premier registre source. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104992008"
---
# <a name="lrp---vs"></a>LRP-vs

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



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| lrp                    |      | x    | x    | x     | x    | x     |



 

Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




