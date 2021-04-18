---
description: Synchronisation des commandes de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Synchronisation des commandes de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526289"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="95b65-103">Synchronisation des commandes de DVD</span><span class="sxs-lookup"><span data-stu-id="95b65-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="95b65-104">Les commandes de DVD ne se terminent pas toujours instantanément.</span><span class="sxs-lookup"><span data-stu-id="95b65-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="95b65-105">Pour cette raison, certaines méthodes de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sont asynchrones.</span><span class="sxs-lookup"><span data-stu-id="95b65-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="95b65-106">Celles-ci incluent des méthodes de lecture, telles que **PlayTitle**, et des méthodes de navigation dans les menus, telles que **ShowMenu** et **ReturnFromSubmenu**.</span><span class="sxs-lookup"><span data-stu-id="95b65-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="95b65-107">Une méthode asynchrone est retournée immédiatement, sans attendre la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="95b65-108">Une fois la méthode retournée, d’autres événements peuvent empêcher l’exécution de la commande, même si la méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="95b65-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="95b65-109">DirectShow offre plusieurs options de synchronisation des commandes, allant de la synchronisation à la synchronisation complète à l’aide d’événements de graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="95b65-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="95b65-110">Toutes les méthodes asynchrones ont un paramètre *dwFlags* et un paramètre *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="95b65-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="95b65-111">Le paramètre *dwFlags* spécifie le comportement de synchronisation, et le paramètre *ppCmd* retourne un pointeur vers un objet de synchronisation facultatif.</span><span class="sxs-lookup"><span data-stu-id="95b65-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="95b65-112">Des comportements différents se produisent selon les valeurs que vous donnez à ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="95b65-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="95b65-113">**Aucune synchronisation**</span><span class="sxs-lookup"><span data-stu-id="95b65-113">**No Synchronization**</span></span>

<span data-ttu-id="95b65-114">Pour une application de lecture de DVD de base, la meilleure option consiste à ignorer les problèmes de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="95b65-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="95b65-115">Parfois, une commande peut échouer ou l’interface utilisateur peut être légèrement décalée lors de la mise à jour, mais ces erreurs sont de l’ordre des fractions de seconde.</span><span class="sxs-lookup"><span data-stu-id="95b65-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="95b65-116">Pour émettre une commande sans synchronisation, définissez l’indicateur DVD \_ cmd \_ \_ None dans le paramètre *dwFlags* et définissez le paramètre *ppCmd* sur la **valeur null**:</span><span class="sxs-lookup"><span data-stu-id="95b65-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="95b65-117">**Blocage**</span><span class="sxs-lookup"><span data-stu-id="95b65-117">**Blocking**</span></span>

<span data-ttu-id="95b65-118">Si vous définissez l' \_ \_ \_ \_ indicateur de bloc d’indicateur cmd DVD cmd dans le paramètre *dwFlags* , la méthode se bloque jusqu’à la fin de l’exécution de la commande :</span><span class="sxs-lookup"><span data-stu-id="95b65-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="95b65-119">En effet, cet indicateur convertit une méthode asynchrone en méthode synchrone.</span><span class="sxs-lookup"><span data-stu-id="95b65-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="95b65-120">L’inconvénient est que votre interface utilisateur est bloquée si vous appelez la méthode à partir du thread d’application.</span><span class="sxs-lookup"><span data-stu-id="95b65-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="95b65-121">**Objet de synchronisation**</span><span class="sxs-lookup"><span data-stu-id="95b65-121">**Synchronization Object**</span></span>

<span data-ttu-id="95b65-122">Toutes les méthodes asynchrones peuvent retourner un objet de synchronisation, que vous pouvez utiliser pour attendre le début ou la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="95b65-123">Pour récupérer cet objet, transmettez l’adresse d’un pointeur [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) dans le paramètre *ppCmd* :</span><span class="sxs-lookup"><span data-stu-id="95b65-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="95b65-124">Si la méthode est réussie, elle retourne un nouvel objet **IDvdCmd** .</span><span class="sxs-lookup"><span data-stu-id="95b65-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="95b65-125">La méthode [**IDvdCmd :: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) se bloque jusqu’à ce que la commande commence, et la méthode [**IDvdCmd :: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) se bloque jusqu’à la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="95b65-126">La valeur de retour indique l’état de la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="95b65-127">Le code suivant est fonctionnellement équivalent à la définition de \_ l' \_ indicateur de bloc d’indicateur cmd DVD cmd \_ \_ , indiqué précédemment.</span><span class="sxs-lookup"><span data-stu-id="95b65-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="95b65-128">Dans ce cas, la méthode **PlayTitle** n’est pas bloquée, mais l’application bloque en appelant **WaitForEnd**.</span><span class="sxs-lookup"><span data-stu-id="95b65-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="95b65-129">**Événements d’état de la commande**</span><span class="sxs-lookup"><span data-stu-id="95b65-129">**Command Status Events**</span></span>

