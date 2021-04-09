---
description: ICE78 vérifie que la table AdvtUISequence n’existe pas ou est vide. Cela est nécessaire, car aucune interface utilisateur n’est autorisée pendant la publicité.
ms.assetid: 8ed1c68f-331d-42f9-80df-bdcb42962482
title: ICE78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8993a0a03b0f70bf2d99511782bc9b7d259d4c9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113851"
---
# <a name="ice78"></a>ICE78

ICE78 vérifie que la [table AdvtUISequence](advtuisequence-table.md) n’existe pas ou est vide. Cela est nécessaire, car aucune interface utilisateur n’est autorisée pendant la publicité.

## <a name="result"></a>Résultats

ICE78 publie une erreur si la table AdvtUISequence existe et n’est pas vide.

## <a name="example"></a>Exemple

ICE78 signale l’erreur suivante pour l’exemple :

Action’action1 'trouvée dans la table AdvtUISequence. Aucune interface utilisateur n’est autorisée pendant la publicité. Par conséquent, la table AdvtUISequence doit être vide ou absente.

[Table AdvtUISequence](advtuisequence-table.md)(partielle)



| Action  | Condition | Séquence |
|---------|-----------|----------|
| Action1 | TRUE      | 1        |



 

Pour corriger l’erreur, supprimez « action1 » de la table ou supprimez la table.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



