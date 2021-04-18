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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532744"
---
# <a name="sample-grabber-filter"></a><span data-ttu-id="da2a9-103">Exemple de filtre d’accrochage</span><span class="sxs-lookup"><span data-stu-id="da2a9-103">Sample Grabber Filter</span></span>

> [!Note]  
> <span data-ttu-id="da2a9-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="da2a9-104">\[Deprecated.</span></span> <span data-ttu-id="da2a9-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="da2a9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="da2a9-106">L’exemple de filtre d’accrochage permet de récupérer des exemples au fur et à mesure qu’ils passent par le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="da2a9-106">The Sample Grabber filter provides a way to retrieve samples as they pass through the filter graph.</span></span> <span data-ttu-id="da2a9-107">Il s’agit d’un filtre de transformation avec une broche d’entrée et une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="da2a9-107">It is a transform filter with one input pin and one output pin.</span></span> <span data-ttu-id="da2a9-108">Il passe tous les exemples en aval inchangés, de sorte que vous pouvez l’insérer dans un graphique de filtre sans modifier le flux de données.</span><span class="sxs-lookup"><span data-stu-id="da2a9-108">It passes all samples downstream unchanged, so you can insert it into a filter graph without altering the data stream.</span></span> <span data-ttu-id="da2a9-109">Votre application peut ensuite récupérer des échantillons individuels à partir du filtre en appelant des méthodes sur l’interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="da2a9-109">Your application can then retrieve individual samples from the filter by calling methods on the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>

