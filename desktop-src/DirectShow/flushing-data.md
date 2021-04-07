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
# <a name="flushing-data"></a><span data-ttu-id="dd1aa-103">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="dd1aa-103">Flushing Data</span></span>

<span data-ttu-id="dd1aa-104">Le pseudo-code suivant montre comment implémenter la méthode [**IPIN :: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) :</span><span class="sxs-lookup"><span data-stu-id="dd1aa-104">The following pseudocode shows how to implement the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method:</span></span>


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



<span data-ttu-id="dd1aa-105">Lors du démarrage du vidage, la méthode **BeginFlush** prend le verrou de filtre, qui sérialise le changement d’État.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-105">When flushing starts, the **BeginFlush** method takes the filter lock, which serializes the state change.</span></span> <span data-ttu-id="dd1aa-106">Il n’est pas encore possible de prendre le verrou de diffusion en continu, car le vidage se produit sur le thread d’application et le thread de streaming peut être au milieu d’un appel de **réception** .</span><span class="sxs-lookup"><span data-stu-id="dd1aa-106">It is not yet safe to take the streaming lock, because flushing happens on the application thread, and the streaming thread might be in the middle of a **Receive** call.</span></span> <span data-ttu-id="dd1aa-107">Le code confidentiel doit garantir que la **réception** n’est pas bloquée et que les appels suivants à la **réception** échoueront.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-107">The pin needs to guarantee that **Receive** is not blocked, and that any subsequent calls to **Receive** will fail.</span></span> <span data-ttu-id="dd1aa-108">La méthode [**CBaseInputPin :: BeginFlush**](cbaseinputpin-beginflush.md) définit un indicateur interne, [**CBaseInputPin :: m \_ bFlushing**](cbaseinputpin-m-bflushing.md).</span><span class="sxs-lookup"><span data-stu-id="dd1aa-108">The [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method sets an internal flag, [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md).</span></span> <span data-ttu-id="dd1aa-109">Lorsque l’indicateur a la **valeur true**, la méthode **Receive** échoue.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-109">When the flag is **TRUE**, the **Receive** method fails.</span></span>

<span data-ttu-id="dd1aa-110">En remettant l’appel **BeginFlush** en aval, le code PIN garantit que tous les filtres en aval libèrent leurs exemples et retournent des appels de **réception** .</span><span class="sxs-lookup"><span data-stu-id="dd1aa-110">By delivering the **BeginFlush** call downstream, the pin guarantees that all downstream filters release their samples and return from **Receive** calls.</span></span> <span data-ttu-id="dd1aa-111">Cela garantit à son tour que la broche d’entrée n’est pas bloquée en attente de **GetBuffer** ou de **réception**.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-111">This in turn guarantees that the input pin is not blocked waiting for **GetBuffer** or **Receive**.</span></span> <span data-ttu-id="dd1aa-112">Si la méthode de **réception** de votre PIN attend un événement (par exemple, pour obtenir des ressources), la méthode **BeginFlush** doit forcer l’arrêt de l’attente en définissant l’événement.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-112">If your pin's **Receive** method ever waits on an event (for example, to get resources), the **BeginFlush** method should force the wait to terminate by setting the event.</span></span> <span data-ttu-id="dd1aa-113">À ce stade, le retour de la méthode **Receive** est garanti, et l’indicateur **m \_ bFlushing** empêche les nouveaux appels de **réception** d’effectuer n’importe quel travail.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-113">At this point, the **Receive** method is guaranteed to return, and the **m\_bFlushing** flag prevents new **Receive** calls from doing any work.</span></span>

<span data-ttu-id="dd1aa-114">Pour certains filtres, c’est tout ce que **BeginFlush** doit faire.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-114">For some filters, that is all **BeginFlush** needs to do.</span></span> <span data-ttu-id="dd1aa-115">La méthode **EndFlush** indique au filtre qu’il peut recommencer à recevoir des exemples.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-115">The **EndFlush** method will signal to the filter that it can start receiving samples again.</span></span> <span data-ttu-id="dd1aa-116">D’autres filtres peuvent avoir besoin d’utiliser des variables ou des ressources dans des **BeginFlush** qui sont également utilisées dans **Receive**.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-116">Other filters may need to use variables or resources in **BeginFlush** that are also used in **Receive**.</span></span> <span data-ttu-id="dd1aa-117">Dans ce cas, le filtre doit d’abord conserver le verrou de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-117">In that case, the filter should hold the streaming lock first.</span></span> <span data-ttu-id="dd1aa-118">Veillez à ne pas effectuer cette opération avant l’une des étapes précédentes, car vous risquez de provoquer un blocage.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-118">Be sure not to do this before any of the previous steps, because you might cause a deadlock.</span></span>

<span data-ttu-id="dd1aa-119">La méthode **EndFlush** maintient le verrou de filtre et propage l’appel en aval :</span><span class="sxs-lookup"><span data-stu-id="dd1aa-119">The **EndFlush** method holds the filter lock and propagates the call downstream:</span></span>


```C++
HRESULT CMyInputPin::EndFlush()
{
    CAutoLock lock_it(m_pLock);
    for (each output pin)
        hr = pOutputPin->DeliverEndFlush();
    return CBaseInputPin::EndFlush();
}
```



<span data-ttu-id="dd1aa-120">La méthode [**CBaseInputPin :: EndFlush**](cbaseinputpin-endflush.md) réinitialise l’indicateur **m \_ bFlushing** sur **false**, ce qui permet à la méthode **Receive** de commencer à recevoir des exemples.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-120">The [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method resets the **m\_bFlushing** flag to **FALSE**, which allows the **Receive** method to start receiving samples again.</span></span> <span data-ttu-id="dd1aa-121">Il doit s’agir de la dernière étape de **EndFlush**, car le code confidentiel ne doit pas recevoir d’exemples tant que le vidage n’est pas terminé et que tous les filtres en aval sont avertis.</span><span class="sxs-lookup"><span data-stu-id="dd1aa-121">This should be the last step in **EndFlush**, because the pin must not receive any samples until flushing is complete and all downstream filters are notified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd1aa-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dd1aa-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1aa-123">Threads et sections critiques</span><span class="sxs-lookup"><span data-stu-id="dd1aa-123">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 



