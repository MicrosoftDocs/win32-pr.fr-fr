---
description: Récupère 10 autres analyses d’analyse pour toutes les entrées manuscrites associées au IInkAnalyzer.
ms.assetid: 42b702cf-54a3-413b-9f3a-dcdae7c2e89b
title: 'IInkAnalyzer :: GetAlternates, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 37219226e651e286a6d1d63accbd7e548b3b7807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513427"
---
# <a name="iinkanalyzergetalternates-method"></a><span data-ttu-id="088fb-103">IInkAnalyzer :: GetAlternates, méthode</span><span class="sxs-lookup"><span data-stu-id="088fb-103">IInkAnalyzer::GetAlternates method</span></span>

<span data-ttu-id="088fb-104">Récupère 10 autres analyses d’analyse pour toutes les entrées manuscrites associées au [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="088fb-104">Retrieves 10 analysis alternates for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="088fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="088fb-105">Syntax</span></span>


```C++
HRESULT GetAlternates(
  [out] IAnalysisAlternates **ppAlternates
);
```



## <a name="parameters"></a><span data-ttu-id="088fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="088fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="088fb-107">*ppAlternates* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="088fb-107">*ppAlternates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="088fb-108">Pointeur vers les 10 premiers objets [**IAnalysisAlternate**](ianalysisalternate.md) pour toutes les entrées manuscrites associées au [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="088fb-108">A pointer to the top 10 [**IAnalysisAlternate**](ianalysisalternate.md) objects for all ink associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="088fb-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="088fb-109">Return value</span></span>

<span data-ttu-id="088fb-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="088fb-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="088fb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="088fb-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="088fb-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppAlternates* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="088fb-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAlternates* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="088fb-113">L’alternative supérieure est retournée en tant que premier remplacement de la collection.</span><span class="sxs-lookup"><span data-stu-id="088fb-113">The top alternate is returned as the first alternate of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="088fb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="088fb-114">Requirements</span></span>



| <span data-ttu-id="088fb-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="088fb-115">Requirement</span></span> | <span data-ttu-id="088fb-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="088fb-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="088fb-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="088fb-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="088fb-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="088fb-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="088fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="088fb-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="088fb-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="088fb-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="088fb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="088fb-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="088fb-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="088fb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="088fb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="088fb-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="088fb-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="088fb-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="088fb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="088fb-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="088fb-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="088fb-127">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="088fb-127">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="088fb-128">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="088fb-128">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="088fb-129">**IInkAnalyzer :: GetAlternatesForContextNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="088fb-129">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="088fb-130">**IInkAnalyzer :: GetAlternatesForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="088fb-130">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="088fb-131">**IInkAnalyzer :: ModifyTopAlternate, méthode**</span><span class="sxs-lookup"><span data-stu-id="088fb-131">**IInkAnalyzer::ModifyTopAlternate Method**</span></span>](iinkanalyzer-modifytopalternate.md)
</dt> <dt>

[<span data-ttu-id="088fb-132">**IInkAnalyzer :: ModifyTopAlternateWithConfirmation, méthode**</span><span class="sxs-lookup"><span data-stu-id="088fb-132">**IInkAnalyzer::ModifyTopAlternateWithConfirmation Method**</span></span>](iinkanalyzer-modifytopalternatewithconfirmation.md)
</dt> <dt>

[<span data-ttu-id="088fb-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="088fb-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

