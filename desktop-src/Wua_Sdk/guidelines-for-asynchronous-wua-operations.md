---
description: Cette rubrique identifie les instructions à suivre lorsque vous effectuez des opérations d’agent de Windows Update asynchrones (WUA).
ms.assetid: 1fb16904-732d-4341-8267-ab8896fc0f7c
title: Instructions pour les opérations WUA asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a4b2198a235d9a03e3730e5d6dce2cd54c0e1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524120"
---
# <a name="guidelines-for-asynchronous-wua-operations"></a>Instructions pour les opérations WUA asynchrones

Cette rubrique identifie les instructions à suivre lorsque vous effectuez des opérations d’agent de Windows Update asynchrones (WUA).

-   Les opérations WUA asynchrones ne garantissent aucune vitesse d’achèvement particulière. La durée d’exécution d’une opération WUA asynchrone peut varier considérablement en fonction du matériel informatique, de la version du système d’exploitation et de la configuration du réseau. Comme pour les autres API Windows qui ont des dépendances réseau et qui ne contiennent pas de paramètre de délai d’attente ou de délai d’attente documenté, nous vous recommandons d’implémenter vos propres mécanismes de délai d’attente si vous avez besoin de temps de réponse garantis. Par exemple, vous pouvez créer un thread de travail qui appelle une méthode WUA asynchrone et définit un événement ou un autre objet de synchronisation lorsque l’opération WUA asynchrone se termine ; le thread principal peut ensuite utiliser la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) , qui vous permet de spécifier une valeur de délai d’attente.
-   Lorsque vous terminez une recherche, le téléchargement, l’installation ou la désinstallation de mises à jour, vous pouvez utiliser [**IUpdateSearcher :: EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch), [**IUpdateDowloader :: car EndDownload**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader), [**IUpdateInstaller :: EndInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-endinstall) et [**IUpdateInstaller :: EndUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-enduninstall) à partir de n’importe quel thread.
-   Lorsque vous lancez une recherche, un téléchargement, une installation ou une désinstallation de mises à jour à l’aide de [**IUpdateSearcher :: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader :: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller :: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)et [**IUpdateInstaller :: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall), veillez à conserver suffisamment de autorisations d’accès lorsque vous publiez des références aux objets API WUA.
    -   Assurez-vous que tous les objets de rappel utilisés dans l’opération asynchrone ne sont pas référencés avant de les détruire. Attendez que le décompte de références d’un objet de rappel retourne à la valeur initiale avant de le détruire.
    -   La référence à l’objet de traitement retourné par la méthode **Begin** correspondante doit être contrôlée par un objet qui diffère des objets de rappel. Utilisez un objet qui diffère des objets de rappel pour éviter les références circulaires.
    -   Si vous tentez de contrôler la référence à l’objet de traitement à l’aide d’un objet de rappel, vous devez appeler la méthode [**IDownloadJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) en dehors de la fonction de rappel pour déconnecter l’objet de traitement de l’objet de rappel. Vous devez effectuer cette opération avant de libérer la référence à l’objet de traitement retourné par la méthode **Begin** .
-   Assurez-vous que les opérations WUA asynchrones sont terminées. L’environnement d’exécution de scripts Windows peut mettre fin à un script lorsque toutes les commandes en dehors de toute fonction sont terminées, même si l’API WUA fait encore référence à l’objet de rappel.
    -   Utilisez l’une des méthodes de **nettoyage** ou faites en sorte que la fonction de rappel définisse une variable globale partagée après l’achèvement.
    -   N’appelez jamais [**IDownloadJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-cleanup), [**IInstallationJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-cleanup)ou [**ISearchJob :: Cleanup**](/windows/desktop/api/Wuapi/nf-wuapi-isearchjob-cleanup) sur un objet de traitement dans sa fonction de rappel.
    -   Pour garantir la séquence de nettoyage correcte dans un script qui s’exécute sur Windows Internet Explorer, appelez la méthode **Cleanup** sur tous les objets de tâche lors du traitement de Window. onbeforeunload.
-   N’utilisez pas de types de données définis par l’utilisateur (UDT) pour les opérations WUA asynchrones. Le type n’est pas pris en charge par [**IUpdateSearcher :: BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch), [**IUpdateDownloader :: BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload), [**IUpdateInstaller :: BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall)ou [**IUpdateInstaller :: BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall).

 

 
