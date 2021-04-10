---
description: Un appel de procédure asynchrone (APC) est une fonction qui s’exécute de façon asynchrone dans le contexte d’un thread particulier.
ms.assetid: 0197d78e-a4dc-414b-88ba-c5ec5f2ed614
title: Appels de procédure asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd95e9afd663e2a462335b3c47bfe99462b449e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952495"
---
# <a name="asynchronous-procedure-calls"></a>Appels de procédure asynchrone

Un *appel de procédure asynchrone* (APC) est une fonction qui s’exécute de façon asynchrone dans le contexte d’un thread particulier. Lorsqu’un APC est mis en file d’attente sur un thread, le système émet une interruption logicielle. La prochaine fois que le thread sera planifié, il exécutera la fonction APC. Un APC généré par le système est appelé *APC en mode noyau*. Un APC généré par une application est appelé *APC en mode utilisateur*. Un thread doit être dans un état d’alerte pour exécuter un APC en mode utilisateur.

Chaque thread possède sa propre file d’attente APC. Une application met en file d’attente un APC sur un thread en appelant la fonction [**QueueUserAPC**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) . Le thread appelant spécifie l’adresse d’une fonction APC dans l’appel à **QueueUserAPC**. La mise en file d’attente d’un APC est une demande pour que le thread appelle la fonction APC.

Lorsqu’un APC en mode utilisateur est mis en file d’attente, le thread dans lequel il est mis en file d’attente n’est pas dirigé vers l’appel de la fonction APC, sauf s’il est dans un état d’alerte. Un thread entre dans un état d’alerte quand il appelle la fonction [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**WaitForMultipleObjectsEx**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjectsex)ou [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) . Si l’attente est satisfaite avant que l’APC ne soit mis en file d’attente, le thread n’est plus dans un état d’attente d’alerte, de sorte que la fonction APC ne sera pas exécutée. Toutefois, l’APC est toujours mis en file d’attente, de sorte que la fonction APC est exécutée lorsque le thread appelle une autre fonction d’attente alertable.

Les fonctions [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex), [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer), [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)et [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex) sont implémentées à l’aide d’un APC comme mécanisme de rappel de notification d’achèvement.

Si vous utilisez un [pool de threads](../procthread/thread-pools.md), Notez que les APC ne fonctionnent pas et d’autres mécanismes de signalisation, car le système contrôle la durée de vie des threads du pool de threads. il est donc possible qu’un thread se termine avant la remise de la notification. Au lieu d’utiliser un mécanisme de signalisation basé sur APC, tel que le paramètre *pfnCompletionRoutine* de [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) ou [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex), utilisez un objet d’attente, tel qu’un Timer créé avec [**CreateThreadpoolTimer**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpooltimer). Pour les e/s, utilisez un objet de fin d’e/s créé avec [**CreateThreadpoolIo**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-createthreadpoolio) ou une [**structure OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) basée sur *hEvent* où l’événement peut être passé à la fonction [**SetThreadpoolWait**](/windows/win32/api/threadpoolapiset/nf-threadpoolapiset-setthreadpoolwait) .

## <a name="synchronization-internals"></a>Éléments internes de la synchronisation

Lorsqu’une demande d’e/s est émise, une structure est allouée pour représenter la demande. Cette structure est appelée paquet de demande d’e/s (IRP). Avec les e/s synchrones, le thread génère l’IRP, l’envoie à la pile de l’appareil et attend que l’IRP se termine. Avec les e/s asynchrones, le thread génère l’IRP et l’envoie à la pile de l’appareil. La pile peut effectuer immédiatement la IRP, ou elle peut retourner un état d’attente indiquant que la demande est en cours. Dans ce cas, la IRP est toujours associée au thread, donc elle sera annulée si le thread se termine ou appelle une fonction telle que [**CancelIo**](/windows/win32/api/ioapiset/nf-ioapiset-cancelio). Dans le même temps, le thread peut continuer à exécuter d’autres tâches pendant que la pile de l’appareil continue à traiter l’IRP.

Le système peut indiquer plusieurs méthodes pour indiquer que la IRP est terminée :

-   Mettez à jour la structure OVERLAPPED avec le résultat de l’opération afin que le thread puisse interroger pour déterminer si l’opération est terminée.
-   Signalez l’événement dans la structure OVERLAPPED pour qu’un thread puisse se synchroniser sur l’événement et être réveillée lorsque l’opération se termine.
-   Met en file d’attente l’IRP vers l’APC en attente du thread afin que le thread exécute la routine APC lorsqu’il entre dans un état d’attente alerté et retourne à partir de l’opération d’attente avec un état indiquant qu’il a exécuté une ou plusieurs routines APC.
-   Mettre l’IRP en file d’attente sur un port de terminaison d’e/s, où il sera exécuté par le thread suivant qui attend le port de terminaison.

Les threads qui attendent un port de terminaison d’e/s n’attendent pas dans un état d’alerte. Par conséquent, si ces threads émettent des IRP qui sont définis pour s’exécuter comme des APC pour le thread, ces achèvements IPC ne se produiront pas dans les délais. ils se produisent uniquement si le thread récupère une demande à partir du port de terminaison d’e/s, puis qu’il passe à une attente d’alerte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’un minuteur qui peut être utilisé avec un appel de procédure asynchrone](using-a-waitable-timer-with-an-asynchronous-procedure-call.md)
</dt> </dl>

 

 
