---
title: CMP-PS
description: Choisissez src1 si src0 0. Dans le cas contraire, choisissez src2. La comparaison est effectuée par canal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232602"
---
# <a name="cmp---ps"></a>CMP-PS

Choisissez src1 si src0 >= 0. Dans le cas contraire, choisissez src2. La comparaison est effectuée par canal.

## <a name="syntax"></a>Syntaxe



| CMP DST, src0, src1, src2 |
|---------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.
-   src2 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CMP                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Il existe quelques limitations supplémentaires pour les versions 1 \_ 2 et 1 \_ 3 :

-   Chaque nuanceur peut utiliser jusqu’à un maximum de trois instructions CMP.
-   Le registre de destination ne peut pas être le même que l’un des registres source.

Cet exemple effectue une comparaison de quatre canaux.


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




