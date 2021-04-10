---
description: Supprime un indicateur d’analyse de IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: IInkAnalyzer ::D méthode eleteAnalysisHint (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113351"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a><span data-ttu-id="b14b4-103">IInkAnalyzer ::D méthode eleteAnalysisHint</span><span class="sxs-lookup"><span data-stu-id="b14b4-103">IInkAnalyzer::DeleteAnalysisHint method</span></span>

<span data-ttu-id="b14b4-104">Supprime un indicateur d’analyse de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b14b4-104">Removes an analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b14b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b14b4-105">Syntax</span></span>


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a><span data-ttu-id="b14b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b14b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14b4-107">*pHintToDelete* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b14b4-107">*pHintToDelete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14b4-108">Indicateur d’analyse de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b14b4-108">The analysis hint from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14b4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b14b4-109">Return value</span></span>

<span data-ttu-id="b14b4-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b14b4-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b14b4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b14b4-111">Remarks</span></span>

<span data-ttu-id="b14b4-112">La suppression d’un indicateur d’analyse ne marque pas la zone de l’indicateur pour la réanalyse.</span><span class="sxs-lookup"><span data-stu-id="b14b4-112">Removing an analysis hint does not mark the hint's area for reanalysis.</span></span> <span data-ttu-id="b14b4-113">Pour marquer la zone dans l’indicateur pour la réanalyse, utilisez la [**méthode IInkAnalyzer :: SetDirtyRegion**](iinkanalyzer-setdirtyregion.md) pour définir la région de modification sur l’Union de la région et de la zone de modification actuelles de l’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="b14b4-113">To mark the area within the hint for reanalysis, use [**IInkAnalyzer::SetDirtyRegion Method**](iinkanalyzer-setdirtyregion.md) to set the dirty region to the union of the current dirty region and area of the analysis hint.</span></span>

<span data-ttu-id="b14b4-114">L’indicateur est supprimé de l’analyseur. Toutefois, le [**IContextNode**](icontextnode.md) lui-même n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="b14b4-114">The hint is removed from the analyzer; however, the [**IContextNode**](icontextnode.md) itself is not deleted.</span></span>

<span data-ttu-id="b14b4-115">Cette méthode retourne un code d’erreur quand *pHintToDelete* est un [**IContextNode**](icontextnode.md) qui n’est pas de type AnalysisHint (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="b14b4-115">This method returns an error code when *pHintToDelete* is a [**IContextNode**](icontextnode.md) that is not of type AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b14b4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b14b4-116">Requirements</span></span>



| <span data-ttu-id="b14b4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b14b4-117">Requirement</span></span> | <span data-ttu-id="b14b4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b14b4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14b4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b14b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b14b4-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b14b4-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b14b4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b14b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b14b4-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b14b4-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b14b4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b14b4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14b4-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b14b4-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b14b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b14b4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b14b4-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b14b4-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b14b4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b14b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14b4-128">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b14b4-128">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b14b4-129">**IInkAnalyzer :: CreateAnalysisHint, méthode**</span><span class="sxs-lookup"><span data-stu-id="b14b4-129">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="b14b4-130">**IInkAnalyzer :: GetAnalysisHints, méthode**</span><span class="sxs-lookup"><span data-stu-id="b14b4-130">**IInkAnalyzer::GetAnalysisHints Method**</span></span>](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[<span data-ttu-id="b14b4-131">**IInkAnalyzer :: GetAnalysisHintsByName, méthode**</span><span class="sxs-lookup"><span data-stu-id="b14b4-131">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="b14b4-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b14b4-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




