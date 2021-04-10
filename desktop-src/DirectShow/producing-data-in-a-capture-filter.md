---
description: Cette rubrique décrit comment un filtre de capture DirectShow personnalisé doit générer des données de sortie.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Génération de données dans un filtre de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950217"
---
# <a name="producing-data-in-a-capture-filter"></a><span data-ttu-id="04b2b-103">Génération de données dans un filtre de capture</span><span class="sxs-lookup"><span data-stu-id="04b2b-103">Producing Data in a Capture Filter</span></span>

<span data-ttu-id="04b2b-104">Cette rubrique décrit comment un filtre de capture DirectShow personnalisé doit générer des données de sortie.</span><span class="sxs-lookup"><span data-stu-id="04b2b-104">This topic describes how a custom DirectShow capture filter should generate output data.</span></span>

## <a name="filter-state-changes"></a><span data-ttu-id="04b2b-105">Modifications de l’état du filtre</span><span class="sxs-lookup"><span data-stu-id="04b2b-105">Filter State Changes</span></span>

<span data-ttu-id="04b2b-106">Un filtre de capture doit produire des données uniquement lorsque le filtre est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="04b2b-106">A capture filter should produce data only when the filter is running.</span></span> <span data-ttu-id="04b2b-107">N’envoyez pas de données à partir de vos codes confidentiels lorsque le filtre est suspendu.</span><span class="sxs-lookup"><span data-stu-id="04b2b-107">Do not send data from your pins when the filter is paused.</span></span> <span data-ttu-id="04b2b-108">Retournez également **VFW S ne peut pas être \_ \_ \_** renvoyé à partir de la méthode [**CBaseFilter :: GetState**](cbasefilter-getstate.md) lorsque le filtre est suspendu.</span><span class="sxs-lookup"><span data-stu-id="04b2b-108">Also, return **VFW\_S\_CANT\_CUE** from the [**CBaseFilter::GetState**](cbasefilter-getstate.md) method when the filter is paused.</span></span> <span data-ttu-id="04b2b-109">Cette valeur de retour indique au gestionnaire de graphique de filtre qu’il ne doit pas attendre les données de votre filtre pendant que le filtre est suspendu.</span><span class="sxs-lookup"><span data-stu-id="04b2b-109">This return value informs the Filter Graph Manager that it should not wait for any data from your filter while the filter is paused.</span></span> <span data-ttu-id="04b2b-110">Pour plus d’informations, consultez [États de filtre](filter-states.md).</span><span class="sxs-lookup"><span data-stu-id="04b2b-110">For more information, see [Filter States](filter-states.md).</span></span>

<span data-ttu-id="04b2b-111">Le code suivant montre comment implémenter la méthode [**IMediaFilter :: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) :</span><span class="sxs-lookup"><span data-stu-id="04b2b-111">The following code shows how to implement the [**IMediaFilter::GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) method:</span></span>


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a><span data-ttu-id="04b2b-112">Contrôle de flux individuels</span><span class="sxs-lookup"><span data-stu-id="04b2b-112">Controlling Individual Streams</span></span>

<span data-ttu-id="04b2b-113">Les broches de sortie d’un filtre de capture doivent prendre en charge l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) , afin qu’une application puisse activer ou désactiver chaque pin individuellement.</span><span class="sxs-lookup"><span data-stu-id="04b2b-113">A capture filter's output pins should support the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface, so that an application can turn each pin on or off individually.</span></span> <span data-ttu-id="04b2b-114">Par exemple, une application peut afficher un aperçu sans capture, puis passer en mode capture sans reconstruire le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="04b2b-114">For example, an application can preview without capturing, and then switch to capture mode without rebuilding the filter graph.</span></span> <span data-ttu-id="04b2b-115">Vous pouvez utiliser la classe [**CBaseStreamControl**](cbasestreamcontrol.md) pour implémenter cette interface.</span><span class="sxs-lookup"><span data-stu-id="04b2b-115">You can use the [**CBaseStreamControl**](cbasestreamcontrol.md) class to implement this interface.</span></span>

## <a name="time-stamps"></a><span data-ttu-id="04b2b-116">Horodatages</span><span class="sxs-lookup"><span data-stu-id="04b2b-116">Time Stamps</span></span>

<span data-ttu-id="04b2b-117">Quand le filtre capture un exemple, horodatage l’exemple avec l’heure actuelle du flux.</span><span class="sxs-lookup"><span data-stu-id="04b2b-117">When the filter captures a sample, time stamp the sample with the current stream time.</span></span> <span data-ttu-id="04b2b-118">L’heure de fin est l’heure de début plus la durée.</span><span class="sxs-lookup"><span data-stu-id="04b2b-118">The end time is the start time plus the duration.</span></span> <span data-ttu-id="04b2b-119">Par exemple, si le filtre capture 10 échantillons par seconde et que la durée du flux est de 200 millions unités lorsque le filtre capture l’échantillon, les horodatages doivent être 200 millions et 201 millions.</span><span class="sxs-lookup"><span data-stu-id="04b2b-119">For example, if the filter is capturing at ten samples per second, and the stream time is 200,000,000 units when the filter captures the sample, the time stamps should be 200000000 and 201000000.</span></span> <span data-ttu-id="04b2b-120">(Il y a 10 millions unités par seconde.)</span><span class="sxs-lookup"><span data-stu-id="04b2b-120">(There are 10,000,000 units per second.)</span></span>

