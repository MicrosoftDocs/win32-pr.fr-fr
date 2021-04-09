---
description: Récupère des alternatives d’analyse pour les traits avec les identificateurs de trait spécifiés.
ms.assetid: e8bc198e-de0b-49b7-9120-4298985dfe64
title: 'IInkAnalyzer :: GetAlternatesForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternatesForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 115b2cc1be4ba35614ada6fddd9c9fbcdfa76357
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113342"
---
# <a name="iinkanalyzergetalternatesforstrokes-method"></a><span data-ttu-id="233c2-103">IInkAnalyzer :: GetAlternatesForStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="233c2-103">IInkAnalyzer::GetAlternatesForStrokes method</span></span>

<span data-ttu-id="233c2-104">Récupère des alternatives d’analyse pour les traits avec les identificateurs de trait spécifiés.</span><span class="sxs-lookup"><span data-stu-id="233c2-104">Retrieves analysis alternates for the strokes with the specified stroke identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="233c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="233c2-105">Syntax</span></span>


```C++
HRESULT GetAlternatesForStrokes(
  [in]  ULONG              ulStrokeIdsCount,
  [in]  LONG               *plStrokes,
  [in]  ULONG              ulMaximumAlternates,
  [out] AnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="233c2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="233c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233c2-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="233c2-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c2-108">Nombre d’identificateurs de trait dans *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="233c2-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="233c2-109">*plStrokes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="233c2-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c2-110">Tableau d’identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="233c2-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="233c2-111">*ulMaximumAlternates* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="233c2-111">*ulMaximumAlternates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233c2-112">Nombre maximal d’autres solutions d’analyse retournées.</span><span class="sxs-lookup"><span data-stu-id="233c2-112">The maximum number of analysis alternatives returned.</span></span>

</dd> <dt>

<span data-ttu-id="233c2-113">*ppAlternates* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="233c2-113">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="233c2-114">Objet [**IAnalysisAlternates**](ianalysisalternates.md) contenant les alternatives d’analyse.</span><span class="sxs-lookup"><span data-stu-id="233c2-114">The [**IAnalysisAlternates**](ianalysisalternates.md) object containing the analysis alternatives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233c2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="233c2-115">Return value</span></span>

<span data-ttu-id="233c2-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="233c2-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="233c2-117">Notes</span><span class="sxs-lookup"><span data-stu-id="233c2-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="233c2-118">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppAlternates* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="233c2-118">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="233c2-119">Le [**IAnalysisAlternate**](ianalysisalternate.md) supérieur est retourné en tant que premier remplacement de la collection.</span><span class="sxs-lookup"><span data-stu-id="233c2-119">The top [**IAnalysisAlternate**](ianalysisalternate.md) is returned as the first alternate of the collection.</span></span>

<span data-ttu-id="233c2-120">Les traits spécifiés n’ont pas besoin de représenter des zones adjacentes du document.</span><span class="sxs-lookup"><span data-stu-id="233c2-120">The specified strokes do not have to represent adjacent areas of the document.</span></span>

## <a name="requirements"></a><span data-ttu-id="233c2-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="233c2-121">Requirements</span></span>



| <span data-ttu-id="233c2-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="233c2-122">Requirement</span></span> | <span data-ttu-id="233c2-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="233c2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233c2-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="233c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="233c2-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="233c2-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="233c2-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="233c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="233c2-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="233c2-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="233c2-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="233c2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="233c2-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="233c2-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="233c2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="233c2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="233c2-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="233c2-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="233c2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="233c2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233c2-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="233c2-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="233c2-134">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="233c2-134">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="233c2-135">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="233c2-135">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="233c2-136">**IInkAnalyzer :: GetAlternates, méthode**</span><span class="sxs-lookup"><span data-stu-id="233c2-136">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="233c2-137">**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="233c2-137">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="233c2-138">**IInkAnalyzer :: ModifyTopAlternate, méthode**</span><span class="sxs-lookup"><span data-stu-id="233c2-138">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="233c2-139">**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**</span><span class="sxs-lookup"><span data-stu-id="233c2-139">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="233c2-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="233c2-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

