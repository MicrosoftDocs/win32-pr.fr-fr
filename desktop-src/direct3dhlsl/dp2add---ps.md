---
title: dp2add-PS
description: Exécute un produit 2D point et un addition scalaire.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39a7cd640de57f2f69c8ee3b46ee6be6e52cbb16f9db39ef902725241d77b9c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068359"
---
# <a name="dp2add---ps"></a>dp2add-PS

Exécute un produit 2D point et un addition scalaire.

## <a name="syntax"></a>Syntaxe


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Où :

-   l’heure d’été est un registre de destination.
-   src0, src1 et src2 sont trois registres sources.
-   {x \| y \| z \| w} est le Swizzle de réplication requis sur src2.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

La valeur scalaire pour Add est choisie par l’Swizzle répliqué sur src2.

L’extrait de code suivant montre les opérations effectuées.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




