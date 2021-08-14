---
description: Les fonctions Wait permettent à un thread de bloquer sa propre exécution.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Fonctions Wait
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764963"
---
# <a name="wait-functions"></a>Fonctions Wait

Les *fonctions Wait* permettent à un thread de bloquer sa propre exécution. Les fonctions Wait ne retournent pas tant que les critères spécifiés ne sont pas remplis. Le type de fonction Wait détermine l’ensemble de critères utilisé. Lorsqu’une fonction Wait est appelée, elle vérifie si les critères d’attente ont été satisfaits. Si les critères ne sont pas satisfaits, le thread appelant passe à l’état d’attente jusqu’à ce que les conditions des critères d’attente soient remplies ou que l’intervalle de délai d’attente spécifié soit écoulé.

-   [Fonctions d’attente d’objet unique](#single-object-wait-functions)
-   [Fonctions d’attente à plusieurs objets](#multiple-object-wait-functions)
-   [Fonctions d’attente alertables](#alertable-wait-functions)
-   [Fonctions d’attente inscrites](#registered-wait-functions)
-   [En attente d’une adresse](#waiting-on-an-address)
-   [Fonctions Wait et intervalles de délai d’attente](#wait-functions-and-time-out-intervals)
-   [Fonctions Wait et objets de synchronisation](#wait-functions-and-synchronization-objects)
-   [Fonctions Wait et création de Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Fonctions d’attente d’objet unique

Les fonctions [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)et [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) requièrent un handle vers un objet de synchronisation. Ces fonctions retournent lorsque l’une des conditions suivantes se produit :

-   L’objet spécifié est dans l’état signalé.
-   L’intervalle de délai d’attente est écoulé. L’intervalle de délai d’attente peut être défini sur **infini** pour spécifier que l’attente n’expirera pas.

La fonction [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permet au thread appelant de définir de manière atomique l’état d’un objet à signaler et d’attendre que l’état d’un autre objet soit défini sur signalé.

## <a name="multiple-object-wait-functions"></a>Fonctions d’attente à plusieurs objets

Les fonctions [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)et [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permettent au thread appelant de spécifier un tableau contenant un ou plusieurs descripteurs d’objets de synchronisation. Ces fonctions retournent lorsque l’une des conditions suivantes se produit :

-   L’état de l’un des objets spécifiés a la valeur signalée ou les États de tous les objets ont été signalés. Vous pouvez contrôler si l’un ou l’ensemble des États sera utilisé dans l’appel de fonction.
-   L’intervalle de délai d’attente est écoulé. L’intervalle de délai d’attente peut être défini sur **infini** pour spécifier que l’attente n’expirera pas.

La fonction [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) et [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) vous permettent de spécifier des objets d’événement d’entrée dans le tableau de handles d’objets. Cette opération est effectuée lorsque vous spécifiez le type d’entrée à attendre dans la file d’attente d’entrée du thread. Par exemple, un thread peut utiliser **MsgWaitForMultipleObjects** pour bloquer son exécution jusqu’à ce que l’état d’un objet spécifié soit défini sur signalé et que l’entrée de la souris soit disponible dans la file d’attente d’entrée du thread. Le thread peut utiliser la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) ou [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) pour récupérer l’entrée.

Lors de l’attente de la définition des États de tous les objets comme signalés, ces fonctions à plusieurs objets ne modifient pas les États des objets spécifiés tant que les États de tous les objets n’ont pas été signalés. Par exemple, l’état d’un objet mutex peut être signalé, mais le thread appelant n’obtient pas la propriété tant que les États des autres objets spécifiés dans le tableau n’ont pas également été définis sur signalé. En attendant, un autre thread peut devenir propriétaire de l’objet mutex, ce qui définit son état sur non signalé.

Lors de l’attente de la définition de l’état d’un objet unique comme signalé, ces fonctions à plusieurs objets vérifient les descripteurs dans le tableau dans l’ordre, en commençant par l’index 0, jusqu’à ce que l’un des objets soit signalé. Si plusieurs objets sont signalés, la fonction retourne l’index du premier handle dans le tableau dont l’objet a été signalé.

## <a name="alertable-wait-functions"></a>Fonctions d’attente alertables

Les fonctions [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)et [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) diffèrent des autres fonctions d’attente dans la mesure où elles peuvent éventuellement effectuer une opération d' *attente d’alerte*. Dans une opération d’attente d’alerte, la fonction peut retourner lorsque les conditions spécifiées sont remplies, mais elle peut également retourner si le système met en file d’attente une routine d’exécution d’e/s ou un APC pour l’exécuter par le thread en attente. Pour plus d’informations sur les opérations d’attente alertables et les routines d’exécution d’e/s, consultez [synchronisation et entrée et sortie avec chevauchement](synchronization-and-overlapped-input-and-output.md). Pour plus d’informations sur les APC, consultez [appels de procédure asynchrone](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Fonctions d’attente inscrites

La fonction [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) diffère des autres fonctions d’attente en ce que l’opération d’attente est effectuée par un thread du [pool de threads](../procthread/thread-pooling.md). Lorsque les conditions spécifiées sont remplies, la fonction de rappel est exécutée par un thread de travail à partir du pool de threads.

Par défaut, une opération d’attente inscrite est une opération à attente multiple. Le système réinitialise le minuteur chaque fois que l’événement est signalé (ou lorsque l’intervalle de délai d’attente est écoulé) jusqu’à ce que vous appeliez la fonction [**UnregisterWaitEx**](unregisterwaitex.md) pour annuler l’opération. Pour spécifier qu’une opération d’attente ne doit être exécutée qu’une seule fois, définissez le paramètre *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) sur **WT \_ EXECUTEONLYONCE**.

Si le thread appelle des fonctions qui utilisent des APC, définissez le paramètre *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) sur **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>En attente d’une adresse

Un thread peut utiliser la fonction [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) pour attendre que la valeur d’une adresse cible passe d’une valeur indésirable à une autre valeur. Cela permet aux threads d’attendre la modification d’une valeur sans avoir à faire pivoter ou gérer les problèmes de synchronisation qui peuvent survenir lorsque le thread capture une valeur indésirable, mais que la valeur change avant que le thread puisse attendre.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) retourne lorsque le code qui modifie la valeur cible signale la modification en appelant [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) pour mettre en éveil un seul thread en attente ou [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) pour réveiller tous les threads en attente. Si un intervalle de délai d’attente est spécifié avec **WaitOnAddress** et qu’aucun thread n’appelle une fonction Wake, la fonction retourne lorsque l’intervalle de délai d’attente expire. Si aucun intervalle de délai d’attente n’est spécifié, le thread attend indéfiniment.

## <a name="wait-functions-and-time-out-intervals"></a>Fonctions Wait et intervalles de délai d’attente

La précision de l’intervalle de délai d’attente spécifié dépend de la résolution de l’horloge système. L’horloge système « batte » à une vitesse constante. Si l’intervalle de délai d’attente est inférieur à la résolution de l’horloge système, l’attente peut expirer en moins de la durée spécifiée. Si l’intervalle de délai d’attente est supérieur à un, mais inférieur à deux, l’attente peut se situer n’importe où entre une graduation, et ainsi de suite.

Pour augmenter la précision de l’intervalle de délai d’attente pour les fonctions Wait, appelez la fonction **timeGetDevCaps** pour déterminer la résolution de minuteur minimale prise en charge et la fonction **timeBeginPeriod** pour définir la résolution de la minuterie sur sa valeur minimale. Soyez prudent lors de l’appel de **timeBeginPeriod**, car les appels fréquents peuvent avoir une incidence significative sur l’horloge système, l’utilisation de l’alimentation du système et le planificateur. Si vous appelez **timeBeginPeriod**, appelez-le une fois tôt dans l’application et veillez à appeler la fonction **timeEndPeriod** à la fin de l’application.

## <a name="wait-functions-and-synchronization-objects"></a>Fonctions Wait et objets de synchronisation

Les fonctions Wait peuvent modifier les États de certains types d' [objets de synchronisation](synchronization-objects.md). La modification se produit uniquement pour l’objet ou les objets dont l’état signalé a entraîné le retour de la fonction. Les fonctions Wait peuvent modifier les États des objets de synchronisation comme suit :

-   Le nombre d’un objet Semaphore diminue d’une unité, et l’état du sémaphore est défini sur non signalé si son nombre est égal à zéro.
-   Les États du mutex, de l’événement de réinitialisation automatique et des objets de notification de modification sont définis sur non signalé.
-   L’état d’un minuteur de synchronisation est défini sur non signalé.
-   Les États de l’événement de réinitialisation manuelle, du minuteur de réinitialisation manuelle, du processus, du thread et des objets d’entrée de la console ne sont pas affectés par une fonction d’attente.

## <a name="wait-functions-and-creating-windows"></a>Fonctions Wait et création de Windows

Vous devez être prudent lorsque vous utilisez les fonctions Wait et le code qui crée directement ou indirectement des fenêtres. Si un thread crée des fenêtres, il doit traiter les messages. Les diffusions de messages sont envoyées à toutes les fenêtres du système. Si vous disposez d’un thread qui utilise une fonction Wait sans délai d’expiration, le système se bloque. Les deux exemples de code qui crée indirectement des fenêtres sont DDE et la fonction **CoInitialize** . Par conséquent, si vous disposez d’un thread qui crée des fenêtres, utilisez [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) ou [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), plutôt que les autres fonctions d’attente.

 

 
