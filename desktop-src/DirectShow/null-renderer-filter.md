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
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528893"
---
# <a name="null-renderer-filter"></a><span data-ttu-id="98ede-103">Filtre de convertisseur null</span><span class="sxs-lookup"><span data-stu-id="98ede-103">Null Renderer Filter</span></span>

> [!Note]  
> <span data-ttu-id="98ede-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="98ede-104">\[Deprecated.</span></span> <span data-ttu-id="98ede-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="98ede-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98ede-106">Le filtre de convertisseur null est un convertisseur qui ignore chaque échantillon qu’il reçoit, sans afficher ou restituer les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="98ede-106">The Null Renderer filter is a renderer that discards every sample it receives, without displaying or rendering the sample data.</span></span>



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98ede-107">Interfaces de filtre</span><span class="sxs-lookup"><span data-stu-id="98ede-107">Filter interfaces</span></span>                        | <span data-ttu-id="98ede-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span><span class="sxs-lookup"><span data-stu-id="98ede-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)</span></span> |
| <span data-ttu-id="98ede-109">Types de média de broche d’entrée</span><span class="sxs-lookup"><span data-stu-id="98ede-109">Input pin media types</span></span>                    | <span data-ttu-id="98ede-110">Tout type de média</span><span class="sxs-lookup"><span data-stu-id="98ede-110">Any media type</span></span>                                                                                                       |
| <span data-ttu-id="98ede-111">Interfaces pin d’entrée</span><span class="sxs-lookup"><span data-stu-id="98ede-111">Input pin interfaces</span></span>                     | <span data-ttu-id="98ede-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="98ede-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>               |
| <span data-ttu-id="98ede-113">Types de média de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="98ede-113">Output pin media types</span></span>                   | <span data-ttu-id="98ede-114">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="98ede-114">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="98ede-115">Interfaces de broche de sortie</span><span class="sxs-lookup"><span data-stu-id="98ede-115">Output pin interfaces</span></span>                    | <span data-ttu-id="98ede-116">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="98ede-116">Not applicable.</span></span>                                                                                                      |
| <span data-ttu-id="98ede-117">CLSID du filtre</span><span class="sxs-lookup"><span data-stu-id="98ede-117">Filter CLSID</span></span>                             | <span data-ttu-id="98ede-118">CLSID \_ NullRenderer</span><span class="sxs-lookup"><span data-stu-id="98ede-118">CLSID\_NullRenderer</span></span>                                                                                                  |
| <span data-ttu-id="98ede-119">CLSID de page de propriétés</span><span class="sxs-lookup"><span data-stu-id="98ede-119">Property Page CLSID</span></span>                      | <span data-ttu-id="98ede-120">Aucune page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="98ede-120">No property page.</span></span>                                                                                                    |
| <span data-ttu-id="98ede-121">Exécutable</span><span class="sxs-lookup"><span data-stu-id="98ede-121">Executable</span></span>                               | <span data-ttu-id="98ede-122">Qedit.dll</span><span class="sxs-lookup"><span data-stu-id="98ede-122">Qedit.dll</span></span>                                                                                                            |
| [<span data-ttu-id="98ede-123">Mérite</span><span class="sxs-lookup"><span data-stu-id="98ede-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="98ede-124">MÉRITE \_ n' \_ \_ utilise pas</span><span class="sxs-lookup"><span data-stu-id="98ede-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                  |
| [<span data-ttu-id="98ede-125">Catégorie de filtre</span><span class="sxs-lookup"><span data-stu-id="98ede-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="98ede-126">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="98ede-126">CLSID\_LegacyAmFilterCategory</span></span>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="98ede-127">Notes</span><span class="sxs-lookup"><span data-stu-id="98ede-127">Remarks</span></span>

<span data-ttu-id="98ede-128">Utilisez ce filtre quand une broche de sortie dans le graphique nécessite une connexion en aval, mais que vous ne souhaitez pas afficher les données à partir de ce code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="98ede-128">Use this filter when an output pin in the graph requires a downstream connection, but you do not wish to render the data from that pin.</span></span> <span data-ttu-id="98ede-129">En connectant la broche de sortie au convertisseur null, vous terminez la connexion sans restituer les données.</span><span class="sxs-lookup"><span data-stu-id="98ede-129">By connecting the output pin to the Null Renderer, you complete the connection without rendering the data.</span></span>

<span data-ttu-id="98ede-130">Même si ce filtre n’affiche aucun échantillon, il attend la durée de présentation de chaque exemple avant d’ignorer l’exemple.</span><span class="sxs-lookup"><span data-stu-id="98ede-130">Even though this filter does not render any samples, it does wait for each sample's presentation time before discarding the sample.</span></span> <span data-ttu-id="98ede-131">Par conséquent, le graphique s’exécutera au taux normal.</span><span class="sxs-lookup"><span data-stu-id="98ede-131">Therefore, the graph will run at the normal rate.</span></span> <span data-ttu-id="98ede-132">Si vous souhaitez que le graphique s’exécute aussi rapidement que possible, affectez la **valeur null** à l’horloge de référence.</span><span class="sxs-lookup"><span data-stu-id="98ede-132">If you want the graph the run as quickly as possible, set the reference clock to **NULL**.</span></span> <span data-ttu-id="98ede-133">Pour plus d’informations, consultez [définition de l’horloge du graphique](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="98ede-133">For more information, see [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98ede-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98ede-134">Requirements</span></span>



| <span data-ttu-id="98ede-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98ede-135">Requirement</span></span> | <span data-ttu-id="98ede-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="98ede-136">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="98ede-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="98ede-137">Header</span></span><br/> | <dl> <span data-ttu-id="98ede-138"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="98ede-138"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98ede-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98ede-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98ede-140">Objets des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="98ede-140">DirectShow Editing Services Objects</span></span>](directshow-editing-services-objects.md)
</dt> </dl>

 

 




