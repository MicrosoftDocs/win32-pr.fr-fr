---
description: L’exemple de filtre d’accrochage permet de récupérer des exemples au fur et à mesure qu’ils passent par le graphique de filtre.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Exemple de filtre d’accrochage (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909667"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="3678b-103">Exemple de filtre d’accrochage</span><span class="sxs-lookup"><span data-stu-id="3678b-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="3678b-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3678b-104">\[Deprecated.</span></span> <span data-ttu-id="3678b-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3678b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3678b-106">L’exemple de filtre d’accrochage permet de récupérer des exemples au fur et à mesure qu’ils passent par le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="3678b-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="3678b-107">Il s’agit d’un filtre de transformation avec une broche d’entrée et une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="3678b-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="3678b-108">Il passe tous les exemples en aval inchangés, de sorte que vous pouvez l’insérer dans un graphique de filtre sans modifier le flux de données.</span><span class="sxs-lookup"><span data-stu-id="3678b-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="3678b-109">Votre application peut ensuite récupérer des échantillons individuels à partir du filtre en appelant des méthodes sur l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="3678b-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="3678b-110">Si vous souhaitez récupérer des exemples sans restituer les données, connectez le filtre d’accroche d’échantillon au filtre de [**convertisseur null**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3678b-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



| <span data-ttu-id="3678b-111">Étiquette</span><span class="sxs-lookup"><span data-stu-id="3678b-111">Label</span></span> | <span data-ttu-id="3678b-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3678b-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3678b-113">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="3678b-113">Filter interfaces</span></span>                        | <span data-ttu-id="3678b-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="3678b-114">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="3678b-115">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="3678b-115">Input pin media types</span></span>                    | <span data-ttu-id="3678b-116">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="3678b-116">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="3678b-117">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="3678b-117">Input pin interfaces</span></span>                     | <span data-ttu-id="3678b-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3678b-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="3678b-119">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3678b-119">Output pin media types</span></span>                   | <span data-ttu-id="3678b-120">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="3678b-120">Any media type.</span></span> <span data-ttu-id="3678b-121">Correspond au type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3678b-121">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="3678b-122">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="3678b-122">Output pin interfaces</span></span>                    | <span data-ttu-id="3678b-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3678b-123">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3678b-124">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="3678b-124">Filter CLSID</span></span>                             | <span data-ttu-id="3678b-125">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="3678b-125">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="3678b-126">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="3678b-126">Property Page CLSID</span></span>                      | <span data-ttu-id="3678b-127">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="3678b-127">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="3678b-128">Exécutable</span><span class="sxs-lookup"><span data-stu-id="3678b-128">Executable</span></span>                               | <span data-ttu-id="3678b-129">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="3678b-129">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="3678b-130">Mérite</span><span class="sxs-lookup"><span data-stu-id="3678b-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="3678b-131">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="3678b-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="3678b-132">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="3678b-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3678b-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="3678b-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="3678b-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="3678b-134">Remarks</span></span>

<span data-ttu-id="3678b-135">Pour utiliser ce filtre, ajoutez-le au graphique de filtre et appelez [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) avec le type de média souhaité.</span><span class="sxs-lookup"><span data-stu-id="3678b-135">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="3678b-136">Cette méthode spécifie le type de média pour les connexions de broche d’entrée et de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="3678b-136">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="3678b-137">Connectez ensuite le filtre à d’autres filtres dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="3678b-137">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="3678b-138">Si vous appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**, le filtre met en mémoire tampon chaque échantillon qu’il reçoit avant de le passer en aval.</span><span class="sxs-lookup"><span data-stu-id="3678b-138">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="3678b-139">Appelez la méthode [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) pour récupérer le contenu actuel de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3678b-139">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="3678b-140">Vous pouvez également appeler [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md) pour que le filtre appelle une fonction de rappel chaque fois qu’il reçoit un exemple.</span><span class="sxs-lookup"><span data-stu-id="3678b-140">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="3678b-141">Le filtre présente les limitations suivantes pour les formats vidéo :</span><span class="sxs-lookup"><span data-stu-id="3678b-141">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="3678b-142">Il ne prend pas en charge les types vidéo avec une orientation verticale ( **bihauteur** négative).</span><span class="sxs-lookup"><span data-stu-id="3678b-142">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="3678b-143">Elle ne prend pas en charge la structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (type de format égal au **format \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="3678b-143">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="3678b-144">Elle rejette tout type de vidéo dans lequel le Stride de la surface ne correspond pas à la largeur de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="3678b-144">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="3678b-145">Par conséquent, la accroche d’échantillon ne se connecte pas au convertisseur de mixage vidéo (VMR) pour certains types de vidéo.</span><span class="sxs-lookup"><span data-stu-id="3678b-145">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="3678b-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3678b-146">Requirements</span></span>



| <span data-ttu-id="3678b-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3678b-147">Requirement</span></span> | <span data-ttu-id="3678b-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3678b-148">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3678b-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="3678b-149">Header</span></span><br/> | <dl> <span data-ttu-id="3678b-150"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="3678b-150"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3678b-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3678b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3678b-152">Objets des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="3678b-152">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="3678b-153">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="3678b-153">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




