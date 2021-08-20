---
description: Les notifications suivantes sont utilisées avec les fonctions SetupInstallFile, SetupInstallFileEx et SetupInstallFromInfSection. Pour plus d’informations sur le format et l’utilisation des notifications, consultez notifications.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: Notifications de fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b48aff261cd867b1d2f01dbcad79f6e8fdefe49b1cfbba8dd07bb6c4572354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117965493"
---
# <a name="inf-file-notifications"></a>Notifications de fichier INF

Les notifications suivantes sont utilisées avec les fonctions [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea), [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)et [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) . Pour plus d’informations sur le format et l’utilisation des notifications, consultez [notifications](notifications.md).



| Notification                                                      | Description                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**SPFILENOTIFY \_ FILEOPDELAYED**](spfilenotify-fileopdelayed.md) | Le fichier est en cours d’utilisation et l’opération en cours est retardée jusqu’au redémarrage du système. |
| [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md)   | La langue du fichier actuel ne correspond pas à la langue du système.                   |
| [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md)   | Une copie du fichier spécifié existe déjà sur la cible.                             |
| [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md)     | Une version plus récente du fichier spécifié existe sur la cible.                            |



 

> [!Note]  
> Étant donné que [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crée et valide une file d’attente de fichiers interne, il utilise également les [notifications de file d’attente de fichiers](file-queue-notifications.md).

 

 

 



