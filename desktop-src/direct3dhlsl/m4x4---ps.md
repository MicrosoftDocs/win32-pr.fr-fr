---
title: M4X4-PS
description: Multiplie un vecteur à 4 composants par une matrice 4x4. | M4X4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7dfba3713bcd376c369a17d4856b64965e2e83c22ff03b282d4c9880d6c8700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906858"
---
# <a name="m4x4---ps"></a>M4X4-PS

Multiplie un vecteur à 4 composants par une matrice 4x4.

## <a name="syntax"></a>Syntaxe



| M4X4 DST, src0, src1 |
|----------------------|



 

where

-   l’heure d’été est le registre de destination. Le résultat est un vecteur à 4 composants.
-   src0 est un registre source qui représente un vecteur à 4 composants.
-   src1 est un registre source qui représente une matrice 4x4, qui correspond au premier des 4 registres consécutifs.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Le masque XYZW (par défaut) est requis pour le registre de destination. Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.

Les modificateurs Swizzle et négation ne sont pas valides pour le registre src0. Les registres DST et src0 ne peuvent pas être identiques.

L’extrait de code suivant montre les opérations effectuées.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



Le vecteur d’entrée se trouve dans Register src0. La matrice 4x4 d’entrée se trouve dans Register src1, et les trois registres supérieurs suivants, comme illustré dans l’expansion ci-dessous.

Cette opération est couramment utilisée pour transformer une position en une matrice de projection. Cette instruction est implémentée sous la forme d’un ensemble de produits point comme indiqué ici.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




