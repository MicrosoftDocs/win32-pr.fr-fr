---
description: Se produit avant que le IInkAnalyzer accède aux données de trait.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: '_IAnalysisEvents :: UpdateStrokesCache, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106520247"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a><span data-ttu-id="29cda-103">\_Événement IAnalysisEvents :: UpdateStrokesCache</span><span class="sxs-lookup"><span data-stu-id="29cda-103">\_IAnalysisEvents::UpdateStrokesCache event</span></span>

<span data-ttu-id="29cda-104">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) accède aux données de trait.</span><span class="sxs-lookup"><span data-stu-id="29cda-104">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span>

## <a name="syntax"></a><span data-ttu-id="29cda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29cda-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="29cda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29cda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29cda-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29cda-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29cda-108">Nombre d’identificateurs de trait dans *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="29cda-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="29cda-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="29cda-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29cda-110">Identificateurs des traits dont les données de paquet ont été effacées.</span><span class="sxs-lookup"><span data-stu-id="29cda-110">The identifiers of the strokes whose packet data has been cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29cda-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29cda-111">Return value</span></span>

<span data-ttu-id="29cda-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="29cda-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="29cda-113">Notes</span><span class="sxs-lookup"><span data-stu-id="29cda-113">Remarks</span></span>

<span data-ttu-id="29cda-114">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement lors de l’analyse de l’encre lorsqu’il accède à un ou plusieurs traits pour lesquels les données du paquet ont été effacées.</span><span class="sxs-lookup"><span data-stu-id="29cda-114">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event during ink analysis when it accesses one or more strokes for which the packet data has been cleared.</span></span> <span data-ttu-id="29cda-115">Pour mettre à jour les données de paquets de trait, utilisez la méthode de [**méthode IInkAnalyzer :: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md) .</span><span class="sxs-lookup"><span data-stu-id="29cda-115">To update the stroke packet data, use the [**IInkAnalyzer::UpdateStrokesData Method**](iinkanalyzer-updatestrokesdata.md) method.</span></span>

<span data-ttu-id="29cda-116">[**IInkAnalyzer**](iinkanalyzer.md) ne déclenche pas cet événement lors de l’accès à un nœud de feuille manuscrite partiellement rempli lorsque l’emplacement du nœud n’a pas été défini par le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="29cda-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not raise this event when accessing a partially populated ink leaf node when the location of the node has not been set by the **IInkAnalyzer**.</span></span>

<span data-ttu-id="29cda-117">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="29cda-117">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29cda-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29cda-118">Requirements</span></span>



| <span data-ttu-id="29cda-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29cda-119">Requirement</span></span> | <span data-ttu-id="29cda-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="29cda-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29cda-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29cda-121">Minimum supported client</span></span><br/> | <span data-ttu-id="29cda-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29cda-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29cda-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29cda-123">Minimum supported server</span></span><br/> | <span data-ttu-id="29cda-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="29cda-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="29cda-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="29cda-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="29cda-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="29cda-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="29cda-127">DLL</span><span class="sxs-lookup"><span data-stu-id="29cda-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29cda-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29cda-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="29cda-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29cda-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29cda-130">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="29cda-130">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="29cda-131">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="29cda-131">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="29cda-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="29cda-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="29cda-133">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="29cda-133">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="29cda-134">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="29cda-134">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="29cda-135">**IInkAnalyzer :: UpdateStrokesData, méthode**</span><span class="sxs-lookup"><span data-stu-id="29cda-135">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="29cda-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="29cda-136">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="29cda-137">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="29cda-137">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="29cda-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="29cda-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




