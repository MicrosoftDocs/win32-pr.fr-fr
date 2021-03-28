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
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104381186"
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

## <a name="remarks"></a>Notes



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| breakp                |      |      |      |      |      | x    | x     | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




