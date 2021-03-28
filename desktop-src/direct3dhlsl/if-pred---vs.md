---
title: Si prédit-vs
description: Début d’un if prédit-vs... else-vs... endif-bloc vs, avec la condition extraite du contenu du registre de prédicat.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313636"
---
# <a name="if-pred---vs"></a>Si prédit-vs

Début d’un if prédit-vs... [else-vs](else---vs.md)... [endif-bloc vs](endif---vs.md) , avec la condition extraite du contenu du registre de prédicat.

## <a name="syntax"></a>Syntaxe



| Si \[ ! \] prédit. replicateSwizzle |
|-------------------------------|



 

Où :

-   \[!\] modificateur NOT facultatif. Cela modifie la valeur dans le registre de prédicat.
-   prédit est le registre de prédicat, P0. Consultez [Registre de prédicat](dx9-graphics-reference-asm-vs-registers-predicate.md).
-   replicateSwizzle est un composant unique qui est copié (ou répliqué) sur les quatre composants (swizzled). Les composants valides sont les suivants : x, y, z, w ou r, g, b, a.

## <a name="remarks"></a>Notes



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ logiciels | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|------|-------|------|-------|
| Si prédite                |      |      | x    | x     | x    | x     |



 

Cette instruction est utilisée pour ignorer un bloc de code, en fonction d’un canal du registre de prédicat. Chaque \_ bloc si prédit doit se terminer par une instruction Else ou endif.

Les restrictions sont les suivantes :

Si les \_ blocs prédits peuvent être imbriqués. Cela compte la profondeur d’imbrication dynamique totale, ainsi que [si les blocs \_ COMP sont](if-comp---vs.md) .

Un \_ bloc si prédit ne peut pas chevaucher un bloc de boucle, il doit l’être entièrement à l’intérieur ou l’entourer.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions du nuanceur de sommets](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




