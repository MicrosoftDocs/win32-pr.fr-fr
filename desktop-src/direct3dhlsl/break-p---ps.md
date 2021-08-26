---
title: breakp-PS
description: Quittez de manière conditionnelle la boucle actuelle au ENDLOOP-PS ou endrep-PS le plus proche. Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da0d2bceea7a3e44f02e6b732337cb3447d6ef1c9798f95b664bf4da96ec2dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983319"
---
# <a name="breakp---ps"></a>breakp-PS

Quittez de manière conditionnelle la boucle actuelle au [ENDLOOP-PS](endloop---ps.md) ou [endrep-PS](endrep---ps.md)le plus proche. Utilisez l’un des composants de l’inscription de prédicat comme condition pour déterminer s’il convient ou non d’exécuter l’instruction.

## <a name="syntax"></a>Syntaxe



| breakp \[ ! \] P0. x|y|Lettre|s |
|-----------------------------|



 

Où :

-   \[!\] est un modificateur de négation facultatif.
-   P0 correspond au [Registre de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   {x \| y \| z \| w} est le Swizzle de réplication requis sur P0.

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




