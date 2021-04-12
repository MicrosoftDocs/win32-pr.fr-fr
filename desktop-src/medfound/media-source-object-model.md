---
description: Modèle d’objet de source multimédia
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modèle d’objet de source multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321589"
---
# <a name="media-source-object-model"></a><span data-ttu-id="716bc-103">Modèle d’objet de source multimédia</span><span class="sxs-lookup"><span data-stu-id="716bc-103">Media Source Object Model</span></span>

<span data-ttu-id="716bc-104">Cette rubrique décrit le modèle d’objet pour les sources multimédias dans Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="716bc-104">This topic describes the object model for media sources in Microsoft Media Foundation.</span></span> <span data-ttu-id="716bc-105">Une source multimédia doit implémenter deux objets :</span><span class="sxs-lookup"><span data-stu-id="716bc-105">A media source must implement two objects:</span></span>

-   <span data-ttu-id="716bc-106">Un descripteur de présentation, qui décrit le contenu de la source, y compris le nombre de flux et le format de chaque flux.</span><span class="sxs-lookup"><span data-stu-id="716bc-106">A presentation descriptor, which describes the contents of the source, including the number of streams and the format of each stream.</span></span> <span data-ttu-id="716bc-107">Pour plus d’informations sur les descripteurs de présentation, consultez [descripteurs de présentation](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="716bc-107">For more information about presentation descriptors, see [Presentation Descriptors](presentation-descriptors.md).</span></span>
-   <span data-ttu-id="716bc-108">Un ou plusieurs flux de données multimédias, qui génèrent les données sources.</span><span class="sxs-lookup"><span data-stu-id="716bc-108">One or more media streams, which generate the source data.</span></span>

<span data-ttu-id="716bc-109">La source ne crée pas les flux avant le démarrage de la lecture.</span><span class="sxs-lookup"><span data-stu-id="716bc-109">The source does not create the streams until playback starts.</span></span>

## <a name="media-source-interfaces"></a><span data-ttu-id="716bc-110">Interfaces sources de média</span><span class="sxs-lookup"><span data-stu-id="716bc-110">Media Source Interfaces</span></span>

<span data-ttu-id="716bc-111">Une source multimédia doit exposer les interfaces suivantes via **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="716bc-111">A media source must expose the following interfaces through **QueryInterface**.</span></span>



| <span data-ttu-id="716bc-112">Interface</span><span class="sxs-lookup"><span data-stu-id="716bc-112">Interface</span></span>                                                | <span data-ttu-id="716bc-113">Description</span><span class="sxs-lookup"><span data-stu-id="716bc-113">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="716bc-114">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="716bc-114">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | <span data-ttu-id="716bc-115">Obligatoire pour toutes les sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="716bc-115">Required for all media sources.</span></span>                                                                                 |
| [<span data-ttu-id="716bc-116">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="716bc-116">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="716bc-117">Obligatoire pour toutes les sources multimédias.</span><span class="sxs-lookup"><span data-stu-id="716bc-117">Required for all media sources.</span></span> <span data-ttu-id="716bc-118">L’interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) hérite de cette interface.</span><span class="sxs-lookup"><span data-stu-id="716bc-118">The [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface inherits this interface.</span></span> |



 

<span data-ttu-id="716bc-119">Si vous le souhaitez, une source de média peut implémenter l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) et implémenter l’une des interfaces suivantes en tant que services :</span><span class="sxs-lookup"><span data-stu-id="716bc-119">Optionally, a media source can implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface and implement any of the following interfaces as services:</span></span>



| <span data-ttu-id="716bc-120">Interface de service</span><span class="sxs-lookup"><span data-stu-id="716bc-120">Service interface</span></span>                                  | <span data-ttu-id="716bc-121">Description</span><span class="sxs-lookup"><span data-stu-id="716bc-121">Description</span></span>                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="716bc-122">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="716bc-122">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | <span data-ttu-id="716bc-123">Contrôle la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="716bc-123">Controls the playback rate.</span></span>                                       |
| [<span data-ttu-id="716bc-124">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="716bc-124">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | <span data-ttu-id="716bc-125">Indique la plage des taux de lecture pris en charge.</span><span class="sxs-lookup"><span data-stu-id="716bc-125">Reports the range of playback rates that are supported.</span></span>           |
| [<span data-ttu-id="716bc-126">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="716bc-126">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | <span data-ttu-id="716bc-127">Permet au gestionnaire de qualité d’ajuster la qualité audio ou vidéo.</span><span class="sxs-lookup"><span data-stu-id="716bc-127">Enables the quality manager to adjust the audio or video quality.</span></span> |
| [<span data-ttu-id="716bc-128">**IMFMetadataProvider**</span><span class="sxs-lookup"><span data-stu-id="716bc-128">**IMFMetadataProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | <span data-ttu-id="716bc-129">Fournit des métadonnées.</span><span class="sxs-lookup"><span data-stu-id="716bc-129">Provides metadata.</span></span>                                                |



 

<span data-ttu-id="716bc-130">Si la source du média peut fonctionner à des vitesses autres que la vitesse normale (1,0), elle doit exposer le service de contrôle de la fréquence ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) et [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span><span class="sxs-lookup"><span data-stu-id="716bc-130">If the media source can play at rates other than normal speed (1.0), it should expose the rate control service ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) and [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)).</span></span> <span data-ttu-id="716bc-131">Dans le cas contraire, il est supposé que la source prend uniquement en charge la lecture à la vitesse normale.</span><span class="sxs-lookup"><span data-stu-id="716bc-131">Otherwise, it is assumed that the source only supports playback at normal speed.</span></span> <span data-ttu-id="716bc-132">Pour plus d’informations, consultez [Implementing Rate Control](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="716bc-132">For more information, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="716bc-133">Pour plus d’informations sur les interfaces de service et les [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consultez [interfaces de service](service-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="716bc-133">For more information about service interfaces and [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), see [Service Interfaces](service-interfaces.md).</span></span>

## <a name="media-stream-interfaces"></a><span data-ttu-id="716bc-134">Interfaces de flux de média</span><span class="sxs-lookup"><span data-stu-id="716bc-134">Media Stream Interfaces</span></span>

<span data-ttu-id="716bc-135">Les flux multimédias doivent implémenter les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="716bc-135">Media streams must implement the following interfaces.</span></span>



| <span data-ttu-id="716bc-136">Interface</span><span class="sxs-lookup"><span data-stu-id="716bc-136">Interface</span></span>                                                | <span data-ttu-id="716bc-137">Description</span><span class="sxs-lookup"><span data-stu-id="716bc-137">Description</span></span>                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="716bc-138">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="716bc-138">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | <span data-ttu-id="716bc-139">Requis pour tous les flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="716bc-139">Required for all media streams.</span></span>                                                                                 |
| [<span data-ttu-id="716bc-140">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="716bc-140">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | <span data-ttu-id="716bc-141">Requis pour tous les flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="716bc-141">Required for all media streams.</span></span> <span data-ttu-id="716bc-142">L’interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) hérite de cette interface.</span><span class="sxs-lookup"><span data-stu-id="716bc-142">The [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface inherits this interface.</span></span> |



 

<span data-ttu-id="716bc-143">Aucune interface de service n’est actuellement définie pour les flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="716bc-143">Currently no service interfaces are defined for media streams.</span></span>

## <a name="related-topics"></a><span data-ttu-id="716bc-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="716bc-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="716bc-145">Sources multimédias</span><span class="sxs-lookup"><span data-stu-id="716bc-145">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



