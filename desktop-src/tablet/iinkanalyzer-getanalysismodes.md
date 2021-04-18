---
description: Récupère les indicateurs qui contrôlent la manière dont le IInkAnalyzer effectue l’analyse de l’encre.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'IInkAnalyzer :: GetAnalysisModes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516015"
---
# <a name="iinkanalyzergetanalysismodes-method"></a><span data-ttu-id="b408b-103">IInkAnalyzer :: GetAnalysisModes, méthode</span><span class="sxs-lookup"><span data-stu-id="b408b-103">IInkAnalyzer::GetAnalysisModes method</span></span>

<span data-ttu-id="b408b-104">Récupère les indicateurs qui contrôlent la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b408b-104">Retrieves flags that control how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="b408b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b408b-105">Syntax</span></span>


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a><span data-ttu-id="b408b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b408b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b408b-107">*pAnalysisMode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b408b-107">*pAnalysisMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b408b-108">Combinaison d’opérations de bits des valeurs d’énumération [**AnalysisModes**](analysismodes.md) .</span><span class="sxs-lookup"><span data-stu-id="b408b-108">A bitwise combination of the [**AnalysisModes**](analysismodes.md) enumeration values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b408b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b408b-109">Return value</span></span>

<span data-ttu-id="b408b-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b408b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b408b-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b408b-111">Requirements</span></span>



| <span data-ttu-id="b408b-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b408b-112">Requirement</span></span> | <span data-ttu-id="b408b-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="b408b-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b408b-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b408b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b408b-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b408b-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b408b-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b408b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b408b-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b408b-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b408b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b408b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b408b-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b408b-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b408b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="b408b-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b408b-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b408b-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b408b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b408b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b408b-123">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b408b-123">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b408b-124">**AnalysisModes**</span><span class="sxs-lookup"><span data-stu-id="b408b-124">**AnalysisModes**</span></span>](analysismodes.md)
</dt> <dt>

[<span data-ttu-id="b408b-125">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b408b-125">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="b408b-126">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b408b-126">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b408b-127">**IInkAnalyzer :: SetAnalysisModes, méthode**</span><span class="sxs-lookup"><span data-stu-id="b408b-127">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="b408b-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b408b-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




