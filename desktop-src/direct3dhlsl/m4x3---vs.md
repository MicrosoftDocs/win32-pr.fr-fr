---
title: m4x3-vs
description: Multiplie un vecteur à 4 composants par une matrice 4x3. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf4fb45fd38fe7d5acec95d750a050144a408c7fd1dedc44be858bc00aa58ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457419"
---
# <a name="m4x3---vs"></a>m4x3-vs

Multiplie un vecteur à 4 composants par une matrice 4x3.

## <a name="syntax"></a>Syntaxe



| m4x3 DST, src0, src1 |
|----------------------|



 

where

-   l’heure d’été est le registre de destination. Le résultat est un vecteur à 3 composants.
-   src0 est un registre source qui représente un vecteur à 4 composants.
-   src1 est un registre source qui représente une matrice 4x3, qui correspond au premier des 3 registres consécutifs.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

Le masque XYZ est requis pour le registre de destination. Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.

Le fragment de code suivant montre les opérations effectuées.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



Le vecteur d’entrée se trouve dans Register src0. La matrice d’entrée 4x3 est dans Register src1, et les deux registres suivants supérieurs, comme illustré dans l’expansion ci-dessous. Un résultat 3D est généré, ce qui laisse l’autre élément du registre de destination (dest. w) non affecté.

Cette opération est couramment utilisée pour transformer un vecteur de position en une matrice qui n’a pas d’effet de projet, comme c’est le cas dans les transformations d’espace de modèle. Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ci-dessous.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Les modificateurs Swizzle et négation ne sont pas valides pour le registre src1. Les registres DST et src0 ne peuvent pas être identiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




