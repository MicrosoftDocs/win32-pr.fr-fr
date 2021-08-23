---
description: Un objet de synchronisation est un objet dont le handle peut être spécifié dans l’une des fonctions Wait pour coordonner l’exécution de plusieurs threads.
ms.assetid: 11558ae9-1056-48bf-96f5-94a051df41c3
title: Objets de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd011663e13d8d6992355d99cc643e2f7243f8385ae75f9274367bfc43fe5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885907"
---
# <a name="synchronization-objects"></a>Objets de synchronisation

Un *objet de synchronisation* est un objet dont le handle peut être spécifié dans l’une des [fonctions Wait](wait-functions.md) pour coordonner l’exécution de plusieurs threads. Plusieurs processus peuvent avoir un handle vers le même objet de synchronisation, ce qui rend possible la synchronisation entre processus.

Les types d’objets suivants sont fournis exclusivement pour la synchronisation.



| Type           | Description                                                                                                                                                                                                      |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Événement          | Avertit un ou plusieurs threads en attente qu'un événement s'est produit. Pour plus d’informations, consultez [objets d’événement](event-objects.md).                                                                                   |
| Mutex          | Ne peut appartenir qu’à un seul thread à la fois, ce qui permet aux threads de coordonner l’accès mutuellement exclusif à une ressource partagée. Pour plus d’informations, consultez la page [objets mutex](mutex-objects.md).                          |
| Semaphore      | Conserve un nombre compris entre zéro et une valeur maximale, limitant ainsi le nombre de threads qui accèdent simultanément à une ressource partagée. Pour plus d’informations, consultez [objets Semaphore](semaphore-objects.md). |
| Minuterie (Timer) | Avertit un ou plusieurs threads en attente qu’une heure spécifiée est arrivée. Pour plus d’informations, consultez la rubrique [objets Timer waitables](waitable-timer-objects.md).                                                          |



 

Bien qu’elles soient disponibles pour d’autres utilisations, les objets suivants peuvent également être utilisés pour la synchronisation.



| Object                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Notification de modification          | Créé par la fonction [**FindFirstChangeNotification**](/windows/win32/api/fileapi/nf-fileapi-findfirstchangenotificationa) , son état est défini sur signalé lorsqu’un type de modification spécifié se produit dans un répertoire ou une arborescence de répertoires spécifiés. Pour plus d’informations, consultez [obtention de notifications de modification de répertoire](../fileio/obtaining-directory-change-notifications.md).                                                                                                                                   |
| Entrée de la console                | Créé lors de la création d’une console. Le descripteur de l’entrée de console est retourné par la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) lorsque CONIN $ est spécifié ou par la fonction [**GetStdHandle**](/windows/console/getstdhandle) . Son état est défini sur signalé quand il y a une entrée non lue dans la mémoire tampon d’entrée de la console et défini sur non signalé lorsque la mémoire tampon d’entrée est vide. Pour plus d’informations sur les consoles, consultez [applications en mode caractère](/windows/console/character-mode-applications) . |
| Travail                          | Créé en appelant la fonction [**CreateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-createjobobjectw) . L’état d’un objet de traitement est défini sur signalé lorsque tous ses processus sont terminés, car la limite de durée de fin de travail spécifiée a été dépassée. Pour plus d’informations sur les objets de traitement, consultez [objets de traitement](../procthread/job-objects.md).                                                                                                                                                             |
| Notification de ressource mémoire | Créé par la fonction [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) . Son état est défini sur signalé lorsqu’un type de modification spécifié se produit dans la mémoire physique. Pour plus d’informations sur la mémoire, consultez Gestion de la [mémoire](../memory/memory-management.md).                                                                                                                                                                                  |
| Process                      | Créé en appelant la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Son état est défini sur non signalé lorsque le processus est en cours d’exécution, et est défini sur signalé lorsque le processus se termine. Pour plus d’informations sur les processus, consultez [processus et threads](../procthread/processes-and-threads.md).                                                                                                                                                                                  |
| Thread                       | Créé lors de la création d’un nouveau thread en appelant la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)ou [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Son état est défini sur non signalé pendant que le thread est en cours d’exécution, et est défini sur signalé lorsque le thread se termine. Pour plus d’informations sur les threads, consultez [processus et threads](../procthread/processes-and-threads.md).                                                            |



 

Dans certains cas, vous pouvez également utiliser un fichier, un canal nommé ou un appareil de communication comme objet de synchronisation. Toutefois, leur utilisation à cet effet est déconseillée. Utilisez plutôt des e/s asynchrones et attendez l’objet d’événement défini dans la structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) . Il est plus sûr d’utiliser l’objet d’événement en raison de la confusion qui peut se produire lorsque plusieurs opérations de chevauchement simultanées sont exécutées sur le même fichier, canal nommé ou périphérique de communication. Dans ce cas, il n’existe aucun moyen de savoir quelle opération a provoqué le signalement de l’état de l’objet.

Pour plus d’informations sur les opérations d’e/s sur les fichiers, les canaux nommés ou les communications, consultez [synchronisation et entrée et sortie avec chevauchement](synchronization-and-overlapped-input-and-output.md).

 

 
