---
title: Si prédit-PS
description: Début d’une si bool-PS... else-PS... endif-bloc PS, avec la condition extraite du contenu du registre de prédicat.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1a9e1c531e5dc6cd76bdd220a94730f2fb7b859eb99d9bba217a008fb02b4c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511915"
---
# <a name="if-pred---ps"></a>Si prédit-PS

Début d’une [si bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-bloc PS](endif---ps.md) , avec la condition extraite du contenu du registre de prédicat.

## <a name="syntax"></a>Syntaxe



| Si \[ ! \] prédit. replicateSwizzle |
|-------------------------------|



 

Où :

-   \[!\] est un modificateur NOT facultatif. Cela modifie la valeur dans le registre de prédicat.
-   prédit est l' [enregistrement de prédicat](dx9-graphics-reference-asm-ps-registers-predicate.md).
-   replicateSwizzle est un composant unique qui est copié (ou répliqué) sur les quatre composants (swizzled). Les composants valides sont les suivants : \[ x, y, z, w \] ou \[ r, g, b, a \] .

## <a name="remarks"></a>Remarques



| Versions de nuanceur de pixels | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Si \_ prédite              |      |      |      |      |      | x    | x     | x    | x     |



 

Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’un canal du registre de prédicat. Chaque \_ bloc si prédit doit se terminer par une instruction [else-PS](else---ps.md) ou [endif-PS](endif---ps.md) .

Les restrictions sont les suivantes :

Si les \_ blocs prédits peuvent être imbriqués. Cela compte la profondeur d’imbrication dynamique totale, ainsi que [si les blocs \_ COMP sont](if-comp---ps.md) .

Un \_ bloc si prédit ne peut pas chevaucher un bloc de boucle ; il doit l’être entièrement à l’intérieur ou l’entourer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions sur le nuanceur de pixels](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




