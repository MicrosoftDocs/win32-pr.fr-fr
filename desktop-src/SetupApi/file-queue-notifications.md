---
description: Les notifications suivantes sont utilisées avec les files d’attente de fichiers. Pour plus d’informations sur le format et l’utilisation des notifications, consultez notifications.
ms.assetid: 4a171b4a-8623-4be3-81ee-99081fe23034
title: Notifications de file d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ed3dcef7de951c66bd3822b5c1e14fed676ea8a55a41d6468f60c5cf6ca218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965692"
---
# <a name="file-queue-notifications"></a>Notifications de file d’attente de fichiers

Les notifications suivantes sont utilisées avec les files d’attente de fichiers. Pour plus d’informations sur le format et l’utilisation des notifications, consultez [notifications](notifications.md).



| Notification                                                      | Description                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ COPYERROR**](spfilenotify-copyerror.md)         | Une erreur s’est produite lors d’une opération de copie de fichier.                                                  |
| [**SPFILENOTIFY \_ DELETEERROR**](spfilenotify-deleteerror.md)     | Une erreur s’est produite lors d’une opération de suppression de fichier.                                                 |
| [**SPFILENOTIFY \_ ENDCOPY**](spfilenotify-endcopy.md)             | Une opération de copie de fichier s’est terminée.                                                                 |
| [**SPFILENOTIFY \_ ENDDELETE**](spfilenotify-enddelete.md)         | Une opération de suppression de fichier s’est terminée.                                                                |
| [**SPFILENOTIFY \_ ENDQUEUE**](spfilenotify-endqueue.md)           | La file d’attente a terminé la validation.                                                                  |
| [**SPFILENOTIFY \_ ENDRENAME**](spfilenotify-endrename.md)         | Une opération de changement de nom de fichier s’est terminée.                                                                  |
| [**SPFILENOTIFY \_ ENDSUBQUEUE**](spfilenotify-endsubqueue.md)     | Une sous-file d’attente (copier, renommer ou supprimer) s’est terminée.                                               |
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | Le fichier était en cours d’utilisation et l’opération actuelle a été retardée jusqu’au redémarrage du système.       |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | Le langage de l’opération en cours ne correspond pas à la langue du système.                           |
| [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)         | Un nouveau média source est nécessaire.                                                                         |
| [**SPFILENOTIFY \_ QUEUESCAN**](spfilenotify-queuescan.md)         | Un nœud de la file d’attente de fichiers a été analysé. ( [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) uniquement) |
| [**SPFILENOTIFY \_ RENAMEERROR**](spfilenotify-renameerror.md)     | Une erreur s’est produite lors d’une opération de changement de nom de fichier.                                                 |
| [**SPFILENOTIFY \_ STARTCOPY**](spfilenotify-startcopy.md)         | Une opération de copie de fichier a démarré.                                                                  |
| [**SPFILENOTIFY \_ STARTDELETE**](spfilenotify-startdelete.md)     | Une opération de suppression de fichier a démarré.                                                                |
| [**SPFILENOTIFY \_ STARTQUEUE**](spfilenotify-startqueue.md)       | La file d’attente a commencé la validation.                                                                    |
| [**SPFILENOTIFY \_ STARTRENAME**](spfilenotify-startrename.md)     | Une opération de changement de nom de fichier a démarré.                                                                |
| [**SPFILENOTIFY \_ STARTSUBQUEUE**](spfilenotify-startsubqueue.md) | Une sous-file d’attente (copier, renommer ou supprimer) a démarré.                                             |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Une copie du fichier spécifié existe déjà sur la cible.                                          |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Une version plus récente du fichier spécifié existe sur la cible.                                         |



 

 

 



