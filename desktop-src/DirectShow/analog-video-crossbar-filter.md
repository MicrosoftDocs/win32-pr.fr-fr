---
description: Filtre de distributeur vidéo analogique
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtre de distributeur vidéo analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17d8700131dbc658a5233d56f339c39eac7a3a0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909597"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="fc6c0-103">Filtre de distributeur vidéo analogique</span><span class="sxs-lookup"><span data-stu-id="fc6c0-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="fc6c0-104">Le filtre de distributeur vidéo analogique représente un distributeur vidéo sur un appareil de capture vidéo qui prend en charge le Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="fc6c0-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="fc6c0-105">Ce filtre est un filtre de wrapper pour les filtres sur les périphériques de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="fc6c0-106">Le nom convivial du filtre provient de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="fc6c0-107">Chaque broche de sortie représente un chemin d’accès matériel pour une vidéo de bande de bande analogique.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="fc6c0-108">L’une des broches d’entrée provient d’un tuner TV (le [filtre Tuner TV](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="fc6c0-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="fc6c0-109">D’autres broches d’entrée prennent en charge les flux vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="fc6c0-110">Le filtre prend en charge tous les formats et sous-types de médias pris en charge sur les connexions en aval.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="fc6c0-111">Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="fc6c0-112">L’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) ajoute automatiquement ce filtre au graphique en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="fc6c0-113">Pour plus d’informations sur les filtres de wrapper et les périphériques de streaming WDM, voir [Comment les périphériques matériels participent au graphique de filtre](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="fc6c0-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



| <span data-ttu-id="fc6c0-114">Étiquette</span><span class="sxs-lookup"><span data-stu-id="fc6c0-114">Label</span></span> | <span data-ttu-id="fc6c0-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc6c0-115">Value</span></span> |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6c0-116">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="fc6c0-116">Filter Interfaces</span></span>                        | <span data-ttu-id="fc6c0-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="fc6c0-117">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="fc6c0-118">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="fc6c0-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="fc6c0-119">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="fc6c0-119">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="fc6c0-120">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="fc6c0-120">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="fc6c0-121">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="fc6c0-121">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="fc6c0-122">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="fc6c0-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="fc6c0-123">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="fc6c0-123">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="fc6c0-124">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="fc6c0-124">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="fc6c0-125">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="fc6c0-125">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="fc6c0-126">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="fc6c0-126">Filter CLSID</span></span>                             | <span data-ttu-id="fc6c0-127">Non applicable</span><span class="sxs-lookup"><span data-stu-id="fc6c0-127">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="fc6c0-128">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="fc6c0-128">Property Page CLSID</span></span>                      | <span data-ttu-id="fc6c0-129">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="fc6c0-129">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="fc6c0-130">Exécutable</span><span class="sxs-lookup"><span data-stu-id="fc6c0-130">Executable</span></span>                               | <span data-ttu-id="fc6c0-131">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="fc6c0-131">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="fc6c0-132">Mérite</span><span class="sxs-lookup"><span data-stu-id="fc6c0-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="fc6c0-133">Dépendant du pilote.</span><span class="sxs-lookup"><span data-stu-id="fc6c0-133">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="fc6c0-134">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="fc6c0-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="fc6c0-135">\_KSCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="fc6c0-135">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="fc6c0-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc6c0-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc6c0-137">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="fc6c0-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="fc6c0-138">Utilisation des conversions</span><span class="sxs-lookup"><span data-stu-id="fc6c0-138">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



