---
description: Filtre Tuner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtre Tuner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909027"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="a1ad5-103">Filtre Tuner TV</span><span class="sxs-lookup"><span data-stu-id="a1ad5-103">TV Tuner Filter</span></span>

<span data-ttu-id="a1ad5-104">Le filtre Tuner TV sélectionne une diffusion analogique ou un canal câblé à afficher.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="a1ad5-105">Le flux de sortie unique est un chemin d’accès matériel pour la vidéo de bande de streaming analogique.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="a1ad5-106">Cette sortie doit se connecter au filtre de la vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="a1ad5-107">Les broches d’entrée incluent une entrée pour Cable et une entrée d’antenne.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="a1ad5-108">Étiquette</span><span class="sxs-lookup"><span data-stu-id="a1ad5-108">Label</span></span> | <span data-ttu-id="a1ad5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1ad5-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1ad5-110">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="a1ad5-110">Filter Interfaces</span></span>                        | <span data-ttu-id="a1ad5-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="a1ad5-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="a1ad5-112">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="a1ad5-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="a1ad5-113">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a1ad5-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="a1ad5-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a1ad5-115">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a1ad5-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a1ad5-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a1ad5-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="a1ad5-117">Vidéo : MEDIATYPE \_ AnalogVideo, \_ sous-type KSDATAFORMAT \_ Aucun audio : MediaType \_ AnalogAudio, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="a1ad5-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="a1ad5-118">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a1ad5-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="a1ad5-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="a1ad5-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="a1ad5-120">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="a1ad5-120">Filter CLSID</span></span>                             | <span data-ttu-id="a1ad5-121">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="a1ad5-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="a1ad5-122">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="a1ad5-122">Property Page CLSID</span></span>                      | <span data-ttu-id="a1ad5-123">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="a1ad5-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="a1ad5-124">Exécutable</span><span class="sxs-lookup"><span data-stu-id="a1ad5-124">Executable</span></span>                               | <span data-ttu-id="a1ad5-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="a1ad5-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="a1ad5-126">Mérite</span><span class="sxs-lookup"><span data-stu-id="a1ad5-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="a1ad5-127">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="a1ad5-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="a1ad5-128">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="a1ad5-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a1ad5-129">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="a1ad5-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="a1ad5-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1ad5-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1ad5-131">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1ad5-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



