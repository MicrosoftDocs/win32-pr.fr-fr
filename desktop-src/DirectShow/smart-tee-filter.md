---
description: Filtre tee intelligent
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtre tee intelligent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482297"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="643a5-103">Filtre tee intelligent</span><span class="sxs-lookup"><span data-stu-id="643a5-103">Smart Tee Filter</span></span>

<span data-ttu-id="643a5-104">Le filtre tee intelligent est utilisé dans les graphiques de capture vidéo pour fractionner le flux vidéo en un flux d’aperçu et un flux de capture.</span><span class="sxs-lookup"><span data-stu-id="643a5-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="643a5-105">Cette opération est effectuée sans copie de données supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="643a5-105">This is done without any additional data copying.</span></span> <span data-ttu-id="643a5-106">Les broches de sortie prennent en charge tous les types de supports pris en charge sur la connexion en aval.</span><span class="sxs-lookup"><span data-stu-id="643a5-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="643a5-107">Le filtre des tees intelligents est utile lorsqu’un filtre de capture vidéo ne fournit pas de codes confidentiels distincts pour la capture et l’aperçu.</span><span class="sxs-lookup"><span data-stu-id="643a5-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="643a5-108">Le filtre tee intelligent ne fournit des données en préversion que si cela n’a pas d’impact sur les performances de capture.</span><span class="sxs-lookup"><span data-stu-id="643a5-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="643a5-109">Elle supprime également les horodatages du flux d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="643a5-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="643a5-110">Le générateur de graphiques de capture insère automatiquement le filtre tee intelligent si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="643a5-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="643a5-111">Pour plus d’informations, consultez combinaison de la [capture vidéo et de l’aperçu](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="643a5-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="643a5-112">L’illustration suivante montre un graphique de capture classique qui utilise le filtre tee intelligent.</span><span class="sxs-lookup"><span data-stu-id="643a5-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![utilisation du filtre tee Smart](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="643a5-114">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="643a5-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="643a5-115">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="643a5-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="643a5-116">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="643a5-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="643a5-117">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="643a5-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="643a5-118">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="643a5-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="643a5-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="643a5-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="643a5-120">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="643a5-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="643a5-121">\_Vidéo MediaType, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="643a5-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="643a5-122">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="643a5-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="643a5-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="643a5-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="643a5-124">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="643a5-124">Filter CLSID</span></span>                             | <span data-ttu-id="643a5-125">CLSID \_ SmartTee</span><span class="sxs-lookup"><span data-stu-id="643a5-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="643a5-126">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="643a5-126">Property Page CLSID</span></span>                      | <span data-ttu-id="643a5-127">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="643a5-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="643a5-128">Exécutable</span><span class="sxs-lookup"><span data-stu-id="643a5-128">Executable</span></span>                               | <span data-ttu-id="643a5-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="643a5-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="643a5-130">Mérite</span><span class="sxs-lookup"><span data-stu-id="643a5-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="643a5-131">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="643a5-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="643a5-132">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="643a5-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="643a5-133">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="643a5-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="643a5-134">Notes</span><span class="sxs-lookup"><span data-stu-id="643a5-134">Remarks</span></span>

<span data-ttu-id="643a5-135">Le code PIN de capture est la broche de sortie 0 et le code PIN de sortie est la broche 1.</span><span class="sxs-lookup"><span data-stu-id="643a5-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="643a5-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="643a5-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="643a5-137">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="643a5-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



