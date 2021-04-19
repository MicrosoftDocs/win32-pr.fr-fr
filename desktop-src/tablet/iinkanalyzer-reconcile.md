---
description: 'Applique les résultats d’une opération d’analyse d’encre en arrière-plan à l’arborescence du nœud de contexte pour les parties de l’arborescence qui n’ont pas été modifiées par l’application depuis l’appel à la méthode IInkAnalyzer :: BackgroundAnalyze.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'IInkAnalyzer :: Reconcile, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514444"
---
# <a name="iinkanalyzerreconcile-method"></a><span data-ttu-id="3d628-103">IInkAnalyzer :: Reconcile, méthode</span><span class="sxs-lookup"><span data-stu-id="3d628-103">IInkAnalyzer::Reconcile method</span></span>

<span data-ttu-id="3d628-104">Applique les résultats d’une opération d’analyse d’encre en arrière-plan à l’arborescence du nœud de contexte pour les parties de l’arborescence qui n’ont pas été modifiées par l’application depuis l’appel à la [**méthode IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="3d628-104">Applies the results of a background ink analysis operation to the context node tree for the portions of the tree that have not been modified by the application since the call to [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d628-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d628-105">Syntax</span></span>


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a><span data-ttu-id="3d628-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d628-106">Parameters</span></span>

<span data-ttu-id="3d628-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="3d628-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d628-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3d628-108">Return value</span></span>

<span data-ttu-id="3d628-109">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3d628-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d628-110">Notes</span><span class="sxs-lookup"><span data-stu-id="3d628-110">Remarks</span></span>

<span data-ttu-id="3d628-111">Par défaut, le [**IInkAnalyzer**](iinkanalyzer.md) exécute une phase de réconciliation automatique immédiatement avant de déclencher les événements [**\_ IAnalysisEvents :: IntermediateResults**](-ianalysisevents-intermediateresults.md) et [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="3d628-111">By default, the [**IInkAnalyzer**](iinkanalyzer.md) performs an automatic reconciliation phase immediately before raising the [**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) and [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) events.</span></span>

<span data-ttu-id="3d628-112">Pour désactiver le rapprochement automatique, désactivez l’indicateur **AnalysisModes \_ AutomaticReconciliation** des modes d’analyse de l’analyseur d’encre (voir [**méthode IInkAnalyzer :: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md) et [**AnalysisModes**](analysismodes.md)).</span><span class="sxs-lookup"><span data-stu-id="3d628-112">To disable automatic reconciliation, clear the **AnalysisModes\_AutomaticReconciliation** flag from the ink analyzer's analysis modes (see [**IInkAnalyzer::SetAnalysisModes Method**](iinkanalyzer-setanalysismodes.md) and [**AnalysisModes**](analysismodes.md)).</span></span> <span data-ttu-id="3d628-113">La méthode [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) retourne une erreur lorsque le rapprochement automatique est désactivé et que votre application ne gère pas l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) .</span><span class="sxs-lookup"><span data-stu-id="3d628-113">The [**IInkAnalyzer::BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) method returns an error when automatic reconciliation is disabled and your application does not handle the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event.</span></span> <span data-ttu-id="3d628-114">Votre application doit appeler la méthode **IInkAnalyzer :: réconcilie** pour que le [**IInkAnalyzer**](iinkanalyzer.md) puisse continuer à traiter les résultats ou continuer l’analyse pour l’étape d’analyse correspondante.</span><span class="sxs-lookup"><span data-stu-id="3d628-114">Your application must call the **IInkAnalyzer::Reconcile Method** method before the [**IInkAnalyzer**](iinkanalyzer.md) can continue to process the results or continue further analysis for the corresponding analysis stage.</span></span>

<span data-ttu-id="3d628-115">Votre application peut apporter des modifications, telles que l’ajout ou la suppression de traits et la modification des données de trait, dans l’arborescence du nœud de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) lors de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3d628-115">Your application can make changes, such as adding or removing strokes and changing stroke data, in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree during background analysis.</span></span> <span data-ttu-id="3d628-116">Ces modifications peuvent invalider certaines parties des résultats de l’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="3d628-116">Such changes can invalidate portions of the background analysis results.</span></span> <span data-ttu-id="3d628-117">Cette méthode applique uniquement les résultats d’analyse à l’arborescence du nœud de contexte de l’analyseur pour les parties de l’arborescence que votre application n’a pas modifiées.</span><span class="sxs-lookup"><span data-stu-id="3d628-117">This method applies analysis results only to the analyzer's context node tree for the portions of the tree that your application has not changed.</span></span> <span data-ttu-id="3d628-118">Cette méthode ajoute également des régions contenant des résultats d’analyse non valides à la région de modification de l’objet **IInkAnalyzer** (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="3d628-118">This method also adds regions containing invalidated analysis results to the **IInkAnalyzer** object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="3d628-119">Pour plus d’informations sur l’utilisation du pour analyser l’encre, consultez [vue d’ensemble](ink-analysis-overview.md)de l’analyse de l’encre. [**AnalysisModes**](analysismodes.md)</span><span class="sxs-lookup"><span data-stu-id="3d628-119">For more information about using the to analyze ink, see [Ink Analysis Overview](ink-analysis-overview.md).[**AnalysisModes**](analysismodes.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="3d628-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d628-120">Requirements</span></span>



| <span data-ttu-id="3d628-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d628-121">Requirement</span></span> | <span data-ttu-id="3d628-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d628-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d628-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d628-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3d628-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d628-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3d628-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d628-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3d628-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d628-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3d628-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d628-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d628-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3d628-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3d628-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3d628-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d628-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d628-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3d628-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d628-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d628-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="3d628-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="3d628-133">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="3d628-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="3d628-134">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="3d628-134">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="3d628-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3d628-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




