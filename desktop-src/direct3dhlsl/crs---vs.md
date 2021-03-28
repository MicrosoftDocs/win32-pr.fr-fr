---
title: CRS-vs
description: Calcule un produit croisé à l’aide de la règle de droite. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322001"
---
# <a name="crs---vs"></a>CRS-vs

Calcule un produit croisé à l’aide de la règle de droite.

## <a name="syntax"></a>Syntaxe



| CRS DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre source.
-   src1 est un registre source.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Sir                    |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme indiqué ici.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Certaines restrictions sur l’utilisation de :

-   src0 ne peut pas être le même registre que dest.
-   src1 ne peut pas être le même registre que dest.
-   src0 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).
-   src1 ne peut pas avoir d’Swizzle autre que le Swizzle par défaut (. XYZW).
-   dest doit avoir exactement l’un des sept masques suivants :. x.y.. \| z. \| \| XY \| . XZ \| . YZ \| . xyz.
-   dest doit être un registre temporaire.
-   dest ne doit pas être le même registre que src0 ou src1

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




