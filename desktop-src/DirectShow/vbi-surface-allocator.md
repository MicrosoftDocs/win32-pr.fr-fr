---
description: Allocateur de surface VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocateur de surface VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909007"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="a0be5-103">Allocateur de surface VBI</span><span class="sxs-lookup"><span data-stu-id="a0be5-103">VBI Surface Allocator</span></span>

<span data-ttu-id="a0be5-104">L’allocateur de surface VBI contrôle l’allocation de mémoires tampons VBI dans des graphiques de télévision analogiques avec des scénarios de capture de port vidéo matériel.</span><span class="sxs-lookup"><span data-stu-id="a0be5-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="a0be5-105">Avec les appareils tels que le décodeur Bt829, la mémoire tampon de trame peut contenir plusieurs mémoires tampons de capture VBI accessibles via un mécanisme matériel propriétaire connu de manière générique comme un port vidéo.</span><span class="sxs-lookup"><span data-stu-id="a0be5-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="a0be5-106">Le filtre allocateur de surface VBI se connecte en aval du filtre de capture et n’a aucune broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="a0be5-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="a0be5-107">Le filtre fonctionne en étroite collaboration avec le [mélangeur de superposition](overlay-mixer-filter.md) (par le biais de DirectDraw) pour effectuer des opérations coordonnées sur le port vidéo matériel, en utilisant la même mémoire tampon de trame SVGA limitée.</span><span class="sxs-lookup"><span data-stu-id="a0be5-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="a0be5-108">Étiquette</span><span class="sxs-lookup"><span data-stu-id="a0be5-108">Label</span></span> | <span data-ttu-id="a0be5-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0be5-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a0be5-110">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="a0be5-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="a0be5-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a0be5-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="a0be5-112">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="a0be5-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="a0be5-113">\_Vidéo MediaType, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="a0be5-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="a0be5-114">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="a0be5-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="a0be5-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="a0be5-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="a0be5-116">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a0be5-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="a0be5-117">MEDIATYPE \_ null, MEDIASUBTYPE \_ null.</span><span class="sxs-lookup"><span data-stu-id="a0be5-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="a0be5-118">(Rien n’est jamais connecté à la broche de sortie.)</span><span class="sxs-lookup"><span data-stu-id="a0be5-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="a0be5-119">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="a0be5-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a0be5-120">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="a0be5-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="a0be5-121">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="a0be5-121">Filter CLSID</span></span>                             | <span data-ttu-id="a0be5-122">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="a0be5-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="a0be5-123">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="a0be5-123">Property Page CLSID</span></span>                      | <span data-ttu-id="a0be5-124">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="a0be5-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="a0be5-125">Exécutable</span><span class="sxs-lookup"><span data-stu-id="a0be5-125">Executable</span></span>                               | <span data-ttu-id="a0be5-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="a0be5-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="a0be5-127">Mérite</span><span class="sxs-lookup"><span data-stu-id="a0be5-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="a0be5-128">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="a0be5-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="a0be5-129">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="a0be5-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a0be5-130">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a0be5-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a0be5-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a0be5-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0be5-132">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0be5-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



