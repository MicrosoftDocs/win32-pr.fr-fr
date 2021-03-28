---
title: M3X2-PS
description: Multiplie un vecteur à 3 composants par une matrice matrice. | M3X2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974386"
---
# <a name="m3x2---ps"></a>M3X2-PS

Multiplie un vecteur à 3 composants par une matrice matrice.

## <a name="syntax"></a>Syntaxe



| M3X2 DST, src0, src1 |
|----------------------|



 

where

-   l’heure d’été est le registre de destination. Le résultat est un vecteur à 2 composants.
-   src0 est un registre source qui représente un vecteur à 3 composants.
-   src1 est un registre source qui représente une matrice matrice, qui correspond au premier des 2 registres consécutifs.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Le masque XY est requis pour le registre de destination. Les modificateurs de négation et Swizzle sont autorisés pour src0, mais pas pour src1.

Les équations suivantes illustrent le fonctionnement de l’instruction :


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



Le vecteur d’entrée se trouve dans Register src0. La matrice d’entrée matrice se trouve dans Register src1 et le registre supérieur suivant dans le même fichier de Registre, comme illustré dans l’extension suivante. Un résultat 2D est généré, laissant les autres éléments du registre de destination (dest. z et dest. w) non affectés.

Cette opération est couramment utilisée pour les transformations 2D. Cette instruction est implémentée en tant que paire de produits scalaires comme indiqué ici.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Les modificateurs Swizzle et négation ne sont pas valides pour le registre src1. Les registres DST et src0, ou l’un des registres src1 + i, ne peuvent pas être identiques.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




