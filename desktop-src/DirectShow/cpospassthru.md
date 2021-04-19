---
description: La classe CPosPassThru gère les commandes de recherche pour les filtres de transformation, en les passant en amont au filtre suivant.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: CPosPassThru, classe (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523629"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="f6a18-103">CPosPassThru, classe</span><span class="sxs-lookup"><span data-stu-id="f6a18-103">CPosPassThru class</span></span>

![hiérarchie de la classe de base cpospassthru](images/cutil14.png)

<span data-ttu-id="f6a18-105">La `CPosPassThru` classe gère les commandes de recherche pour les filtres de transformation, en les passant en amont au filtre suivant.</span><span class="sxs-lookup"><span data-stu-id="f6a18-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="f6a18-106">Quand une application recherche le graphique de filtre, le gestionnaire de graphique de filtre donne la commande Seek aux filtres de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="f6a18-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="f6a18-107">La commande est passée en amont, via la broche de sortie de chaque filtre, jusqu’à ce qu’elle atteigne un filtre qui peut exécuter la commande (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="f6a18-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="f6a18-108">Pour plus d’informations, consultez [recherche](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="f6a18-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="f6a18-109">La `CPosPassThru` classe transmet toutes les commandes Seek à la broche de sortie sur le filtre en amont, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="f6a18-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![la classe cpospassthru envoie des commandes de recherche en amont.](images/cpospassthru.png)

<span data-ttu-id="f6a18-111">Bien que cette classe soit fournie dans la bibliothèque de classes de base, DirectShow fournit également la même classe dans Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="f6a18-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="f6a18-112">L’utilisation de la version Quartz.dll peut être légèrement réduite dans votre filtre, car la classe est chargée au moment de l’exécution à partir de la DLL.</span><span class="sxs-lookup"><span data-stu-id="f6a18-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="f6a18-113">Pour utiliser cette version, appelez la fonction [**CreatePosPassThru**](createpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="f6a18-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="f6a18-114">Dans la méthode **NonDelegatingQueryInterface** de votre code confidentiel de sortie, déléguez à l’objet **CPosPassThru** chaque fois que l’interface demandée est [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="f6a18-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="f6a18-115">Sauf indication contraire, toutes les méthodes [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) et [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de cette classe appellent la méthode correspondante sur l’épingle connectée et retournent le résultat.</span><span class="sxs-lookup"><span data-stu-id="f6a18-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="f6a18-116">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="f6a18-116">Public Methods</span></span>                                                    | <span data-ttu-id="f6a18-117">Description</span><span class="sxs-lookup"><span data-stu-id="f6a18-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6a18-118">**CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f6a18-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="f6a18-119">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f6a18-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="f6a18-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="f6a18-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="f6a18-121">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="f6a18-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="f6a18-122">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="f6a18-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="f6a18-123">Récupère les horodatages de l’échantillon actuel.</span><span class="sxs-lookup"><span data-stu-id="f6a18-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="f6a18-124">Virtuels.</span><span class="sxs-lookup"><span data-stu-id="f6a18-124">Virtual.</span></span>                                           |
| <span data-ttu-id="f6a18-125">Méthodes IMediaPosition</span><span class="sxs-lookup"><span data-stu-id="f6a18-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="f6a18-126">Description</span><span class="sxs-lookup"><span data-stu-id="f6a18-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="f6a18-127">**Obtient la \_ durée**</span><span class="sxs-lookup"><span data-stu-id="f6a18-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="f6a18-128">Récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="f6a18-129">**put \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="f6a18-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="f6a18-130">Définit la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="f6a18-131">**Obtient \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="f6a18-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="f6a18-132">Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="f6a18-133">**put \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="f6a18-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="f6a18-134">Définit l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="f6a18-135">**Obtient \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="f6a18-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="f6a18-136">Récupère la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="f6a18-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="f6a18-137">**put \_ PrerollTime**</span><span class="sxs-lookup"><span data-stu-id="f6a18-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="f6a18-138">Définit la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="f6a18-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="f6a18-139">**taux d’accès \_**</span><span class="sxs-lookup"><span data-stu-id="f6a18-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="f6a18-140">Récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="f6a18-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="f6a18-141">**taux de placement \_**</span><span class="sxs-lookup"><span data-stu-id="f6a18-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="f6a18-142">Définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="f6a18-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="f6a18-143">**Obtient \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="f6a18-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="f6a18-144">Récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="f6a18-145">**CanSeekForward**</span><span class="sxs-lookup"><span data-stu-id="f6a18-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="f6a18-146">Détermine si le flux peut être recherché en arrière.</span><span class="sxs-lookup"><span data-stu-id="f6a18-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="f6a18-147">**CanSeekBackward**</span><span class="sxs-lookup"><span data-stu-id="f6a18-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="f6a18-148">Détermine si le flux peut être recherché par progression.</span><span class="sxs-lookup"><span data-stu-id="f6a18-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="f6a18-149">Méthodes IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="f6a18-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="f6a18-150">Description</span><span class="sxs-lookup"><span data-stu-id="f6a18-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="f6a18-151">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f6a18-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="f6a18-152">Interroge si un flux a spécifié des fonctionnalités de recherche.</span><span class="sxs-lookup"><span data-stu-id="f6a18-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="f6a18-153">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f6a18-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="f6a18-154">Convertit d’un format d’heure en un autre.</span><span class="sxs-lookup"><span data-stu-id="f6a18-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="f6a18-155">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="f6a18-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="f6a18-156">Récupère la plage de temps pendant laquelle la recherche est efficace.</span><span class="sxs-lookup"><span data-stu-id="f6a18-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="f6a18-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f6a18-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="f6a18-158">Récupère toutes les fonctionnalités de recherche du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="f6a18-159">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="f6a18-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="f6a18-160">Récupère la position actuelle, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="f6a18-161">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="f6a18-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="f6a18-162">Récupère la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="f6a18-163">**GetPositions**</span><span class="sxs-lookup"><span data-stu-id="f6a18-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="f6a18-164">Récupère la position actuelle et la position d’arrêt, par rapport à la durée totale du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="f6a18-165">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="f6a18-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="f6a18-166">Récupère la quantité de données qui seront placées en file d’attente avant la position de début.</span><span class="sxs-lookup"><span data-stu-id="f6a18-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="f6a18-167">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="f6a18-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="f6a18-168">Récupère la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="f6a18-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="f6a18-169">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="f6a18-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="f6a18-170">Récupère l’heure à laquelle la lecture s’arrêtera, par rapport à la durée du flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="f6a18-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f6a18-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="f6a18-172">Récupère le format d’heure actuel.</span><span class="sxs-lookup"><span data-stu-id="f6a18-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="f6a18-173">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="f6a18-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="f6a18-174">Détermine si un format d’heure spécifié est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f6a18-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="f6a18-175">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f6a18-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="f6a18-176">Détermine si un format d’heure spécifié est le format en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f6a18-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="f6a18-177">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="f6a18-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="f6a18-178">Récupère le format d’heure par défaut pour le flux.</span><span class="sxs-lookup"><span data-stu-id="f6a18-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="f6a18-179">**SetPositions**</span><span class="sxs-lookup"><span data-stu-id="f6a18-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="f6a18-180">Définit la position actuelle et la position d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f6a18-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="f6a18-181">**Seles**</span><span class="sxs-lookup"><span data-stu-id="f6a18-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="f6a18-182">Définit la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="f6a18-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="f6a18-183">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f6a18-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="f6a18-184">Définit le format d’heure.</span><span class="sxs-lookup"><span data-stu-id="f6a18-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="f6a18-185">Fonctions d’assistance</span><span class="sxs-lookup"><span data-stu-id="f6a18-185">Helper Functions</span></span>                                                  | <span data-ttu-id="f6a18-186">Description</span><span class="sxs-lookup"><span data-stu-id="f6a18-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="f6a18-187">**CreatePosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f6a18-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="f6a18-188">Crée un `CPosPassThru` objet ou [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="f6a18-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="f6a18-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6a18-189">Requirements</span></span>



| <span data-ttu-id="f6a18-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6a18-190">Requirement</span></span> | <span data-ttu-id="f6a18-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6a18-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a18-192">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6a18-192">Header</span></span><br/>  | <dl> <span data-ttu-id="f6a18-193"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f6a18-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f6a18-194">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f6a18-194">Library</span></span><br/> | <dl> <span data-ttu-id="f6a18-195"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f6a18-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