<span data-ttu-id="95b65-130">Si vous définissez l' \_ \_ \_ indicateur SendEvents de l’indicateur de commande de DVD dans le paramètre *DWFLAGS* , le navigateur DVD envoie un événement de démarrage de la commande de DVD de l’ensemble des DVD lors du [**\_ \_ \_ démarrage**](ec-dvd-cmd-start.md) de la commande et un événement de fin de la commande de [**\_ DVD \_ cmd \_**](ec-dvd-cmd-end.md) à la fin de la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="95b65-131">Le paramètre *lParam2* de l’événement est la valeur de retour HRESULT pour la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="95b65-132">Le paramètre *lParam1* de l’événement permet d’obtenir l’objet de synchronisation pour la commande.</span><span class="sxs-lookup"><span data-stu-id="95b65-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="95b65-133">Si vous transmettez *lParam1* à la méthode [**IDvdInfo2 :: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , la méthode retourne un pointeur vers l’interface **IDvdCmd** de l’objet de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="95b65-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="95b65-134">Vous pouvez utiliser cette interface pour attendre la fin de la commande, comme décrit précédemment.</span><span class="sxs-lookup"><span data-stu-id="95b65-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="95b65-135">Toutefois, si vous avez passé **null** pour le paramètre *ppCmd* dans la méthode **IDvdControl2** d’origine, le navigateur DVD ne crée pas d’objet de synchronisation, et **GetCmdFromEvent** retourne E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="95b65-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="95b65-136">Le code suivant montre comment utiliser des événements d’état de commande sans objet de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="95b65-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="95b65-137">Notez que sans objet de synchronisation, vous ne pouvez pas déterminer quelle commande est associée à l’événement.</span><span class="sxs-lookup"><span data-stu-id="95b65-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="95b65-138">Le code suivant montre comment utiliser des événements avec l’objet de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="95b65-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="95b65-139">L’idée est de stocker les objets de synchronisation dans une liste, puis de comparer les pointeurs d’objet lorsque vous obtenez l’événement de fin [**de la commande de DVD ou de \_ \_ \_**](ec-dvd-cmd-start.md) fin de la [**\_ \_ commande \_ de DVD**](ec-dvd-cmd-end.md) de l’EC.</span><span class="sxs-lookup"><span data-stu-id="95b65-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="95b65-140">**Vidage des mémoires tampons du navigateur DVD**</span><span class="sxs-lookup"><span data-stu-id="95b65-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="95b65-141">Pendant la lecture, le navigateur DVD met en mémoire tampon les données vidéo.</span><span class="sxs-lookup"><span data-stu-id="95b65-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="95b65-142">La quantité de données mises en mémoire tampon varie.</span><span class="sxs-lookup"><span data-stu-id="95b65-142">The amount of buffered data varies.</span></span> <span data-ttu-id="95b65-143">Lorsque le navigateur DVD bascule sur un nouveau morceau de vidéo, les données qui se trouvent déjà dans le pipeline ne sont pas perdues, donc la transition est transparente.</span><span class="sxs-lookup"><span data-stu-id="95b65-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="95b65-144">Par défaut, lorsque le navigateur DVD émet une commande, il ne vide pas les données qui se trouvent déjà dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="95b65-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="95b65-145">Par conséquent, il peut y avoir une certaine latence avant que vous puissiez voir l’effet de la commande, en fonction de la quantité de données mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="95b65-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="95b65-146">Pour augmenter la réactivité, vous pouvez forcer le vidage du navigateur DVD en définissant l' \_ indicateur de vidage de l’indicateur de commande DVD cmd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="95b65-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="95b65-147">Cet indicateur peut être combiné avec l’un des indicateurs décrits précédemment, à l’aide d’une opération or au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="95b65-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="95b65-148">L’un des effets secondaires du vidage est que certaines vidéos peuvent être perdues. n’utilisez donc pas cet indicateur si vous devez garantir qu’il n’y a pas d’écart dans la vidéo.</span><span class="sxs-lookup"><span data-stu-id="95b65-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95b65-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95b65-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95b65-150">Applications DVD</span><span class="sxs-lookup"><span data-stu-id="95b65-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



