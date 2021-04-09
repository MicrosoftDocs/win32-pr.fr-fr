---
description: Cette rubrique identifie les indicateurs d’option que vous pouvez utiliser pour contrôler le traitement du thread d’action personnalisé.
ms.assetid: a09b3a0e-564e-41aa-af0d-2e46776f291b
title: Options de traitement des retours d’actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f8664ff489280993a7fc52117f3d19bccb023b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868881"
---
# <a name="custom-action-return-processing-options"></a>Options de traitement des retours d’actions personnalisées

Cette rubrique identifie les indicateurs d’option que vous pouvez utiliser pour contrôler le traitement du thread d’action personnalisé. Les indicateurs sont utilisés pour spécifier que les threads d’action principale et personnalisée s’exécutent de façon synchrone (Windows Installer attend que le thread d’action personnalisé se termine avant de reprendre le thread d’installation principal), ou de façon asynchrone (Windows Installer exécute l’action personnalisée simultanément pendant que l’installation principale se poursuit).

Pour activer les indicateurs d’option, ajoutez la valeur identifiée dans le tableau suivant à la valeur du champ type de la [table CustomAction](customaction-table.md).



| Constante                                                           | Valeur hexadécimale             | Decimal | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|-------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (aucun)                                                             | 0x00000000              | +0      | Exécution synchrone qui échoue si le code de sortie n’est pas 0 (zéro). <br/> Si l’indicateur msidbCustomActionTypeContinue n’est pas défini, l’action personnalisée doit retourner l’une des valeurs de retour qui est décrite dans les valeurs de retour de l' [action personnalisée](custom-action-return-values.md).<br/>                                                                                                                                                                                                                             |
| **msidbCustomActionTypeContinue**                                  | 0x00000040              | + 64     | Une exécution synchrone qui ignore le code de sortie et continue.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **msidbCustomActionTypeAsync**                                     | 0x00000080              | + 128    | Exécution asynchrone qui attend le code de sortie à la fin de la séquence.<br/> Cette option ne peut pas être utilisée avec des [installations simultanées](concurrent-installations.md), [restaurer des actions personnalisées](rollback-custom-actions.md)ou [écrire des actions personnalisées](scripts.md).<br/>                                                                                                                                                                                                                                |
| **msidbCustomActionTypeAsync**  +  **msidbCustomActionTypeContinue** | 0x00000040 + 0x00000080 | +192    | Exécution asynchrone qui n’attend pas la fin de l’opération.<br/> L’exécution se poursuit après l’arrêt de Windows Installer.<br/> Cette option ne peut être utilisée qu’avec les actions personnalisées de type EXE qui sont des [fichiers exécutables](executable-files.md). <br/> Tous les autres types d’actions personnalisées peuvent être asynchrones uniquement dans la session d’installation et doivent terminer pour que l’installation se termine.<br/> Cette option ne peut pas être utilisée avec des [installations simultanées](concurrent-installations.md).<br/> |



 

 

 




