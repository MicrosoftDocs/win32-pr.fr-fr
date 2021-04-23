---
description: Le filtre de convertisseur null est un convertisseur qui ignore chaque échantillon qu’il reçoit, sans afficher ou restituer les exemples de données.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: Filtre de convertisseur null (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908807"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="c1f12-103">Filtre de convertisseur null</span><span class="sxs-lookup"><span data-stu-id="c1f12-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="c1f12-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="c1f12-104">\[Deprecated.</span></span> <span data-ttu-id="c1f12-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c1f12-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1f12-106">Le filtre de convertisseur null est un convertisseur qui ignore chaque échantillon qu’il reçoit, sans afficher ou restituer les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="c1f12-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



| <span data-ttu-id="c1f12-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="c1f12-107">Label</span></span> | <span data-ttu-id="c1f12-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1f12-108">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f12-109">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="c1f12-109">Filter interfaces</span></span>                        | <span data-ttu-id="c1f12-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="c1f12-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="c1f12-111">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="c1f12-111">Input pin media types</span></span>                    | <span data-ttu-id="c1f12-112">Tout type de média</span><span class="sxs-lookup"><span data-stu-id="c1f12-112">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="c1f12-113">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="c1f12-113">Input pin interfaces</span></span>                     | <span data-ttu-id="c1f12-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="c1f12-114">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="c1f12-115">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="c1f12-115">Output pin media types</span></span>                   | <span data-ttu-id="c1f12-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="c1f12-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="c1f12-117">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="c1f12-117">Output pin interfaces</span></span>                    | <span data-ttu-id="c1f12-118">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="c1f12-118">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="c1f12-119">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="c1f12-119">Filter CLSID</span></span>                             | <span data-ttu-id="c1f12-120">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="c1f12-120">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="c1f12-121">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="c1f12-121">Property Page CLSID</span></span>                      | <span data-ttu-id="c1f12-122">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c1f12-122">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="c1f12-123">Exécutable</span><span class="sxs-lookup"><span data-stu-id="c1f12-123">Executable</span></span>                               | <span data-ttu-id="c1f12-124">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="c1f12-124">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="c1f12-125">Mérite</span><span class="sxs-lookup"><span data-stu-id="c1f12-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="c1f12-126">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="c1f12-126">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="c1f12-127">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="c1f12-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c1f12-128">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="c1f12-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="c1f12-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1f12-129">Remarks</span></span>

<span data-ttu-id="c1f12-130">Utilisez ce filtre quand une broche de sortie dans le graphique nécessite une connexion en aval, mais que vous ne souhaitez pas afficher les données à partir de ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="c1f12-130">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="c1f12-131">En connectant la broche de sortie au convertisseur null, vous terminez la connexion sans restituer les données.</span><span class="sxs-lookup"><span data-stu-id="c1f12-131">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="c1f12-132">Même si ce filtre n’affiche aucun échantillon, il attend la durée de présentation de chaque exemple avant d’ignorer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="c1f12-132">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="c1f12-133">Par conséquent, le graphique s’exécutera au taux normal.</span><span class="sxs-lookup"><span data-stu-id="c1f12-133">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="c1f12-134">Si vous souhaitez que le graphique s’exécute aussi rapidement que possible, affectez la **valeur null** à l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="c1f12-134">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="c1f12-135">Pour plus d’informations, consultez [définition de l’horloge du graphique](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="c1f12-135">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1f12-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1f12-136">Requirements</span></span>



| <span data-ttu-id="c1f12-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1f12-137">Requirement</span></span> | <span data-ttu-id="c1f12-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1f12-138">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f12-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1f12-139">Header</span></span><br/> | <dl> <span data-ttu-id="c1f12-140"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1f12-140"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1f12-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1f12-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1f12-142">Objets des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="c1f12-142">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




