---
title: NRM-PS
description: Normaliser un vecteur 3D. | NRM-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322121"
---
# <a name="nrm---ps"></a>NRM-PS

Normaliser un vecteur 3D.

## <a name="syntax"></a>Syntaxe



| NRM DST, SRC |
|--------------|



 

where

-   l’heure d’été est le registre de destination.
-   SRC est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| nrm                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne conceptuellement comme indiqué ici.

squareRootOfTheSum = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



Les registres dest et SRC ne peuvent pas être identiques. Le registre de dest doit être un registre temporaire.

Cette instruction effectue l’interpolation linéaire basée sur la formule suivante.


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




