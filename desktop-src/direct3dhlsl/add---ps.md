---
title: Add-PS
description: Ajoute deux vecteurs. | Add-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130088"
---
# <a name="add---ps"></a>Add-PS

Ajoute deux vecteurs.

## <a name="syntax"></a>Syntaxe



| Ajouter DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| add                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

L’extrait de code suivant montre les opérations effectuées.


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a>Informations sur les instructions



|   Condition requise                       | Value           |
|--------------------------|------------|
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




