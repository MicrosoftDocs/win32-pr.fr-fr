---
description: Vidage des données
ms.assetid: 528763a2-c0f2-4981-91dc-dd17987f5bd5
title: Vidage des données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ddd052c18928d53511d9e955122d2d66ee59d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745636"
---
# <a name="flushing-data"></a>Vidage des données

Le pseudo-code suivant montre comment implémenter la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :


```C++
HRESULT CMyInputPin::BeginFlush()
{
    CAutoLock lock_it(m_pLock);
   
    // First, make sure the Receive method will fail from now on.
    HRESULT hr = CBaseInputPin::BeginFlush();
    
    // Force downstream filters to release samples. If our Receive method
    // is blocked in GetBuffer or Deliver, this will unblock it.
    for (each output pin)
    {
        hr = pOutputPin->DeliverBeginFlush();
    }

    // Unblock our Receive method if it is waiting on an event.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // At this point, the Receive method can't be blocked. Make sure 
    // it finishes, by taking the streaming lock. (Not necessary if this 
    // is the last step.)
    { 
        CAutoLock lock_2(&m_csReceive);

        /* Now it's safe to do anything that would crash or hang 
           if Receive were executing. */
    }
    return hr;
}
```



Lors du démarrage du vidage, la méthode **BeginFlush** prend le verrou de filtre, qui sérialise le changement d’État. Il n’est pas encore possible de prendre le verrou de diffusion en continu, car le vidage se produit sur le thread d’application et le thread de streaming peut être au milieu d’un appel de **réception** . Le code confidentiel doit garantir que la **réception** n’est pas bloquée et que les appels suivants à la **réception** échoueront. La méthode [**CBaseInputPin :: BeginFlush**](cbaseinputpin-beginflush.md) définit un indicateur interne, [**CBaseInputPin :: m \_ bFlushing**](cbaseinputpin-m-bflushing.md). Lorsque l’indicateur a la **valeur true**, la méthode **Receive** échoue.

En remettant l’appel **BeginFlush** en aval, le code PIN garantit que tous les filtres en aval libèrent leurs exemples et retournent des appels de **réception** . Cela garantit à son tour que la broche d’entrée n’est pas bloquée en attente de **GetBuffer** ou de **réception**. Si la méthode de **réception** de votre PIN attend un événement (par exemple, pour obtenir des ressources), la méthode **BeginFlush** doit forcer l’arrêt de l’attente en définissant l’événement. À ce stade, le retour de la méthode **Receive** est garanti, et l’indicateur **m \_ bFlushing** empêche les nouveaux appels de **réception** d’effectuer n’importe quel travail.

Pour certains filtres, c’est tout ce que **BeginFlush** doit faire. La méthode **EndFlush** indique au filtre qu’il peut recommencer à recevoir des exemples. D’autres filtres peuvent avoir besoin d’utiliser des variables ou des ressources dans des **BeginFlush** qui sont également utilisées dans **Receive**. Dans ce cas, le filtre doit d’abord conserver le verrou de diffusion en continu. Veillez à ne pas effectuer cette opération avant l’une des étapes précédentes, car vous risquez de provoquer un blocage.

La méthode **EndFlush** maintient le verrou de filtre et propage l’appel en aval :


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



La méthode [**CBaseInputPin :: EndFlush**](cbaseinputpin-endflush.md) réinitialise l’indicateur **m \_ bFlushing** sur **false**, ce qui permet à la méthode **Receive** de commencer à recevoir des exemples. Il doit s’agir de la dernière étape de **EndFlush**, car le code confidentiel ne doit pas recevoir d’exemples tant que le vidage n’est pas terminé et que tous les filtres en aval sont avertis.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Threads et sections critiques](threads-and-critical-sections.md)
</dt> </dl>

 

 



