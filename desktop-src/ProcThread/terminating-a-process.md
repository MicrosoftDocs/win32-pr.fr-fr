---
description: 'L’arrêt d’un processus a les résultats suivants : tous les threads restants dans le processus sont marqués pour l’arrêt. Toutes les ressources allouées par le processus sont libérées. Tous les objets de noyau sont fermés. Le code de processus est supprimé de la mémoire. Le code de sortie du processus est défini. L’objet processus est signalé.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Arrêt d’un processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d1a97b2b7342b67eaab72cae244b188df4cfeafbf2875d3bd62136ab6139748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081299"
---
# <a name="terminating-a-process"></a>Arrêt d’un processus

L’arrêt d’un processus a les résultats suivants :

-   Les threads restants dans le processus sont marqués pour l’arrêt.
-   Toutes les ressources allouées par le processus sont libérées.
-   Tous les objets de noyau sont fermés.
-   Le code de processus est supprimé de la mémoire.
-   Le code de sortie du processus est défini.
-   L’objet processus est signalé.

Alors que les handles ouverts aux objets noyau sont fermés automatiquement lorsqu’un processus se termine, les objets eux-mêmes existent jusqu’à ce que tous les descripteurs ouverts soient fermés. Par conséquent, un objet reste valide après qu’un processus qui l’utilise se termine si un autre processus y a un handle ouvert.

La fonction [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) retourne l’état d’arrêt d’un processus. Lorsqu’un processus est en cours d’exécution, son état d’arrêt est toujours \_ actif. Lorsqu’un processus se termine, son état d’arrêt passe de toujours \_ actif au code de sortie du processus.

Lorsqu’un processus se termine, l’état de l’objet de processus devient signalé, libérant tous les threads en attente de l’arrêt du processus. Pour plus d’informations sur la synchronisation, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).

Lorsque le système met fin à un processus, il n’arrête pas les processus enfants que le processus a créés. L’arrêt d’un processus ne génère pas de notifications pour les \_ procédures de hook CBT.

Utilisez la fonction [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) pour spécifier certains aspects de l’arrêt du processus lors de l’arrêt du système, par exemple lorsqu’un processus doit se terminer par rapport aux autres processus du système.

## <a name="how-processes-are-terminated"></a>Comment les processus sont terminés

Un processus s’exécute jusqu’à ce que l’un des événements suivants se produise :

-   Tout thread du processus appelle la fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) . Notez qu’une implémentation de la bibliothèque Runtime C (CRT) appelle **ExitProcess** si le thread principal du processus retourne.
-   Le dernier thread du processus se termine.
-   Tout thread appelle la fonction [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) avec un handle vers le processus.
-   Pour les processus de console, le [Gestionnaire de contrôle de console](/windows/console/console-control-handlers) par défaut appelle [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) lorsque la console reçoit un signal CTRL + C ou CTRL + ATTN.
-   L’utilisateur arrête le système ou se déconnecte.

Ne terminez pas un processus, sauf si ses threads se trouvent dans des États connus. Si un thread attend un objet de noyau, il ne se termine pas tant que l’attente n’est pas terminée. Cela peut entraîner l’arrêt de la réponse de l’application.

Le thread principal peut éviter d’arrêter d’autres threads en les dirigeant à appeler [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) avant de provoquer l’arrêt du processus (pour plus d’informations, consultez [arrêt d’un thread](terminating-a-thread.md)). Le thread principal peut toujours appeler [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) par la suite pour s’assurer que tous les threads sont terminés.

Le code de sortie d’un processus est soit la valeur spécifiée dans l’appel à [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) , soit [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), soit la valeur retournée par la fonction main ou [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) du processus. Si un processus est arrêté en raison d’une exception irrécupérable, le code de sortie est la valeur de l’exception à l’origine de l’arrêt. En outre, cette valeur est utilisée comme code de sortie pour tous les threads qui étaient en cours d’exécution lorsque l’exception s’est produite.

Si un processus se termine par [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), le système appelle la fonction de point d’entrée de chaque dll attachée avec une valeur indiquant que le processus est détaché de la dll. Les dll ne sont pas notifiées lorsqu’un processus est terminé par [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Pour plus d’informations sur les dll, consultez [bibliothèques de liens dynamiques](../dlls/dynamic-link-libraries.md).

Si un processus se termine par [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), tous les threads du processus sont terminés immédiatement, sans possibilité d’exécuter du code supplémentaire. Cela signifie que le thread n’exécute pas de code dans les blocs du gestionnaire de terminaisons. En outre, aucune dll attachée n’est notifiée que le processus est en cours de détachement. Si vous avez besoin d’un processus qui termine un autre processus, les étapes suivantes fournissent une meilleure solution :

-   Faire en sorte que les deux processus appellent la fonction [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) pour créer un message privé.
-   Un processus peut mettre fin à l’autre processus en diffusant un message privé à l’aide de la fonction [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) , comme suit :

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   Le processus recevant le message privé appelle [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) pour terminer son exécution.

L’exécution des fonctions [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)et [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) est sérialisée dans un espace d’adressage. Les restrictions suivantes s’appliquent :

-   Lors du démarrage du processus et des routines d’initialisation des DLL, de nouveaux threads peuvent être créés, mais ils ne commencent pas à s’exécuter tant que l’initialisation de la DLL n’est pas terminée pour le processus.
-   Un seul thread à la fois peut être dans une routine d’initialisation ou de détachement de DLL.
-   La fonction [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ne retourne pas jusqu’à ce qu’il n’y ait pas de threads dans leurs routines d’initialisation ou de détachement de dll.

 

 