<span data-ttu-id="da2a9-110">Si vous souhaitez récupérer des exemples sans restituer les données, connectez le filtre d’accroche d’échantillon au filtre de [**convertisseur null**](null-renderer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="da2a9-110">If you want to retrieve samples without rendering the data, connect the Sample Grabber filter to the [**Null Renderer**](null-renderer-filter.md) filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da2a9-111">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="da2a9-111">Filter interfaces</span></span>                        | <span data-ttu-id="da2a9-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)</span><span class="sxs-lookup"><span data-stu-id="da2a9-112">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ISampleGrabber**](isamplegrabber.md)</span></span>                                                                       |
| <span data-ttu-id="da2a9-113">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="da2a9-113">Input pin media types</span></span>                    | <span data-ttu-id="da2a9-114">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="da2a9-114">Any media type.</span></span>                                                                                                                                    |
| <span data-ttu-id="da2a9-115">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="da2a9-115">Input pin interfaces</span></span>                     | <span data-ttu-id="da2a9-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="da2a9-116">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="da2a9-117">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="da2a9-117">Output pin media types</span></span>                   | <span data-ttu-id="da2a9-118">Tout type de média.</span><span class="sxs-lookup"><span data-stu-id="da2a9-118">Any media type.</span></span> <span data-ttu-id="da2a9-119">Correspond au type de média d’entrée.</span><span class="sxs-lookup"><span data-stu-id="da2a9-119">Matches input media type.</span></span>                                                                                                          |
| <span data-ttu-id="da2a9-120">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="da2a9-120">Output pin interfaces</span></span>                    | <span data-ttu-id="da2a9-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="da2a9-121">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="da2a9-122">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="da2a9-122">Filter CLSID</span></span>                             | <span data-ttu-id="da2a9-123">CLSID \_ SampleGrabber</span><span class="sxs-lookup"><span data-stu-id="da2a9-123">CLSID\_SampleGrabber</span></span>                                                                                                                               |
| <span data-ttu-id="da2a9-124">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="da2a9-124">Property Page CLSID</span></span>                      | <span data-ttu-id="da2a9-125">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="da2a9-125">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="da2a9-126">Exécutable</span><span class="sxs-lookup"><span data-stu-id="da2a9-126">Executable</span></span>                               | <span data-ttu-id="da2a9-127">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="da2a9-127">Qedit.dll</span></span>                                                                                                                                          |
| [<span data-ttu-id="da2a9-128">Mérite</span><span class="sxs-lookup"><span data-stu-id="da2a9-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="da2a9-129">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="da2a9-129">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="da2a9-130">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="da2a9-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="da2a9-131">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="da2a9-131">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="da2a9-132">Notes</span><span class="sxs-lookup"><span data-stu-id="da2a9-132">Remarks</span></span>

<span data-ttu-id="da2a9-133">Pour utiliser ce filtre, ajoutez-le au graphique de filtre et appelez [**ISampleGrabber :: SetMediaType**](isamplegrabber-setmediatype.md) avec le type de média souhaité.</span><span class="sxs-lookup"><span data-stu-id="da2a9-133">To use this filter, add it to the filter graph and call [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) with the desired media type.</span></span> <span data-ttu-id="da2a9-134">Cette méthode spécifie le type de média pour les connexions de broche d’entrée et de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="da2a9-134">This method specifies the media type for the filter's input and output pin connections.</span></span> <span data-ttu-id="da2a9-135">Connectez ensuite le filtre à d’autres filtres dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="da2a9-135">Then connect the filter to other filters in the graph.</span></span>

<span data-ttu-id="da2a9-136">Si vous appelez [**ISampleGrabber :: SetBufferSamples**](isamplegrabber-setbuffersamples.md) avec la valeur **true**, le filtre met en mémoire tampon chaque échantillon qu’il reçoit avant de le passer en aval.</span><span class="sxs-lookup"><span data-stu-id="da2a9-136">If you call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with the value **TRUE**, the filter buffers each sample that it receives before passing it downstream.</span></span> <span data-ttu-id="da2a9-137">Appelez la méthode [**ISampleGrabber :: GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) pour récupérer le contenu actuel de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="da2a9-137">Call the [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method to retrieve the current contents of the buffer.</span></span> <span data-ttu-id="da2a9-138">Vous pouvez également appeler [**ISampleGrabber :: SetCallback**](isamplegrabber-setcallback.md) pour que le filtre appelle une fonction de rappel chaque fois qu’il reçoit un exemple.</span><span class="sxs-lookup"><span data-stu-id="da2a9-138">Alternatively, you can call [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) to have the filter invoke a callback function whenever it receives a sample.</span></span>

<span data-ttu-id="da2a9-139">Le filtre présente les limitations suivantes pour les formats vidéo :</span><span class="sxs-lookup"><span data-stu-id="da2a9-139">The filter has the following limitations for video formats:</span></span>

-   <span data-ttu-id="da2a9-140">Il ne prend pas en charge les types vidéo avec une orientation verticale ( **bihauteur** négative).</span><span class="sxs-lookup"><span data-stu-id="da2a9-140">It does not support video types with top-down orientation (negative **biHeight**).</span></span>
-   <span data-ttu-id="da2a9-141">Elle ne prend pas en charge la structure de format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (type de format égal au **format \_ VideoInfo2**).</span><span class="sxs-lookup"><span data-stu-id="da2a9-141">It does not support the [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format structure (format type equal to **FORMAT\_VideoInfo2**).</span></span>
-   <span data-ttu-id="da2a9-142">Elle rejette tout type de vidéo dans lequel le Stride de la surface ne correspond pas à la largeur de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="da2a9-142">It rejects any video type where the surface stride does not match the video width.</span></span>

<span data-ttu-id="da2a9-143">Par conséquent, la accroche d’échantillon ne se connecte pas au convertisseur de mixage vidéo (VMR) pour certains types de vidéo.</span><span class="sxs-lookup"><span data-stu-id="da2a9-143">As a result, the Sample Grabber will not connect to the Video Mixing Renderer (VMR) for some video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="da2a9-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da2a9-144">Requirements</span></span>



| <span data-ttu-id="da2a9-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da2a9-145">Requirement</span></span> | <span data-ttu-id="da2a9-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="da2a9-146">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="da2a9-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="da2a9-147">Header</span></span><br/> | <dl> <span data-ttu-id="da2a9-148"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2a9-148"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da2a9-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da2a9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2a9-150">Objets des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="da2a9-150">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> <dt>

[<span data-ttu-id="da2a9-151">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="da2a9-151">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 




