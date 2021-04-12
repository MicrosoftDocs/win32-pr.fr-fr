---
description: Filtre Tuner TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtre Tuner TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320398"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="a9a51-103">Filtre Tuner TV</span><span class="sxs-lookup"><span data-stu-id="a9a51-103">TV Tuner Filter</span></span>

<span data-ttu-id="a9a51-104">Le filtre Tuner TV sélectionne une diffusion analogique ou un canal câblé à afficher.</span><span class="sxs-lookup"><span data-stu-id="a9a51-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="a9a51-105">Le flux de sortie unique est un chemin d’accès matériel pour la vidéo de bande de streaming analogique.</span><span class="sxs-lookup"><span data-stu-id="a9a51-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="a9a51-106">Cette sortie doit se connecter au filtre de la vidéo analogique.</span><span class="sxs-lookup"><span data-stu-id="a9a51-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="a9a51-107">Les broches d’entrée incluent une entrée pour Cable et une entrée d’antenne.</span><span class="sxs-lookup"><span data-stu-id="a9a51-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9a51-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="a9a51-108">Filter Interfaces</span></span>                        | <span data-ttu-id="a9a51-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="a9a51-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="a9a51-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="a9a51-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a9a51-111">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a9a51-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a9a51-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="a9a51-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a9a51-113">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a9a51-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a9a51-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a9a51-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a9a51-115">Vidéo : MEDIATYPE \_ AnalogVideo, \_ sous-type KSDATAFORMAT \_ Aucun audio : MediaType \_ AnalogAudio, MEDIASUBTYPE \_ null</span><span class="sxs-lookup"><span data-stu-id="a9a51-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="a9a51-116">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a9a51-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="a9a51-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="a9a51-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="a9a51-118">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="a9a51-118">Filter CLSID</span></span>                             | <span data-ttu-id="a9a51-119">CLSID \_ TVTunerFilter</span><span class="sxs-lookup"><span data-stu-id="a9a51-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="a9a51-120">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="a9a51-120">Property Page CLSID</span></span>                      | <span data-ttu-id="a9a51-121">CLSID \_ TVTunerFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="a9a51-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="a9a51-122">Exécutable</span><span class="sxs-lookup"><span data-stu-id="a9a51-122">Executable</span></span>                               | <span data-ttu-id="a9a51-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="a9a51-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="a9a51-124">Mérite</span><span class="sxs-lookup"><span data-stu-id="a9a51-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="a9a51-125">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="a9a51-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="a9a51-126">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="a9a51-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a9a51-127">AM \_ KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="a9a51-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="a9a51-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a9a51-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9a51-129">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="a9a51-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



