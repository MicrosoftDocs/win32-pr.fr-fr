---
title: DP4-PS
description: Calcule le produit scalaire à quatre composants des registres sources. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043020"
---
# <a name="dp4---ps"></a>DP4-PS

Calcule le produit scalaire à quatre composants des registres sources.

## <a name="syntax"></a>Syntaxe



| DP4 DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp4                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre les opérations effectuées :


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



Limitations pour PS \_ 1 \_ 2 et PS \_ 1 \_ 3 :

-   Chaque nuanceur peut utiliser jusqu’à un maximum de quatre instructions DP4.
-   Chaque instruction DP4 compte comme deux instructions arithmétiques.

Limitations pour les \_ versions 1 X :

-   Cette instruction ne peut pas être co-émise, car DP4 s’exécute à la fois dans le pipeline Vector et alpha.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




