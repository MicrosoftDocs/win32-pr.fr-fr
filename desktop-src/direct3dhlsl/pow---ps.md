---
title: Pow-PS
description: Src0 (Full Precision ABS) src1. | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104974007"
---
# <a name="pow---ps"></a>Pow-PS

Src0 (Full Precision ABS)<sup>src1</sup>.

## <a name="syntax"></a>Syntaxe



| Pow DST, src0, src1 |
|---------------------|



 

where

-   l’heure d’été est le registre de destination.
-   src0 est un registre de la source d’entrée. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.
-   src1 est un registre de la source d’entrée. Le registre source nécessite l’utilisation explicite de Swizzle répliqués, c’est-à-dire qu’exactement l’un des composants. x,. y,. z,. w Swizzle (ou. r,. g,. b,. a équivalents) doit être spécifié.

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| pow                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Cette instruction fonctionne comme suit :

dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;

Il s’agit d’une instruction scalaire. par conséquent, les registres source doivent avoir répliqué Swizzles pour indiquer les canaux qui sont utilisés.

La puissance d’entrée (src1) doit être une scalaire.

Le résultat scalaire est répliqué sur les quatre canaux de sortie.

Cette instruction peut être développée en tant que exp (src1 \* log (src0)).

Le registre de l’heure d’été doit être un registre temporaire et ne doit pas être le même que src1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




