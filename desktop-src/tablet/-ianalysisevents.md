---
description: Spécifie les événements associés aux étapes d’analyse d’un objet IInkAnalyzer.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: Interface _IAnalysisEvents
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541217"
---
# <a name="_ianalysisevents-interface"></a><span data-ttu-id="792d5-103">\_Interface IAnalysisEvents</span><span class="sxs-lookup"><span data-stu-id="792d5-103">\_IAnalysisEvents interface</span></span>

<span data-ttu-id="792d5-104">Spécifie les événements associés aux étapes d’analyse d’un objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="792d5-104">Specifies events associated with the analysis steps of an [**IInkAnalyzer**](iinkanalyzer.md) object.</span></span>

-   [<span data-ttu-id="792d5-105">Événements</span><span class="sxs-lookup"><span data-stu-id="792d5-105">Events</span></span>](/windows)

### <a name="events"></a><span data-ttu-id="792d5-106">Événements</span><span class="sxs-lookup"><span data-stu-id="792d5-106">Events</span></span>

<span data-ttu-id="792d5-107">L’interface **\_ IAnalysisEvents** contient ces événements.</span><span class="sxs-lookup"><span data-stu-id="792d5-107">The **\_IAnalysisEvents** interface has these events.</span></span>



| <span data-ttu-id="792d5-108">Événement</span><span class="sxs-lookup"><span data-stu-id="792d5-108">Event</span></span>                                                               | <span data-ttu-id="792d5-109">Description</span><span class="sxs-lookup"><span data-stu-id="792d5-109">Description</span></span>                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="792d5-110">**Activité**</span><span class="sxs-lookup"><span data-stu-id="792d5-110">**Activity**</span></span>](-ianalysisevents-activity.md)                       | <span data-ttu-id="792d5-111">Se produit lors des appels à la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou à la méthode [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) .</span><span class="sxs-lookup"><span data-stu-id="792d5-111">Occurs during calls to the [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md) or [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method.</span></span><br/> |
| [<span data-ttu-id="792d5-112">**IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="792d5-112">**IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md) | <span data-ttu-id="792d5-113">Se produit lorsque l’étape d’analyse intermédiaire actuelle est terminée.</span><span class="sxs-lookup"><span data-stu-id="792d5-113">Occurs when the current intermediate analysis stage is finished.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="792d5-114">**ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="792d5-114">**ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)       | <span data-ttu-id="792d5-115">Se produit lorsque le [**IInkAnalyzer**](iinkanalyzer.md) est prêt à rapprocher les résultats de l’analyse en arrière-plan avec son état actuel.</span><span class="sxs-lookup"><span data-stu-id="792d5-115">Occurs when the [**IInkAnalyzer**](iinkanalyzer.md) is ready to reconcile its background analysis results with its current state.</span></span><br/>                                                  |
| [<span data-ttu-id="792d5-116">**Résultats**</span><span class="sxs-lookup"><span data-stu-id="792d5-116">**Results**</span></span>](-ianalysisevents-results.md)                         | <span data-ttu-id="792d5-117">Se produit lorsque l’étape d’analyse finale est terminée.</span><span class="sxs-lookup"><span data-stu-id="792d5-117">Occurs when the final analysis stage is finished.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="792d5-118">**UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="792d5-118">**UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)   | <span data-ttu-id="792d5-119">Se produit avant que le [**IInkAnalyzer**](iinkanalyzer.md) accède aux données de trait.</span><span class="sxs-lookup"><span data-stu-id="792d5-119">Occurs before the [**IInkAnalyzer**](iinkanalyzer.md) accesses stroke data.</span></span><br/>                                                                                                        |



 

## <a name="requirements"></a><span data-ttu-id="792d5-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="792d5-120">Requirements</span></span>



| <span data-ttu-id="792d5-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="792d5-121">Requirement</span></span> | <span data-ttu-id="792d5-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="792d5-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="792d5-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="792d5-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="792d5-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="792d5-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="792d5-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="792d5-126">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="792d5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="792d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="792d5-128">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="792d5-128">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="792d5-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="792d5-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="792d5-130">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="792d5-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="792d5-131">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="792d5-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="792d5-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="792d5-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

