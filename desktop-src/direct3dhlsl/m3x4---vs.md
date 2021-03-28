---
title: M3x4-vs
description: Multiplie un vecteur à 3 composants par une matrice 3x4. | M3x4-vs
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974026"
---
# <a name="m3x4---vs"></a>M3x4-vs

Multiplie un vecteur à 3 composants par une matrice 3x4.

## <a name="syntax"></a>Syntaxe



| M3x4 DST, src0, src1 |
|----------------------|



 

where

-   l’heure d’été est le registre de destination. Le résultat est un vecteur à 4 composants.
-   src0 est un registre source qui représente un vecteur à 3 composants.
-   src1 est un registre source qui représente une matrice 3x4, qui correspond au premier des 4 registres consécutifs.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

Le masque XYZW (par défaut) est requis pour le registre de destination. Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.

Le fragment de code suivant montre les opérations effectuées.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



Le vecteur d’entrée se trouve dans Register src0. La matrice d’entrée 3x4 est dans Register src1 et les trois registres supérieurs suivants, comme illustré dans l’expansion ci-dessous.

Cette opération est couramment utilisée pour transformer un vecteur de position en une matrice qui a un effet de projet, mais qui n’applique aucune traduction. Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




