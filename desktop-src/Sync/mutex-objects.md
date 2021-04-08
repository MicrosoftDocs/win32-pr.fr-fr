---
description: Un objet mutex est un objet de synchronisation dont l’État est défini sur signalé lorsqu’il n’appartient à aucun thread, et qui n’est pas signalé lorsqu’il est détenu.
ms.assetid: eca0795a-1fd0-4034-9d61-9416670919cf
title: Objets mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e84c17ba3e99e888f7d1e9137a7f24a4d78ce2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866617"
---
# <a name="mutex-objects"></a>Objets mutex

Un *objet mutex* est un objet de synchronisation dont l’État est défini sur signalé lorsqu’il n’appartient à aucun thread, et qui n’est pas signalé lorsqu’il est détenu. Un seul thread à la fois peut posséder un objet mutex, dont le nom vient du fait qu’il est utile pour coordonner l’accès mutuellement exclusif à une ressource partagée. Par exemple, pour empêcher deux threads d’écrire en mémoire partagée en même temps, chaque thread attend la propriété d’un objet mutex avant d’exécuter le code qui accède à la mémoire. Après avoir écrit dans la mémoire partagée, le thread libère l’objet Mutex.

Un thread utilise la fonction [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) ou [**CreateMutexEx**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa) pour créer un objet Mutex. Le thread de création peut demander la propriété immédiate de l’objet mutex et peut également spécifier un nom pour l’objet Mutex. Il peut également créer un mutex sans nom. Pour plus d’informations sur les noms des objets mutex, Event, Semaphore et Timer, consultez [synchronisation entre processus](interprocess-synchronization.md).

Les threads d’autres processus peuvent ouvrir un handle vers un objet mutex nommé existant en spécifiant son nom dans un appel à la fonction [**OpenMutex**](/windows/win32/api/synchapi/nf-synchapi-openmutexw) . Pour passer un handle à un mutex sans nom à un autre processus, utilisez la fonction [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) ou l’héritage de handle parent-enfant.

Tout thread avec un handle vers un objet mutex peut utiliser l’une des [fonctions Wait](wait-functions.md) pour demander la propriété de l’objet Mutex. Si l’objet mutex appartient à un autre thread, la fonction Wait bloque le thread demandeur jusqu’à ce que le thread propriétaire libère l’objet mutex à l’aide de la fonction [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) . La valeur de retour de la fonction Wait indique si la fonction est retournée pour une raison autre que l’état du mutex défini comme signalé.

Si plusieurs threads sont en attente sur un mutex, un thread en attente est sélectionné. Ne supposez pas un ordre FIFO (premier entré, premier sorti). Les événements externes tels que les APC en mode noyau peuvent modifier l’ordre d’attente.

Une fois qu’un thread a obtenu la propriété d’un mutex, il peut spécifier le même Mutex dans des appels répétés aux [fonctions Wait-Functions](wait-functions.md) sans bloquer son exécution. Cela empêche un thread de se bloquer en attendant un mutex qu’il détient déjà. Pour libérer sa propriété dans de telles circonstances, le thread doit appeler [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) une fois pour chaque fois que le mutex a respecté les conditions d’une fonction d’attente.

Si un thread se termine sans libérer sa propriété d’un objet mutex, l’objet mutex est considéré comme abandonné. Un thread en attente peut acquérir la propriété d’un objet mutex abandonné, mais la fonction Wait retourne **wait \_ abandonné** pour indiquer que l’objet mutex est abandonné. Un objet mutex abandonné indique qu’une erreur s’est produite et que toute ressource partagée protégée par l’objet mutex est dans un État indéfini. Si le thread continue comme si l’objet mutex n’avait pas été abandonné, il n’est plus considéré comme abandonné après la libération de sa propriété par le thread. Cela restaure le comportement normal si un descripteur de l’objet mutex est spécifié par la suite dans une fonction Wait.

Notez que les [objets de section critique](critical-section-objects.md) fournissent une synchronisation similaire à celle fournie par les objets mutex, à ceci près que les objets de section critique peuvent être utilisés uniquement par les threads d’un processus unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’objets mutex](using-mutex-objects.md)
</dt> </dl>

 

 