<span data-ttu-id="04b2b-121">Pour calculer le temps de flux, appelez la méthode [**IReferenceClock :: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) pour obtenir le temps de référence actuel, puis soustraction l’heure de début d’origine.</span><span class="sxs-lookup"><span data-stu-id="04b2b-121">To calculate the stream time, call the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method to get the current reference time, and then substract the original start time.</span></span> <span data-ttu-id="04b2b-122">Vous pouvez également appeler la méthode [**CBaseFilter :: StreamTime**](cbasefilter-streamtime.md) , qui effectue le même calcul.</span><span class="sxs-lookup"><span data-stu-id="04b2b-122">Alternatively, call the [**CBaseFilter::StreamTime**](cbasefilter-streamtime.md) method, which performs the same calculation.</span></span> <span data-ttu-id="04b2b-123">Pour définir l’horodatage sur un exemple, appelez la méthode [**IMediaSample :: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) .</span><span class="sxs-lookup"><span data-stu-id="04b2b-123">To set the time stamp on a sample, call the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

<span data-ttu-id="04b2b-124">Toutefois, si le filtre a un code pin d’aperçu, les exemples du code PIN de préversion ne doivent pas avoir de datage.</span><span class="sxs-lookup"><span data-stu-id="04b2b-124">If the filter has a preview pin, however, samples from the preview pin should not have time stamps.</span></span> <span data-ttu-id="04b2b-125">En effet, les exemples atteindront toujours le convertisseur légèrement après l’heure de la capture.</span><span class="sxs-lookup"><span data-stu-id="04b2b-125">The reason is that samples will always reach the renderer slightly after the time of capture.</span></span> <span data-ttu-id="04b2b-126">Si les exemples sont horodatés, le convertisseur les traite comme tard et peut tenter de rattraper le problème en supprimant des exemples.</span><span class="sxs-lookup"><span data-stu-id="04b2b-126">If the samples are time stamped, the renderer will treat them as late, and it may try to catch up by dropping samples.</span></span> <span data-ttu-id="04b2b-127">(Pour plus d’informations, consultez [filtres de capture vidéo DirectShow](directshow-video-capture-filters.md).) Notez que l’interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) requiert le code confidentiel pour effectuer le suivi des temps d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="04b2b-127">(For more information, see [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Note that the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface requires the pin to keep track of sample times.</span></span> <span data-ttu-id="04b2b-128">Pour un code pin d’aperçu, vous devrez peut-être modifier l’implémentation afin qu’elle ne repose pas sur les horodatages.</span><span class="sxs-lookup"><span data-stu-id="04b2b-128">For a preview pin, you might need to modify the implementation so that it does not rely on time stamps.</span></span>

<span data-ttu-id="04b2b-129">Les horodatages doivent toujours augmenter d’un échantillon à l’autre.</span><span class="sxs-lookup"><span data-stu-id="04b2b-129">Time stamps must always increase from one sample to the next.</span></span> <span data-ttu-id="04b2b-130">Cela est vrai même lorsque le filtre est suspendu.</span><span class="sxs-lookup"><span data-stu-id="04b2b-130">This is true even when the filter pauses.</span></span> <span data-ttu-id="04b2b-131">Si le filtre est exécuté, s’interrompt, puis s’exécute à nouveau, le premier échantillon après la pause doit avoir un horodatage plus grand que le dernier échantillon avant la pause.</span><span class="sxs-lookup"><span data-stu-id="04b2b-131">If the filter runs, pauses, and then runs again, the first sample after the pause must have a larger time stamp than the last sample before the pause.</span></span>

<span data-ttu-id="04b2b-132">En fonction des données que vous capturez, il peut être utile de définir l’heure du média sur les échantillons.</span><span class="sxs-lookup"><span data-stu-id="04b2b-132">Depending on the data you are capturing, it might be appropriate to set the media time on the samples.</span></span>

<span data-ttu-id="04b2b-133">Pour plus d’informations, consultez [heure et horloges dans DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="04b2b-133">For more information, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="04b2b-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04b2b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04b2b-135">Filtres de capture vidéo DirectShow</span><span class="sxs-lookup"><span data-stu-id="04b2b-135">DirectShow Video Capture Filters</span></span>](directshow-video-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="04b2b-136">Temps et horloges dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="04b2b-136">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="04b2b-137">Écriture de filtres de capture</span><span class="sxs-lookup"><span data-stu-id="04b2b-137">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



