---
description: Spécifie les événements associés aux étapes du proxy de données d’un objet IInkAnalyzer.
ms.assetid: 57fee525-02e2-4721-b6e5-28112d53db2a
title: Interface _IAnalysisProxyEvents (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b83019cafb6053b9f803c815289d9f9f64d32a5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106525811"
---
# <a name="_ianalysisproxyevents-interface"></a><span data-ttu-id="ffd46-103">\_Interface IAnalysisProxyEvents</span><span class="sxs-lookup"><span data-stu-id="ffd46-103">\_IAnalysisProxyEvents interface</span></span>

<span data-ttu-id="ffd46-104">Spécifie les événements associés aux étapes du proxy de données d’un objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-104">Specifies events associated with the data proxy steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="ffd46-105">Événements</span><span class="sxs-lookup"><span data-stu-id="ffd46-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="ffd46-106">Événements</span><span class="sxs-lookup"><span data-stu-id="ffd46-106">Events</span></span>

<span data-ttu-id="ffd46-107">L’interface **\_ IAnalysisProxyEvents** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="ffd46-107">The **\_IAnalysisProxyEvents** interface has these events.</span></span>



| <span data-ttu-id="ffd46-108">Événement</span><span class="sxs-lookup"><span data-stu-id="ffd46-108">Event</span></span>                                                                                      | <span data-ttu-id="ffd46-109">Description</span><span class="sxs-lookup"><span data-stu-id="ffd46-109">Description</span></span>                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffd46-110">**ContextNodeCreated**</span><span class="sxs-lookup"><span data-stu-id="ffd46-110">**ContextNodeCreated**</span></span>](-ianalysisproxyevents-contextnodecreated.md)                     | <span data-ttu-id="ffd46-111">Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a créé un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-111">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) creates an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                  |
| [<span data-ttu-id="ffd46-112">**ContextNodeDeleting**</span><span class="sxs-lookup"><span data-stu-id="ffd46-112">**ContextNodeDeleting**</span></span>](-ianalysisproxyevents-contextnodedeleting.md)                   | <span data-ttu-id="ffd46-113">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-113">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                                                 |
| [<span data-ttu-id="ffd46-114">**ContextNodeLinkAdding**</span><span class="sxs-lookup"><span data-stu-id="ffd46-114">**ContextNodeLinkAdding**</span></span>](-ianalysisproxyevents-contextnodelinkadding.md)               | <span data-ttu-id="ffd46-115">Se produit avant que [**IInkAnalyzer**](iinkanalyzer.md) ajoute un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-115">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) adds an [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>           |
| [<span data-ttu-id="ffd46-116">**ContextNodeLinkDeleting**</span><span class="sxs-lookup"><span data-stu-id="ffd46-116">**ContextNodeLinkDeleting**</span></span>](-ianalysisproxyevents-contextnodelinkdeleting.md)           | <span data-ttu-id="ffd46-117">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) supprime un objet [**IContextLink**](icontextlink.md) entre deux objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-117">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) deletes a [**IContextLink**](icontextlink.md) object between two [**IContextNode**](icontextnode.md) objects.</span></span><br/>         |
| [<span data-ttu-id="ffd46-118">**ContextNodeMovingToPosition**</span><span class="sxs-lookup"><span data-stu-id="ffd46-118">**ContextNodeMovingToPosition**</span></span>](-ianalysisproxyevents-contextnodemovingtoposition.md)   | <span data-ttu-id="ffd46-119">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) vers une nouvelle position dans la collection de sous-nœuds du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ffd46-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object to a new position within its parent node's collection of subnodes.</span></span><br/> |
| [<span data-ttu-id="ffd46-120">**ContextNodePropertiesUpdated**</span><span class="sxs-lookup"><span data-stu-id="ffd46-120">**ContextNodePropertiesUpdated**</span></span>](-ianalysisproxyevents-contextnodepropertiesupdated.md) | <span data-ttu-id="ffd46-121">Se produit après que le [**IInkAnalyzer**](iinkanalyzer.md) a mis à jour une ou plusieurs propriétés d’un objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd46-121">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span><br/>                                        |
| [<span data-ttu-id="ffd46-122">**ContextNodeReparenting**</span><span class="sxs-lookup"><span data-stu-id="ffd46-122">**ContextNodeReparenting**</span></span>](-ianalysisproxyevents-contextnodereparenting.md)             | <span data-ttu-id="ffd46-123">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) déplace un objet [**IContextNode**](icontextnode.md) en modifiant son nœud parent.</span><span class="sxs-lookup"><span data-stu-id="ffd46-123">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) moves an [**IContextNode**](icontextnode.md) object by changing its parent node.</span></span><br/>                                       |
| [<span data-ttu-id="ffd46-124">**InkAnalyzerStateChanging**</span><span class="sxs-lookup"><span data-stu-id="ffd46-124">**InkAnalyzerStateChanging**</span></span>](-ianalysisproxyevents-inkanalyzerstatechanging.md)         | <span data-ttu-id="ffd46-125">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) ne rapproche les résultats de l’analyse afin qu’une application puisse synchroniser les données avec le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="ffd46-125">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) reconciles analysis results so that an application can synchronize data with the **IInkAnalyzer**.</span></span><br/>                      |
| [<span data-ttu-id="ffd46-126">**PopulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="ffd46-126">**PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)                   | <span data-ttu-id="ffd46-127">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse dans la région d’un objet [**IContextNode**](icontextnode.md) partiellement rempli.</span><span class="sxs-lookup"><span data-stu-id="ffd46-127">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) performs analysis within the region of a partially populated [**IContextNode**](icontextnode.md) object.</span></span><br/>               |
| [<span data-ttu-id="ffd46-128">**StrokeReparented**</span><span class="sxs-lookup"><span data-stu-id="ffd46-128">**StrokeReparented**</span></span>](-ianalysisproxyevents-strokereparented.md)                         | <span data-ttu-id="ffd46-129">Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) déplace un trait d’un objet [**IContextNode**](icontextnode.md) à un autre.</span><span class="sxs-lookup"><span data-stu-id="ffd46-129">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) moves a stroke from one [**IContextNode**](icontextnode.md) object to another.</span></span><br/>                                           |



 

## <a name="remarks"></a><span data-ttu-id="ffd46-130">Notes</span><span class="sxs-lookup"><span data-stu-id="ffd46-130">Remarks</span></span>

<span data-ttu-id="ffd46-131">Utilisez ces événements lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ffd46-131">Use these events when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ffd46-132">Pour plus d’informations sur la synchronisation des données de votre application avec **IInkAnalyzer**, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ffd46-132">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd46-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ffd46-133">Requirements</span></span>



| <span data-ttu-id="ffd46-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ffd46-134">Requirement</span></span> | <span data-ttu-id="ffd46-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ffd46-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd46-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffd46-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd46-137">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ffd46-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ffd46-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffd46-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd46-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ffd46-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ffd46-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ffd46-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd46-141"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd46-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ffd46-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ffd46-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd46-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffd46-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ffd46-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ffd46-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffd46-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ffd46-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ffd46-146">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ffd46-146">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ffd46-147">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="ffd46-147">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ffd46-148">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="ffd46-148">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ffd46-149">\_IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="ffd46-149">\_IAnalysisEvents</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="ffd46-150">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ffd46-150">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

