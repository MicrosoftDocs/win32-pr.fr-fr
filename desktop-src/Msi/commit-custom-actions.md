---
description: Les actions personnalisées de validation sont exécutées à la fin du script d’installation.
ms.assetid: ad766585-e8ac-44b6-9717-7979f803886c
title: Valider des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a126468df400e23c8eb59885b6e5a66c96d740c0c0e0959320697da293d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380304"
---
# <a name="commit-custom-actions"></a>Valider des actions personnalisées

Les actions personnalisées de validation sont exécutées à la fin du script d’installation. Si l' [action InstallFinalize](installfinalize-action.md) est réussie, le programme d’installation exécute ensuite toutes les actions personnalisées commit existantes. Le seul paramètre de mode défini par le programme d’installation dans ce cas est MSIRUNMODE \_ Commit. Pour obtenir une description des paramètres du mode d’exécution, consultez [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

Une action personnalisée de validation peut être spécifiée en ajoutant un indicateur d’option au champ type de la [table CustomAction](customaction-table.md). Consultez [action personnalisée In-Script les options d’exécution](custom-action-in-script-execution-options.md) pour l’indicateur d’option désignant une action personnalisée de validation.

Une action personnalisée de validation est le complément à une [action personnalisée de restauration](rollback-custom-actions.md) et peut être utilisée avec les actions personnalisées Rollback pour inverser les actions personnalisées qui effectuent des modifications directement sur le système.

Notez qu’une action personnalisée de restauration peut ne pas être en mesure de supprimer toutes les modifications apportées par les actions personnalisées de validation. Bien que le programme d’installation écrit à la fois les actions personnalisées Rollback et Commit dans le script de restauration, les actions personnalisées commit ne s’exécutent qu’une fois que le programme d’installation a traité avec succès le script d’installation. Les actions personnalisées de validation sont les premières actions à exécuter dans le script de restauration. Si une action personnalisée de validation échoue, le programme d’installation lance la restauration, mais ne peut restaurer que les opérations déjà écrites dans le script de restauration. Cela signifie que, selon l’action personnalisée de validation, une restauration peut ne pas être en mesure d’annuler les modifications apportées par l’action. Vous pouvez ignorer les échecs dans les actions personnalisées de validation en créant l’action personnalisée afin d’ignorer les codes de retour.

Les actions personnalisées de restauration et de validation ne s’exécutent pas lorsque la restauration est désactivée. Si un auteur de package requiert ces types d’actions personnalisées pour une installation correcte, il doit utiliser la propriété [**RollbackDisabled**](rollbackdisabled.md) dans une condition qui empêche l’installation de se poursuivre lorsque la restauration est désactivée.

 

 



