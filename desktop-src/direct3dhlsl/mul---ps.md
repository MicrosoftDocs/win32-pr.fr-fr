---
title: Mul-PS
description: Multiplie les sources dans la destination. | Mul-PS
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 74ff42065f7b41c1d775a0b1924d732110c31bd3121d2464b33eb8b20ae31e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986299"
---
# <a name="mul---ps"></a>Mul-PS

Multiplie les sources dans la destination.

## <a name="syntax"></a>Syntaxe



| Mul DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| mul                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre les opérations effectuées.


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




