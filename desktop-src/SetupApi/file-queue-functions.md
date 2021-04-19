---
description: Les fonctions suivantes sont utilisées avec les files d’attente de fichiers.
ms.assetid: f05e2abf-983f-4418-bf92-f5ca6502196e
title: Fonctions de file d’attente de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acaf1fb1fbd2dc4f020577a1ae68d6ec9b2e95c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521052"
---
# <a name="file-queue-functions"></a>Fonctions de file d’attente de fichiers

Les fonctions suivantes sont utilisées avec les files d’attente de fichiers.



| Fonction                                                             | Description                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue)                   | Met fin à la file d’attente. Les transactions restantes ne sont pas validées.                                   |
| [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)                 | Valide toutes les transactions mises en file d’attente.                                                                      |
| [**SetupOpenFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue)                     | Initialise et retourne un handle vers la file d’attente de fichiers.                                                   |
| [**SetupPromptReboot**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptreboot)                       | Invite l’utilisateur à redémarrer son ordinateur, si nécessaire.                                         |
| [**SetupQueueCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya)                             | Met en file d’attente une copie de fichier.                                                                                   |
| [**SetupQueueCopySection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona)               | Met en file d’attente les fichiers dans une section de fichiers de copie INF.                                                        |
| [**SetupQueueDefaultCopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedefaultcopya)               | Met en file d’attente les fichiers dans une section de fichiers de copie INF à l’aide des informations par défaut spécifiées dans un fichier INF. |
| [**SetupQueueDelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea)                         | Met en file d’attente la suppression d’un fichier.                                                                               |
| [**SetupQueueDeleteSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)           | Met en file d’attente les fichiers dans un fichier INF supprimer les fichiers.                                                      |
| [**SetupQueueRename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)                         | Met en file d’attente un changement de nom de fichier.                                                                                 |
| [**SetupQueueRenameSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)           | Met en file d’attente les fichiers dans une section renommer les fichiers INF.                                                      |
| [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)                     | Analyse la file d’attente de fichiers.                                                                                 |
| [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) | Définit la substitution du chemin d’accès de la plateforme.                                                                      |



 

 

 



