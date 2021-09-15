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
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518640"
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

## <a name="remarks"></a>Notes



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

 

 




