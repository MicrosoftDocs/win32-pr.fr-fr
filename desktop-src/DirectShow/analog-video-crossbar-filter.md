---
description: Filtre de distributeur vidéo analogique
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtre de distributeur vidéo analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950137"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="a01e1-103">Filtre de distributeur vidéo analogique</span><span class="sxs-lookup"><span data-stu-id="a01e1-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="a01e1-104">Le filtre de distributeur vidéo analogique représente un distributeur vidéo sur un appareil de capture vidéo qui prend en charge le Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="a01e1-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="a01e1-105">Ce filtre est un filtre de wrapper pour les filtres sur les périphériques de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="a01e1-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="a01e1-106">Le nom convivial du filtre provient de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a01e1-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="a01e1-107">Chaque broche de sortie représente un chemin d’accès matériel pour une vidéo de bande de bande analogique.</span><span class="sxs-lookup"><span data-stu-id="a01e1-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="a01e1-108">L’une des broches d’entrée provient d’un tuner TV (le [filtre Tuner TV](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="a01e1-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="a01e1-109">D’autres broches d’entrée prennent en charge les flux vidéo ou audio.</span><span class="sxs-lookup"><span data-stu-id="a01e1-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="a01e1-110">Le filtre prend en charge tous les formats et sous-types de médias pris en charge sur les connexions en aval.</span><span class="sxs-lookup"><span data-stu-id="a01e1-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="a01e1-111">Vous ne pouvez pas créer directement ce filtre avec CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="a01e1-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="a01e1-112">L’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) ajoute automatiquement ce filtre au graphique en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="a01e1-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="a01e1-113">Pour plus d’informations sur les filtres de wrapper et les périphériques de streaming WDM, voir [Comment les périphériques matériels participent au graphique de filtre](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="a01e1-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01e1-114">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="a01e1-114">Filter Interfaces</span></span>                        | <span data-ttu-id="a01e1-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="a01e1-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="a01e1-116">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="a01e1-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="a01e1-117">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="a01e1-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="a01e1-118">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="a01e1-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="a01e1-119">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a01e1-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="a01e1-120">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a01e1-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="a01e1-121">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="a01e1-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="a01e1-122">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a01e1-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="a01e1-123">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a01e1-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="a01e1-124">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="a01e1-124">Filter CLSID</span></span>                             | <span data-ttu-id="a01e1-125">Non applicable</span><span class="sxs-lookup"><span data-stu-id="a01e1-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="a01e1-126">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="a01e1-126">Property Page CLSID</span></span>                      | <span data-ttu-id="a01e1-127">CLSID \_ CrossbarFilterPropertyPage</span><span class="sxs-lookup"><span data-stu-id="a01e1-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="a01e1-128">Exécutable</span><span class="sxs-lookup"><span data-stu-id="a01e1-128">Executable</span></span>                               | <span data-ttu-id="a01e1-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="a01e1-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="a01e1-130">Mérite</span><span class="sxs-lookup"><span data-stu-id="a01e1-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="a01e1-131">Dépendant du pilote.</span><span class="sxs-lookup"><span data-stu-id="a01e1-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="a01e1-132">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="a01e1-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a01e1-133">\_KSCATEGORY \_</span><span class="sxs-lookup"><span data-stu-id="a01e1-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a01e1-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a01e1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a01e1-135">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="a01e1-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a01e1-136">Utilisation des conversions</span><span class="sxs-lookup"><span data-stu-id="a01e1-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



