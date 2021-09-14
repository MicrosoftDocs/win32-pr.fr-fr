---
description: 'L’arrêt d’un thread a les résultats suivants : toutes les ressources détenues par le thread, telles que les fenêtres et les raccordements, sont libérées. Le code de sortie du thread est défini. L’objet thread est signalé. Si le thread est le seul thread actif dans le processus, le processus est arrêté. Pour plus d’informations, consultez arrêt d’un processus.'
ms.assetid: 633e5d0c-e9d8-4f9a-9411-17cbe9e2e6e4
title: Arrêt d’un thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada421356666316072aabff8281787cc140ad114
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007084"
---
# <a name="terminating-a-thread"></a>Arrêt d’un thread

L’arrêt d’un thread a les résultats suivants :

-   Toutes les ressources détenues par le thread, telles que les fenêtres et les raccordements, sont libérées.
-   Le code de sortie du thread est défini.
-   L’objet thread est signalé.
-   Si le thread est le seul thread actif dans le processus, le processus est arrêté. Pour plus d’informations, consultez [arrêt d’un processus](terminating-a-process.md).

La fonction [**GetExitCodeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodethread) retourne l’état d’arrêt d’un thread. Pendant l’exécution d’un thread, son état d’arrêt est toujours \_ actif. Lorsqu’un thread se termine, son état d’arrêt passe de toujours \_ actif au code de sortie du thread.

Lorsqu’un thread se termine, l’état de l’objet thread devient signalé, libérant tout autre thread en attente de l’arrêt du thread. Pour plus d’informations sur la synchronisation, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).

Lorsqu’un thread se termine, son objet thread n’est pas libéré tant que tous les descripteurs ouverts du thread ne sont pas fermés.

## <a name="how-threads-are-terminated"></a>Arrêt des threads

Un thread s’exécute jusqu’à ce que l’un des événements suivants se produise :

-   Le thread appelle la fonction [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) .
-   Tout thread du processus appelle la fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) .
-   La fonction de thread retourne.
-   Tout thread appelle la fonction [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) avec un handle vers le thread.
-   Tout thread appelle la fonction [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) avec un handle vers le processus.

Le code de sortie d’un thread est soit la valeur spécifiée dans l’appel à [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread), soit [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), soit la valeur retournée par la fonction de thread.

Si un thread se termine par [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), le système appelle la fonction de point d’entrée de chaque dll attachée avec une valeur indiquant que le thread se détache de la dll (sauf si vous appelez la fonction [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ). Si un thread se termine par [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), les fonctions de point d’entrée dll sont appelées une fois pour indiquer que le processus est en cours de détachement. Les dll ne sont pas notifiées lorsqu’un thread se termine par [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ou [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Pour plus d’informations sur les dll, consultez [bibliothèques de liens dynamiques](../dlls/dynamic-link-libraries.md).

Les fonctions [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) et [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) doivent être utilisées uniquement dans des circonstances extrêmes, dans la mesure où elles n’autorisent pas le nettoyage des threads, ne notifient pas les dll attachées et ne libèrent pas la pile initiale. En outre, les handles des objets détenus par le thread ne sont pas fermés tant que le processus n’est pas terminé. Les étapes suivantes fournissent une meilleure solution :

-   Créez un objet d’événement à l’aide de la fonction [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) .
-   Créez les threads.
-   Chaque thread surveille l’état de l’événement en appelant la fonction [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) . Utilisez un intervalle de délai d’attente de zéro.
-   Chaque thread met fin à sa propre exécution lorsque l’événement est défini sur l’état signalé ([**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retourne l' \_ objet wait \_ 0).

 

 
