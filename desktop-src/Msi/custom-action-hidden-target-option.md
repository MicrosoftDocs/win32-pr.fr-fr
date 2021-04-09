---
description: Utilisez les indicateurs d’option suivants pour spécifier que le programme d’installation n’écrit pas la valeur entrée dans le champ cible de la table CustomAction dans le journal. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ type de la table CustomAction.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Option cible masquée des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034651"
---
# <a name="custom-action-hidden-target-option"></a>Option cible masquée des actions personnalisées

Utilisez les indicateurs d’option suivants pour spécifier que le programme d’installation n’écrit pas la valeur entrée dans le champ cible de la [table CustomAction](customaction-table.md) dans le journal. Pour définir l’option, ajoutez la valeur de ce tableau à la valeur du champ type de la table CustomAction.



| Constante                            | Valeur hexadécimale | Decimal | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (aucun)                              | 0x0000      | 0       | Le programme d’installation peut écrire la valeur dans la colonne cible de la table CustomAction dans le fichier journal.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8 192    | Le programme d’installation ne peut pas écrire la valeur dans la colonne cible de la [table CustomAction](customaction-table.md) dans le fichier journal. La propriété CustomActionData n’est pas non plus journalisée lorsque le programme d’installation exécute l’action personnalisée.<br/> Étant donné que le programme d’installation définit la valeur de CustomActionData à partir d’une propriété portant le même nom que l’action personnalisée, cette propriété doit être listée dans la propriété [**MsiHiddenProperties**](msihiddenproperties.md) pour empêcher sa valeur d’apparaître dans le journal.<br/> |



 

Pour plus d’informations, consultez [empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence des actions personnalisées](custom-action-reference.md)
</dt> <dt>

[À propos des actions personnalisées](about-custom-actions.md)
</dt> <dt>

[Utilisation d’actions personnalisées](using-custom-actions.md)
</dt> </dl>

 

 




