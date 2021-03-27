---
title: M3x3-vs
description: Multiplie un vecteur à 3 composants par une matrice 3x3. | M3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394000"
---
# <a name="m3x3---vs"></a>M3x3-vs

Multiplie un vecteur à 3 composants par une matrice 3x3.

## <a name="syntax"></a>Syntaxe



| M3x3 DST, src0, src1 |
|----------------------|



 

where

-   l’heure d’été est le registre de destination. Le résultat est un vecteur à 3 composants.
-   src0 est un registre source qui représente un vecteur à 3 composants.
-   src1 est un registre source qui représente une matrice 3x3, qui correspond au premier des 3 registres consécutifs.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

Le masque XYZ est requis pour le registre de destination. Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.

Le fragment de code suivant montre les opérations effectuées.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Le vecteur d’entrée se trouve dans Register src0. La matrice 3x3 entrée se trouve dans Register src1, et les deux registres supérieurs suivants, comme illustré dans l’expansion ci-dessous. Un résultat 3D est généré, ce qui laisse l’autre élément du registre de destination (dest. w) non affecté.

Cette opération est couramment utilisée pour transformer les vecteurs normaux lors des calculs d’éclairage. Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ci-dessous.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




