---
description: Choix du convertisseur vidéo approprié
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Choix du convertisseur vidéo approprié
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513113"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="6b171-103">Choix du convertisseur vidéo approprié</span><span class="sxs-lookup"><span data-stu-id="6b171-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="6b171-104">DirectShow fournit plusieurs filtres de convertisseur vidéo, résumés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6b171-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="6b171-105">Filtrer</span><span class="sxs-lookup"><span data-stu-id="6b171-105">Filter</span></span>                                                                  | <span data-ttu-id="6b171-106">Notes</span><span class="sxs-lookup"><span data-stu-id="6b171-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="6b171-107">[**Rendu vidéo amélioré**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="6b171-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="6b171-108">Utilise Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b171-108">Uses Direct3D 9.</span></span> <span data-ttu-id="6b171-109">Nécessite Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6b171-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="6b171-110">[Convertisseur de mixage vidéo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="6b171-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="6b171-111">Utilise Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="6b171-111">Uses Direct3D 9.</span></span> <span data-ttu-id="6b171-112">Nécessite Windows XP ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6b171-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="6b171-113">[Filtre de mixage vidéo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="6b171-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="6b171-114">Utilise DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="6b171-114">Uses DirectDraw.</span></span> <span data-ttu-id="6b171-115">Nécessite Windows XP ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6b171-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="6b171-116">Mixage de superposition</span><span class="sxs-lookup"><span data-stu-id="6b171-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="6b171-117">Prend en charge les superpositions matérielles via DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="6b171-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="6b171-118">Filtre de [convertisseur vidéo](video-renderer-filter.md) hérité.</span><span class="sxs-lookup"><span data-stu-id="6b171-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="6b171-119">Utilise DirectDraw ou (rarement) GDI</span><span class="sxs-lookup"><span data-stu-id="6b171-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="6b171-120">Le convertisseur à utiliser dépend en grande partie des versions de Windows que vous devez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="6b171-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="6b171-121">Dans Windows Vista et versions ultérieures, les applications doivent utiliser le EVR si le matériel le prend en charge.</span><span class="sxs-lookup"><span data-stu-id="6b171-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="6b171-122">Sinon, revenez à VMR-9 ou VMR-7.</span><span class="sxs-lookup"><span data-stu-id="6b171-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="6b171-123">Le EVR offre de meilleures performances et une meilleure qualité vidéo que les convertisseurs précédents.</span><span class="sxs-lookup"><span data-stu-id="6b171-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="6b171-124">En outre, il est conçu pour fonctionner avec le Gestionnaire de fenêtrage (DWM).</span><span class="sxs-lookup"><span data-stu-id="6b171-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="6b171-125">Avant Windows Vista, utilisez VMR-9 si le matériel prend en charge les fonctionnalités du port informatique et de la vidéo n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6b171-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="6b171-126">Dans le cas contraire, utilisez VMR-7.</span><span class="sxs-lookup"><span data-stu-id="6b171-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="6b171-127">Sur les systèmes plus anciens, vous devrez peut-être utiliser le mélangeur de superposition (pour le port vidéo ou la prise en charge de la superposition matérielle) ou le filtre de convertisseur vidéo hérité.</span><span class="sxs-lookup"><span data-stu-id="6b171-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="6b171-128">Les méthodes [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) et [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) utilisent VMR-7 par défaut.</span><span class="sxs-lookup"><span data-stu-id="6b171-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="6b171-129">Si le matériel ne prend pas en charge VMR-7, ces méthodes reviennent au filtre de convertisseur vidéo hérité.</span><span class="sxs-lookup"><span data-stu-id="6b171-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="6b171-130">EVR et VMR-9 ne sont jamais les convertisseurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="6b171-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b171-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b171-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b171-132">Rendu vidéo</span><span class="sxs-lookup"><span data-stu-id="6b171-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



