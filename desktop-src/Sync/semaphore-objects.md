---
description: Un objet Semaphore est un objet de synchronisation qui gère un nombre compris entre zéro et une valeur maximale spécifiée.
ms.assetid: d9da1d98-a306-4e2d-a149-1eef6a724751
title: Objets Semaphore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c814be0ab2fafe7fbabfdeca5b640cfb550172a09e465dddc71629dfa5b0068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886258"
---
# <a name="semaphore-objects"></a>Objets Semaphore

Un *objet Semaphore* est un objet de synchronisation qui gère un nombre compris entre zéro et une valeur maximale spécifiée. Le nombre est décrémenté chaque fois qu’un thread termine une attente pour l’objet Semaphore et est incrémenté chaque fois qu’un thread libère le sémaphore. Lorsque le nombre atteint zéro, aucun thread supplémentaire ne peut attendre que l’état de l’objet sémaphore soit signalé. L’état d’un sémaphore est défini sur « signalé » quand son nombre est supérieur à zéro et sur « non signalé » quand son nombre est égal à zéro.

L’objet Semaphore est utile pour contrôler une ressource partagée pouvant prendre en charge un nombre limité d’utilisateurs. Il agit comme une porte qui limite le nombre de threads qui partagent la ressource à un nombre maximal spécifié. Par exemple, une application peut limiter le nombre de fenêtres qu’elle crée. Elle utilise un sémaphore avec un nombre maximal égal à la limite de la fenêtre, en décrémentant le nombre chaque fois qu’une fenêtre est créée et en l’incrémentant à chaque fois qu’une fenêtre est fermée. L’application spécifie l’objet Semaphore dans l’appel à l’une des [fonctions Wait](wait-functions.md) avant la création de chaque fenêtre. Lorsque le nombre est égal à zéro, ce qui indique que la limite de la fenêtre a été atteinte : la fonction Wait bloque l’exécution du code de création de fenêtre.

Un thread utilise la fonction [**CreateSemaphore,**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea) ou [**CreateSemaphoreEx**](/windows/desktop/api/WinBase/nf-winbase-createsemaphoreexa) pour créer un objet Semaphore. Le thread de création spécifie le nombre initial et la valeur maximale du nombre pour l’objet. Le nombre initial ne doit pas être inférieur à zéro ni supérieur à la valeur maximale. Le thread de création peut également spécifier un nom pour l’objet Semaphore. Les threads d’autres processus peuvent ouvrir un handle vers un objet sémaphore existant en spécifiant son nom dans un appel à la fonction [**OpenSemaphore**](/windows/win32/api/synchapi/nf-synchapi-opensemaphorew) . Pour plus d’informations sur les noms des objets mutex, Event, Semaphore et Timer, consultez [synchronisation entre processus](interprocess-synchronization.md).

Si plusieurs threads sont en attente sur un sémaphore, un thread en attente est sélectionné. Ne supposez pas un ordre FIFO (premier entré, premier sorti). Les événements externes tels que les APC en mode noyau peuvent modifier l’ordre d’attente.

Chaque fois que l’une des [fonctions Wait](wait-functions.md) est retournée parce que l’état d’un sémaphore a été signalé, le nombre du sémaphore est réduit d’une unité. La fonction [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) augmente le nombre d’un sémaphore d’une quantité spécifiée. Le nombre ne peut jamais être inférieur à zéro ou supérieur à la valeur maximale.

Le nombre initial d’un sémaphore est généralement défini sur la valeur maximale. Le décompte est ensuite décrémenté à partir de ce niveau, car la ressource protégée est consommée. Vous pouvez également créer un sémaphore avec un nombre initial de zéro pour bloquer l’accès à la ressource protégée pendant l’initialisation de l’application. Après l’initialisation, vous pouvez utiliser [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) pour incrémenter le nombre à la valeur maximale.

Un thread qui possède un objet mutex peut attendre de façon répétée que le même objet mutex soit signalé sans que son exécution ne soit bloquée. Toutefois, un thread qui attend plusieurs fois le même objet Semaphore décrémente le nombre du sémaphore chaque fois qu’une opération d’attente est terminée ; le thread est bloqué lorsque le nombre est égal à zéro. De même, seul le thread qui possède un mutex peut appeler la fonction [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) , même si tout thread peut utiliser [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) pour augmenter le nombre d’un objet Semaphore.

Un thread peut décrémenter plusieurs fois le nombre d’un sémaphore en spécifiant de manière répétée le même objet Semaphore dans les appels à l’une des [fonctions Wait](wait-functions.md). Toutefois, l’appel de l’une des fonctions d’attente à plusieurs objets avec un tableau qui contient plusieurs handles du même sémaphore n’entraîne pas de décrémentations multiples.

Lorsque vous avez fini d’utiliser l’objet Semaphore, appelez la fonction [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) pour fermer le descripteur. L’objet Semaphore est détruit quand son dernier descripteur a été fermé. La fermeture du handle n’affecte pas le nombre de sémaphores ; par conséquent, veillez à appeler [**ReleaseSemaphore,**](/windows/win32/api/synchapi/nf-synchapi-releasesemaphore) avant de fermer le handle ou avant que le processus ne se termine. Sinon, les opérations d’attente en attente expirent ou se poursuivent indéfiniment, selon qu’une valeur de délai d’attente a été spécifiée ou non.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’objets Semaphore](using-semaphore-objects.md)
</dt> </dl>

 

 
