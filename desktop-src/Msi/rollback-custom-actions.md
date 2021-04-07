---
description: Quand le programme d’installation traite le script d’installation, il génère simultanément un script de restauration.
ms.assetid: 5b9bfc5a-6a78-4b0e-aed8-f25aba089af1
title: Restaurer les actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4ad91f8f94145399d51ed2ef53999ab0a91d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863541"
---
# <a name="rollback-custom-actions"></a>Restaurer les actions personnalisées

Quand le programme d’installation traite le script d’installation, il génère simultanément un script de restauration. En plus du script de restauration, le programme d’installation enregistre une copie de chaque fichier qu’il supprime pendant l’installation. Ces fichiers sont conservés dans un répertoire système caché. Une fois l’installation terminée, le script de restauration et les fichiers enregistrés sont supprimés. Si une installation échoue, le programme d’installation tente de restaurer les modifications apportées lors de l’installation et de restaurer l’état d’origine de l’ordinateur.

Bien que les actions personnalisées qui planifient des opérations système en insérant des lignes dans la table de base de données soient inversées par une restauration de l’installation, les actions personnalisées qui modifient directement le système ou qui émettent des commandes vers d’autres services système ne peuvent pas toujours être inversées par une restauration. Une action personnalisée de restauration est une action exécutée par le programme d’installation uniquement pendant une restauration de l’installation. son objectif est d’inverser une action personnalisée qui a apporté des modifications au système.

Une action personnalisée de restauration est un type d' [action personnalisée d’exécution différée](deferred-execution-custom-actions.md), car son exécution est différée lorsqu’elle est appelée pendant la séquence d’installation. Elle diffère d’une action personnalisée différée standard en ce qu’elle n’est exécutée qu’au cours d’une restauration. Une action personnalisée de restauration doit toujours précéder l’action personnalisée différée, elle est restaurée dans la séquence d’action. Une action personnalisée de restauration doit également gérer le cas où l’action personnalisée différée est interrompue au milieu de l’exécution. Par exemple, si l’utilisateur appuie sur le bouton Annuler pendant l’exécution de l’action personnalisée.

Notez que les actions personnalisées Rollback ne peuvent pas s’exécuter de façon asynchrone. Consultez [actions personnalisées synchrones et asynchrones](synchronous-and-asynchronous-custom-actions.md).

Le complément à une action personnalisée de restauration est une [action personnalisée de validation](commit-custom-actions.md). Le programme d’installation exécute une action personnalisée de validation pendant la séquence d’installation, copie l’action personnalisée dans le script de restauration, mais n’exécute pas l’action pendant la restauration.

Notez qu’une action personnalisée de restauration peut ne pas être en mesure de supprimer toutes les modifications apportées par les actions personnalisées de validation. Bien que le programme d’installation écrit à la fois les actions personnalisées Rollback et Commit dans le script de restauration, les actions personnalisées commit ne s’exécutent qu’une fois que le programme d’installation a traité avec succès le script d’installation. Les actions personnalisées de validation sont les premières actions à exécuter dans le script de restauration. Si une action personnalisée de validation échoue, le programme d’installation lance la restauration, mais ne peut restaurer que les opérations déjà écrites dans le script de restauration. Cela signifie que, selon l’action personnalisée de validation, une restauration peut ne pas être en mesure d’annuler les modifications apportées par l’action. Vous pouvez ignorer les échecs dans les actions personnalisées de validation en créant l’action personnalisée afin d’ignorer les codes de retour.

Quand le programme d’installation exécute une action personnalisée de restauration, le seul paramètre de mode qu’il définit est MSIRUNMODE \_ Rollback. Pour obtenir une description des paramètres du mode d’exécution, consultez [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) .

Vous pouvez spécifier une action de restauration personnalisée en ajoutant un indicateur d’option au champ type de la [table CustomAction](customaction-table.md). Consultez [action personnalisée In-Script les options d’exécution](custom-action-in-script-execution-options.md) pour l’indicateur d’option désignant une action personnalisée de restauration.

Les actions personnalisées de restauration et de validation ne s’exécutent pas lorsque la restauration est désactivée. Si un auteur de package requiert ces types d’actions personnalisées pour une installation correcte, il doit utiliser la propriété [**RollbackDisabled**](rollbackdisabled.md) dans une condition qui empêche l’installation de se poursuivre lorsque la restauration est désactivée. Pour plus d’informations sur la désactivation de la restauration [, consultez restauration de l’installation (Windows Installer)](rollback-installation.md).

 

 



