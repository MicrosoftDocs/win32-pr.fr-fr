---
description: Récupère une collection ordonnée d’objets IInkAnalysisRecognizer.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: 'IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d596a8138f8ab16852ce99116eef66372ff2b074
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862686"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a><span data-ttu-id="fc8de-103">IInkAnalyzer :: GetInkAnalysisRecognizersByPriority, méthode</span><span class="sxs-lookup"><span data-stu-id="fc8de-103">IInkAnalyzer::GetInkAnalysisRecognizersByPriority method</span></span>

<span data-ttu-id="fc8de-104">Récupère une collection ordonnée d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="fc8de-104">Retrieves an ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8de-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc8de-105">Syntax</span></span>


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a><span data-ttu-id="fc8de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc8de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8de-107">*ppInkAnalysisRecognizers* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fc8de-107">*ppInkAnalysisRecognizers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8de-108">Collection ordonnée d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="fc8de-108">An ordered collection of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8de-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc8de-109">Return value</span></span>

<span data-ttu-id="fc8de-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="fc8de-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8de-111">Notes</span><span class="sxs-lookup"><span data-stu-id="fc8de-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="fc8de-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur *ppInkAnalysisRecognizers* lorsque vous n’avez plus besoin d’utiliser l’objet.</span><span class="sxs-lookup"><span data-stu-id="fc8de-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppInkAnalysisRecognizers* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="fc8de-113">L’ordre des détecteurs dans cette collection indique l’ordre dans lequel le [**IInkAnalyzer**](iinkanalyzer.md) évalue les regroupements disponibles.</span><span class="sxs-lookup"><span data-stu-id="fc8de-113">The order of the recognizers in this collection indicates the order in which the [**IInkAnalyzer**](iinkanalyzer.md) evaluates the available recognizers.</span></span> <span data-ttu-id="fc8de-114">Le **IInkAnalyzer** utilise la langue des traits comme critère principal pour l’application d’un [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="fc8de-114">The **IInkAnalyzer** uses the language of the strokes as its primary criterion for applying an [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="fc8de-115">En tant que critère secondaire, **IInkAnalyzer** compare les informations d’indicateur d’analyse aux fonctionnalités prises en charge d’un objet **IInkAnalysisRecognizer** (consultez [**IInkAnalysisRecognizer :: GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span><span class="sxs-lookup"><span data-stu-id="fc8de-115">As a secondary criterion, the **IInkAnalyzer** compares analysis hint information against an **IInkAnalysisRecognizer** object's supported capabilities (see [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)).</span></span> <span data-ttu-id="fc8de-116">Pour plus d’informations sur les indicateurs d’analyse, consultez la [**méthode IInkAnalyzer :: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md).</span><span class="sxs-lookup"><span data-stu-id="fc8de-116">For more information about analysis hints, see [**IInkAnalyzer::CreateAnalysisHint Method**](iinkanalyzer-createanalysishint.md).</span></span>

<span data-ttu-id="fc8de-117">Si plusieurs [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) prennent en charge un identificateur de langue, le [**IInkAnalyzer**](iinkanalyzer.md) utilise un algorithme « ajusté » pour sélectionner le premier **IInkAnalysisRecognizer** pour analyser les traits de cette langue.</span><span class="sxs-lookup"><span data-stu-id="fc8de-117">If more than one [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports a language identifier, the [**IInkAnalyzer**](iinkanalyzer.md) uses a "first-fit" algorithm to select the first **IInkAnalysisRecognizer** to analyze strokes of that language.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8de-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc8de-118">Requirements</span></span>



| <span data-ttu-id="fc8de-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc8de-119">Requirement</span></span> | <span data-ttu-id="fc8de-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc8de-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8de-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8de-121">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8de-122">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc8de-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="fc8de-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8de-123">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8de-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc8de-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="fc8de-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc8de-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc8de-126"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fc8de-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fc8de-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fc8de-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc8de-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8de-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="fc8de-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc8de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8de-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="fc8de-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="fc8de-131">**IInkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="fc8de-131">**IInkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="fc8de-132">**IInkAnalyzer :: SetHighestPriorityInkAnalysisRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="fc8de-132">**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer Method**</span></span>](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="fc8de-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="fc8de-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

