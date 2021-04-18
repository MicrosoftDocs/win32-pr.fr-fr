---
description: La classe COutputQueue implémente une file d’attente pour fournir des exemples de médias.
ms.assetid: da35bdac-fdc2-4b38-8253-547a19213cce
title: COutputQueue, classe (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd6167402abd36db8f436f6e27b18213642f010b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526530"
---
# <a name="coutputqueue-class"></a>COutputQueue, classe

![coutputqueue](images/oput01.png)

La `COutputQueue` classe implémente une file d’attente pour fournir des exemples de médias.

Cette classe permet à une broche de sortie de remettre des exemples de manière asynchrone. Les exemples sont placés dans une file d’attente et un thread de travail les remet à la broche d’entrée. La file d’attente peut également contenir des messages de contrôle qui indiquent un nouveau segment, une notification de fin de flux ou une opération de vidage.

Pour utiliser cette classe, créez un objet **COutputQueue** pour chaque broche de sortie sur le filtre. Dans la méthode du constructeur, spécifiez la broche d’entrée connectée à cette broche de sortie. À l’aide de cette classe, la broche de sortie n’appelle pas les méthodes directement sur la broche d’entrée. Au lieu de cela, il appelle les méthodes correspondantes dans `COutputQueue` , comme indiqué dans le tableau suivant.



| Pin, méthode                                                            | Méthode COutputQueue                                     |
|-----------------------------------------------------------------------|---------------------------------------------------------|
| [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush)                           | [**BeginFlush**](coutputqueue-beginflush.md)           |
| [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)                               | [**EndFlush**](coutputqueue-endflush.md)               |
| [**IPin :: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)                         | [**EOS**](coutputqueue-eos.md)                         |
| [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)                           | [**NewSegment**](coutputqueue-newsegment.md)           |
| [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)                 | [**Çoive**](coutputqueue-receive.md)                 |
| [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) | [**ReceiveMultiple**](coutputqueue-receivemultiple.md) |



 

Si vous le souhaitez, vous pouvez configurer l' `COutputQueue` objet pour remettre des exemples de manière synchrone, sans thread de travail. L’objet peut également décider au moment de l’exécution s’il faut utiliser un thread de travail, en fonction des caractéristiques de la broche d’entrée. Pour plus d’informations, consultez [**COutputQueue :: COutputQueue**](coutputqueue-coutputqueue.md).



| Variables membres protégées                                   | Description                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**m \_ pPin**](coutputqueue-m-ppin.md)                       | Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel d’entrée.                                               |
| [**m \_ pInputPin**](coutputqueue-m-pinputpin.md)             | Pointeur vers l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) du code confidentiel d’entrée.                               |
| [**m \_ bBatchExact**](coutputqueue-m-bbatchexact.md)         | Indicateur qui spécifie si l’objet fournit des exemples dans des lots exacts.                                |
| [**m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)           | Taille du lot.                                                                                              |
| [**\_liste m**](coutputqueue-m-list.md)                       | File d’attente de l’exemple de support.                                                                                      |
| [**m \_ hSem**](coutputqueue-m-hsem.md)                       | Handle vers un sémaphore, utilisé par le thread pour attendre des exemples.                                           |
| [**m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) | Événement qui signale quand une opération de vidage est terminée.                                                  |
| [**m \_ hThread**](coutputqueue-m-hthread.md)                 | Handle vers le thread de travail.                                                                             |
| [**m \_ ppSamples**](coutputqueue-m-ppsamples.md)             | Tableau d’exemples de taille [**COutputQueue :: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).               |
| [**m \_ nBatched**](coutputqueue-m-nbatched.md)               | Nombre d’échantillons actuellement traités par lot et en attente de traitement.                                             |
| [**m \_ lWaiting**](coutputqueue-m-lwaiting.md)               | Indicateur qui a une valeur différente de zéro lorsque le thread attend un échantillon.                                   |
| [**m \_ bFlushing**](coutputqueue-m-bflushing.md)             | Indicateur qui spécifie si l’objet effectue une opération de vidage.                                  |
| [**m \_ bTerminate**](coutputqueue-m-bterminate.md)           | Indicateur qui spécifie si le thread doit se terminer.                                                 |
| [**m \_ bSendAnyway**](coutputqueue-m-bsendanyway.md)         | Indicateur de remplacement du traitement par lots.                                                                       |
| [**m \_ h**](coutputqueue-m-hr.md)                           | Valeur **HRESULT** qui indique si l’objet accepte des exemples.                                 |
| [**m \_ hEventPop**](coutputqueue-m-heventpop.md)             | Événement signalé chaque fois que l’objet supprime un échantillon de la file d’attente.                              |
| Méthodes protégées                                            | Description                                                                                              |
| [**InitialThreadProc**](coutputqueue-initialthreadproc.md)  | Appelle la méthode [**COutputQueue :: ThreadProc**](coutputqueue-threadproc.md) lorsque le thread est créé. |
| [**ThreadProc**](coutputqueue-threadproc.md)                | Récupère des exemples de la file d’attente et les remet à la broche d’entrée.                                     |
| [**IsQueued**](coutputqueue-isqueued.md)                    | Détermine si l’objet utilise un thread de travail pour fournir des exemples.                               |
| [**QueueSample**](coutputqueue-queuesample.md)              | Met en file d’attente un exemple de média ou un message de contrôle.                                                                |
| [**IsSpecialSample**](coutputqueue-isspecialsample.md)      | Détermine si les données mises en file d’attente sont un message de contrôle.                                                     |
| [**FreeSamples**](coutputqueue-freesamples.md)              | Libère tous les exemples en attente.                                                                               |
| [**NotifyThread**](coutputqueue-notifythread.md)            | Notifie le thread que la file d’attente contient des données.                                                        |
| M&#233;thodes publiques                                               | Description                                                                                              |
| [**COutputQueue**](coutputqueue-coutputqueue.md)            | Méthode de constructeur.                                                                                      |
| [**~ COutputQueue**](coutputqueue--coutputqueue.md)          | Méthode de destructeur.                                                                                       |
| [**BeginFlush**](coutputqueue-beginflush.md)                | Commence une opération de vidage.                                                                                |
| [**EndFlush**](coutputqueue-endflush.md)                    | Termine une opération de vidage.                                                                                  |
| [**EOS**](coutputqueue-eos.md)                              | Fournit un appel de fin de flux à la broche d’entrée.                                                         |
| [**SendAnyway**](coutputqueue-sendanyway.md)                | Remet les exemples en attente.                                                                            |
| [**NewSegment**](coutputqueue-newsegment.md)                | Remet un nouveau segment à la broche d’entrée.                                                                 |
| [**Çoive**](coutputqueue-receive.md)                      | Remet un échantillon de média à la broche d’entrée.                                                                |
| [**ReceiveMultiple**](coutputqueue-receivemultiple.md)      | Remet un lot d’exemples de supports à la broche d’entrée.                                                      |
| [**Réinitialiser**](coutputqueue-reset.md)                          | Réinitialise l’objet afin qu’il puisse recevoir plus de données.                                                      |
| [**IsIdle**](coutputqueue-isidle.md)                        | Détermine si l’objet attend des données.                                                       |
| [**SetPopEvent**](coutputqueue-setpopevent.md)              | Spécifie un événement qui est signalé chaque fois que l’objet supprime un échantillon de la file d’attente.                 |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Outputq. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




