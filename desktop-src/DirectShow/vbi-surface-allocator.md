---
description: Allocateur de surface VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Allocateur de surface VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757677"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="4650a-103">Allocateur de surface VBI</span><span class="sxs-lookup"><span data-stu-id="4650a-103">VBI Surface Allocator</span></span>

<span data-ttu-id="4650a-104">L’allocateur de surface VBI contrôle l’allocation de mémoires tampons VBI dans des graphiques de télévision analogiques avec des scénarios de capture de port vidéo matériel.</span><span class="sxs-lookup"><span data-stu-id="4650a-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="4650a-105">Avec les appareils tels que le décodeur Bt829, la mémoire tampon de trame peut contenir plusieurs mémoires tampons de capture VBI accessibles via un mécanisme matériel propriétaire connu de manière générique comme un port vidéo.</span><span class="sxs-lookup"><span data-stu-id="4650a-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="4650a-106">Le filtre allocateur de surface VBI se connecte en aval du filtre de capture et n’a aucune broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="4650a-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="4650a-107">Le filtre fonctionne en étroite collaboration avec le [mélangeur de superposition](overlay-mixer-filter.md) (par le biais de DirectDraw) pour effectuer des opérations coordonnées sur le port vidéo matériel, en utilisant la même mémoire tampon de trame SVGA limitée.</span><span class="sxs-lookup"><span data-stu-id="4650a-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4650a-108">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="4650a-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="4650a-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="4650a-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="4650a-110">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="4650a-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="4650a-111">\_Vidéo MediaType, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="4650a-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="4650a-112">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="4650a-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="4650a-113">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="4650a-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="4650a-114">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="4650a-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="4650a-115">MEDIATYPE \_ null, MEDIASUBTYPE \_ null.</span><span class="sxs-lookup"><span data-stu-id="4650a-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="4650a-116">(Rien n’est jamais connecté à la broche de sortie.)</span><span class="sxs-lookup"><span data-stu-id="4650a-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="4650a-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="4650a-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="4650a-118">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="4650a-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="4650a-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="4650a-119">Filter CLSID</span></span>                             | <span data-ttu-id="4650a-120">CLSID \_ VBISurfaces</span><span class="sxs-lookup"><span data-stu-id="4650a-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="4650a-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="4650a-121">Property Page CLSID</span></span>                      | <span data-ttu-id="4650a-122">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="4650a-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="4650a-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="4650a-123">Executable</span></span>                               | <span data-ttu-id="4650a-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="4650a-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="4650a-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="4650a-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="4650a-126">MÉRITE \_ normal</span><span class="sxs-lookup"><span data-stu-id="4650a-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="4650a-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="4650a-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4650a-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="4650a-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="4650a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4650a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4650a-130">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="4650a-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



