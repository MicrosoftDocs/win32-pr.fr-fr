---
description: Obtient une valeur qui indique le niveau de confiance de l’IInkAnalyzer dans la précision du IAnalysisAlternate.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'IAnalysisAlternate :: GetRecognitionConfidence, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751884"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a><span data-ttu-id="ebfe2-103">IAnalysisAlternate :: GetRecognitionConfidence, méthode</span><span class="sxs-lookup"><span data-stu-id="ebfe2-103">IAnalysisAlternate::GetRecognitionConfidence method</span></span>

<span data-ttu-id="ebfe2-104">Obtient une valeur qui indique le niveau de confiance de l' [**IInkAnalyzer**](iinkanalyzer.md) dans la précision du [**IAnalysisAlternate**](ianalysisalternate.md).</span><span class="sxs-lookup"><span data-stu-id="ebfe2-104">Gets a value that indicates the level of confidence that the [**IInkAnalyzer**](iinkanalyzer.md) has in the accuracy of the [**IAnalysisAlternate**](ianalysisalternate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ebfe2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebfe2-105">Syntax</span></span>


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a><span data-ttu-id="ebfe2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebfe2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebfe2-107">*pConfidence* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ebfe2-107">*pConfidence* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebfe2-108">Pointeur vers une [**énumération InkRecognitionConfidence**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) qui indique le niveau de confiance que le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) a dans la précision de l’alternative de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ebfe2-108">A pointer to an [**InkRecognitionConfidence Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) that indicates the level of confidence that the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) has in the accuracy of the recognition alternate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebfe2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebfe2-109">Return value</span></span>

<span data-ttu-id="ebfe2-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="ebfe2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ebfe2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebfe2-111">Requirements</span></span>



| <span data-ttu-id="ebfe2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebfe2-112">Requirement</span></span> | <span data-ttu-id="ebfe2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebfe2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebfe2-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebfe2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ebfe2-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebfe2-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ebfe2-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebfe2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ebfe2-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebfe2-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ebfe2-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebfe2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebfe2-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ebfe2-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ebfe2-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ebfe2-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebfe2-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ebfe2-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ebfe2-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebfe2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebfe2-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="ebfe2-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="ebfe2-124">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ebfe2-124">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ebfe2-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="ebfe2-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="ebfe2-126">**RecognitionConfidence**</span><span class="sxs-lookup"><span data-stu-id="ebfe2-126">**RecognitionConfidence**</span></span>](recognitionconfidence.md)
</dt> <dt>

[<span data-ttu-id="ebfe2-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="ebfe2-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




