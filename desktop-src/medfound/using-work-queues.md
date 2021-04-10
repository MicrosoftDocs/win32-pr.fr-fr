---
description: Cette rubrique explique comment utiliser les files d’attente de travail dans Microsoft Media Foundation.
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: Utilisation des files d’attente de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201841"
---
# <a name="using-work-queues"></a>Utilisation des files d’attente de travail

Cette rubrique explique comment utiliser les files d’attente de travail dans Microsoft Media Foundation.

-   [Utilisation des files d’attente de travail](#using-work-queues)
-   [Arrêt des files d’attente de travail](#shutting-down-work-queues)
-   [Utilisation d’éléments de travail planifiés](#using-scheduled-work-items)
-   [Utilisation de rappels périodiques](#using-periodic-callbacks)
-   [Rubriques connexes](#related-topics)

## <a name="using-work-queues"></a>Utilisation des files d’attente de travail

Une file d’attente de travail est un moyen efficace d’effectuer des opérations asynchrones sur un autre thread. D’un point de vue conceptuel, vous placez des éléments de travail dans la file d’attente et la file d’attente dispose d’un thread qui extrait chaque élément de la file d’attente et le distribue. Les éléments de travail sont implémentés en tant que rappels à l’aide de l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .

Media Foundation crée plusieurs files d’attente de travail standard, appelées *files d’attente de travail de plateforme*. Les applications peuvent également créer leurs propres files d’attente de travail, appelées *files d’attente de travail privées*. Pour obtenir la liste des files d’attente de travail de plateforme, consultez [identificateurs de file d’attente de travail](work-queue-identifiers.md). Pour créer une file d’attente de travail privée, appelez [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue). Cette fonction retourne un identificateur pour la nouvelle file d’attente de travail. Pour placer un élément dans la file d’attente, appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). Dans les deux cas, vous devez spécifier une interface de rappel.

-   [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) prend un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , plus un objet d’État facultatif qui implémente **IUnknown**. Ce sont les mêmes paramètres que ceux utilisés dans les méthodes asynchrones, comme décrit dans la rubrique [méthodes de rappel asynchrones](asynchronous-callback-methods.md). En interne, cette fonction crée un objet de résultat asynchrone, qui est passé à la méthode [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) du rappel.
-   [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) prend un pointeur vers l’interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Cette interface représente un objet de résultat asynchrone. Créez cet objet en appelant [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) et en spécifiant votre interface de rappel et, éventuellement, un objet d’État.

Dans les deux cas, le thread de file d’attente de travail appelle votre méthode [**IMFAsyncCallback :: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Utilisez la méthode **Invoke** pour exécuter l’élément de travail.

Si plusieurs threads ou composants partagent la même file d’attente de travail, vous pouvez appeler [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) pour verrouiller la file d’attente de travail, ce qui empêche la plateforme de la libérer. Pour chaque appel à [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) ou **MFLockWorkQueue**, vous devez appeler [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) une fois pour libérer la file d’attente de travail. Par exemple, si vous créez une file d’attente de travail et que vous la verrouillez une fois, vous devez appeler **MFUnlockWorkQueue** deux fois, une fois pour l’appel à **MFAllocateWorkQueue** et une fois pour l’appel à **MFLockWorkQueue**.

Le code suivant montre comment créer une nouvelle file d’attente de travail, placer un élément de travail dans la file d’attente et libérer la file d’attente de travail.

Pour plus d’informations sur les files d’attente de travail dans Windows 8, consultez [files d’attente de travail et améliorations des threads](media-foundation-work-queue-and-threading-improvements.md) .


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



Cet exemple suppose que *pCallback* est un pointeur vers l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) de l’application. Il suppose également que le rappel définit le descripteur d’événement *hEvent* . Le code attend que cet événement soit défini avant d’appeler [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue).

Les threads de file d’attente de travail sont toujours créés dans le processus de l’appelant. Dans chaque file d’attente de travail, les rappels sont sérialisés. Si vous appelez [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) deux fois avec la même file d’attente de travail, le deuxième rappel n’est pas appelé tant que le premier rappel n’a pas été retourné.

## <a name="shutting-down-work-queues"></a>Arrêt des files d’attente de travail

Avant d’appeler [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), libérez toutes les ressources utilisées par les threads de file d’attente de travail. Pour synchroniser ce processus, vous pouvez verrouiller la plateforme Media Foundation, ce qui empêche la fonction **MFShutdown** de fermer les threads de file d’attente de travail. Si **MFShutdown** est appelé alors que la plateforme est verrouillée, **MFShutdown** attend quelques centaines de millisecondes pour que la plateforme soit déverrouillée. S’il n’est pas déverrouillé dans ce délai, **MFShutdown** ferme les threads de file d’attente de travail.

L’implémentation par défaut de [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) verrouille automatiquement la plateforme Media Foundation lors de la création de l’objet de résultat. La libération de l’interface déverrouille la plateforme. Par conséquent, vous n’avez presque jamais besoin de verrouiller la plateforme directement. Toutefois, si vous écrivez votre propre implémentation personnalisée de **IMFAsyncResult**, vous devez verrouiller et déverrouiller manuellement la plateforme. Pour verrouiller la plateforme, appelez [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform). Pour déverrouiller la plateforme, appelez [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform). Pour obtenir un exemple, consultez [objets de résultats asynchrones personnalisés](custom-asynchronous-result-objects.md).

Après avoir appelé [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), vous devez vous assurer que la plateforme est déverrouillée dans le délai de 5 secondes. Pour ce faire, vous devez libérer tous les pointeurs [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) et appeler [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) si vous avez verrouillé la plateforme manuellement. Veillez à libérer toutes les ressources utilisées par les threads de file d’attente de travail, sans quoi votre application peut présenter une fuite de mémoire.

En règle générale, si votre application s’arrête et libère tous les objets Media Foundation avant d’appeler [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), vous n’avez pas à vous soucier du verrouillage. Le mécanisme de verrouillage permet simplement aux threads de file d’attente de travail de se fermer correctement après l’appel de **MFShutdown**.

## <a name="using-scheduled-work-items"></a>Utilisation d’éléments de travail planifiés

Vous pouvez planifier un rappel au bout d’un laps de temps défini en appelant [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) ou [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex).

-   [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) prend un pointeur vers votre rappel, un objet d’État facultatif et un intervalle de délai d’attente.
-   [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) prend un pointeur vers un objet de résultat asynchrone et une valeur de délai d’attente.

Spécifiez le délai d’expiration sous la forme d’une valeur négative en millisecondes. Par exemple, pour planifier l’appel d’un rappel en 5 secondes, utilisez la valeur − 5000. Les deux fonctions retournent une valeur de **\_ clé MFWORKITEM** , que vous pouvez utiliser pour annuler le rappel en le passant à la fonction [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) .

Les éléments de travail planifiés utilisent toujours la \_ \_ \_ file d’attente de travail de la plateforme de minuteur de rappel MFASYNC.

## <a name="using-periodic-callbacks"></a>Utilisation de rappels périodiques

La fonction [**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) planifie un rappel à appeler régulièrement jusqu’à ce que vous l’annuliez. L’intervalle de rappel est fixe ; les applications ne peuvent pas la modifier. Pour déterminer l’intervalle exact, appelez [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity). L’intervalle est de l’ordre de 10 millisecondes. cette fonction est donc conçue pour les situations où vous avez besoin d’un « battement » fréquent, par exemple l’implémentation d’une horloge de présentation. Si vous souhaitez planifier une opération moins fréquemment, utilisez un élément de travail planifié, comme décrit précédemment.

Contrairement aux autres rappels décrits dans cette rubrique, le rappel périodique n’utilise pas l’interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Au lieu de cela, il utilise un pointeur de fonction. Pour plus d’informations, consultez [**rappel MFPERIODICCALLBACK**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).

Pour annuler le rappel périodique, appelez [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback).

Les rappels périodiques utilisent \_ la \_ \_ file d’attente de travail du minuteur de file d’attente de rappel MFASYNC.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Files d’attente de travail](work-queues.md)
</dt> <dt>

[**MFASYNCRESULT**](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[Améliorations de la file d’attente de travail et du thread](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
