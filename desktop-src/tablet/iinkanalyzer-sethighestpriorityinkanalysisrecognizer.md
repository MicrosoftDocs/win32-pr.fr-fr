---
description: Déplace le IInkAnalysisRecognizer spécifié à la première position dans la liste de reconnaissance d’encre de l’objet IInkAnalyzer.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: 'IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 534b94e4f2964aa81f04e0adac6f45f346c530c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862682"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a><span data-ttu-id="9db47-103">IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode</span><span class="sxs-lookup"><span data-stu-id="9db47-103">IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer method</span></span>

<span data-ttu-id="9db47-104">Déplace le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) spécifié à la première position dans la liste de reconnaissance d’encre de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="9db47-104">Moves the specified [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to the first position in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

## <a name="syntax"></a><span data-ttu-id="9db47-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9db47-105">Syntax</span></span>


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a><span data-ttu-id="9db47-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9db47-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9db47-107">*pInkAnalysisRecognizer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9db47-107">*pInkAnalysisRecognizer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9db47-108">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) à placer à la première position.</span><span class="sxs-lookup"><span data-stu-id="9db47-108">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) to place in the first position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9db47-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9db47-109">Return value</span></span>

<span data-ttu-id="9db47-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9db47-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9db47-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9db47-111">Remarks</span></span>

<span data-ttu-id="9db47-112">Pour récupérer la liste des détecteurs d’encre par ordre de priorité, appelez la [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span><span class="sxs-lookup"><span data-stu-id="9db47-112">To get the list of ink recognizers in priority order, call [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md).</span></span>

<span data-ttu-id="9db47-113">Cette méthode n’affecte pas l’ordre des autres objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans la liste des reconnaissance d’encre de l’objet [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="9db47-113">This method does not affect the order of the rest of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md) object's list of ink recognizers.</span></span>

<span data-ttu-id="9db47-114">L’ordre des détecteurs d’encre retournés par la [**méthode IInkAnalyzer :: GetInkAnalysisRecognizersByPriority**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indique l’ordre dans lequel le [**IInkAnalyzer**](iinkanalyzer.md) évalue les objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) disponibles.</span><span class="sxs-lookup"><span data-stu-id="9db47-114">The order of the ink recognizers returned by [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

<span data-ttu-id="9db47-115">L’utilisation des reconnaissances d’encre est évaluée en fonction de leur ordre dans la liste.</span><span class="sxs-lookup"><span data-stu-id="9db47-115">Use of the ink recognizers is evaluated based on their order in the list.</span></span>

<span data-ttu-id="9db47-116">Pendant l’analyse de l’encre, [**IInkAnalyzer**](iinkanalyzer.md) itère au sein des détecteurs d’encre dans sa liste jusqu’à ce qu’il trouve un module de reconnaissance qui prend en charge la langue et d’autres propriétés des traits.</span><span class="sxs-lookup"><span data-stu-id="9db47-116">During ink analysis, the [**IInkAnalyzer**](iinkanalyzer.md) iterates through the ink recognizers in its list until it finds a recognizer that supports the language and other properties of the strokes.</span></span> <span data-ttu-id="9db47-117">Ce module de reconnaissance est utilisé pour la reconnaissance de l’encre pour ces traits.</span><span class="sxs-lookup"><span data-stu-id="9db47-117">This recognizer is used for ink recognition for those strokes.</span></span>

<span data-ttu-id="9db47-118">Si le [**IInkAnalyzer**](iinkanalyzer.md) ne trouve pas de [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) qui prend en charge un ensemble de traits pendant l’analyse, le **IInkAnalyzer** génère un [**IAnalysisWarning**](ianalysiswarning.md) avec un code d’avertissement de **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (consultez [**IAnalysisWarning :: GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span><span class="sxs-lookup"><span data-stu-id="9db47-118">If the [**IInkAnalyzer**](iinkanalyzer.md) does not find an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) that supports a set of strokes during analysis, the **IInkAnalyzer** generates an [**IAnalysisWarning**](ianalysiswarning.md) with a warning code of **AnalysisWarningCode\_InkAnalysisRecognizerNotInstalled** (see [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9db47-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9db47-119">Requirements</span></span>



| <span data-ttu-id="9db47-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9db47-120">Requirement</span></span> | <span data-ttu-id="9db47-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9db47-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9db47-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db47-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9db47-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9db47-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9db47-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db47-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9db47-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9db47-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9db47-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9db47-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9db47-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9db47-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9db47-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9db47-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9db47-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9db47-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9db47-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9db47-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9db47-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="9db47-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="9db47-132">**IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode**</span><span class="sxs-lookup"><span data-stu-id="9db47-132">**IInkAnalyzer::GetInkAnalysisRecognizersByPriority Method**</span></span>](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[<span data-ttu-id="9db47-133">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="9db47-133">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="9db47-134">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="9db47-134">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="9db47-135">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="9db47-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




