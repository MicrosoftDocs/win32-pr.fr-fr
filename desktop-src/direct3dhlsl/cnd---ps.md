---
title: CND-PS
description: Choisit de façon conditionnelle entre src1 et src2, en fonction de la comparaison src0 0,5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726959"
---
# <a name="cnd---ps"></a>CND-PS

Choisit de façon conditionnelle entre src1 et src2, en fonction de la comparaison src0 > 0,5.

## <a name="syntax"></a>Syntaxe



| CND DST, src0, src1, src2 |
|---------------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.
-   src2 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

Pour les versions 1 \_ 1 à 1 \_ , src0 doit être R0. a.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



La version 1 \_ 4 compare chaque canal séparément.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



Ces exemples montrent une comparaison à quatre canaux effectuée dans un nuanceur de version 1 \_ 4, ainsi qu’une comparaison de canal unique possible dans un nuanceur de version 1 \_ 1.


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



La version 1 \_ 1 à 1 3 effectue une \_ comparaison avec le canal alpha répliqué de R0 uniquement.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



Cet exemple compare deux valeurs, A et B. L’exemple suppose qu’un est chargé dans v0 et que B est chargé dans v1. A et B doivent être dans la plage comprise entre-1 et + 1, et comme les registres de couleurs (VN) sont définis entre 0 et 1, la restriction se produit dans cet exemple.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




