---
title: breakp-vs
description: Quittez de manière conditionnelle la boucle actuelle à la valeur ENDLOOP-vs ou endrep-vs la plus proche. Utilisez l’un des composants du registre de prédicat comme condition pour déterminer s’il faut ou non effectuer l’instruction.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a768acaecaa77a42990b34c50cd8eccb24d61353550751f3ed830e7844d7624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794313"
---
# <a name="breakp---vs"></a>breakp-vs

Décomposer de manière conditionnelle de la boucle actuelle à l’instruction [ENDLOOP-vs](endloop---vs.md) ou [endrep-vs](endrep---vs.md). Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.

## <a name="syntax"></a>Syntaxe



| breakp \[ ! \] P0. x|y|Lettre|s |
|-----------------------------|



 

Où :

-   \[!\] valeur booléenne facultative.
-   P0 correspond au registre de prédicat. Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   {x \| y \| z \| w} est le Swizzle de réplication requis sur P0.

## <a name="remarks"></a>Remarques



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| breakp                 |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




