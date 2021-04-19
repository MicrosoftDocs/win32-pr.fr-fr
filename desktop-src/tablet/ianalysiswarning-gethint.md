---
description: Récupère l’indicateur d’analyse à l’origine de cet avertissement.
ms.assetid: 715aa4b2-6c45-414b-96f2-44c73a073213
title: 'IAnalysisWarning :: GetHint, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2c38a22b799eb6836a85a42748f60207ee7e997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538644"
---
# <a name="ianalysiswarninggethint-method"></a><span data-ttu-id="879e1-103">IAnalysisWarning :: GetHint, méthode</span><span class="sxs-lookup"><span data-stu-id="879e1-103">IAnalysisWarning::GetHint method</span></span>

<span data-ttu-id="879e1-104">Récupère l’indicateur d’analyse à l’origine de cet avertissement.</span><span class="sxs-lookup"><span data-stu-id="879e1-104">Retrieves the analysis hint that caused this warning.</span></span>

## <a name="syntax"></a><span data-ttu-id="879e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="879e1-105">Syntax</span></span>


```C++
HRESULT GetHint(
  [out] IContextNode **pAnalysisHint
);
```



## <a name="parameters"></a><span data-ttu-id="879e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="879e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="879e1-107">*pAnalysisHint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="879e1-107">*pAnalysisHint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="879e1-108">Nœud de contexte d’indicateur d’analyse qui a provoqué cet avertissement, ou **null** si un indicateur d’analyse n’a pas provoqué cet avertissement.</span><span class="sxs-lookup"><span data-stu-id="879e1-108">The analysis hint context node that caused this warning, or **NULL** if an analysis hint did not cause this warning.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="879e1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="879e1-109">Return value</span></span>

<span data-ttu-id="879e1-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="879e1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="879e1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="879e1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="879e1-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pAnalysisHint* lorsque vous n’avez plus besoin d’utiliser le nœud de contexte d’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="879e1-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAnalysisHint* when you no longer need to use the analysis hint context node.</span></span>

 

<span data-ttu-id="879e1-113">Un exemple d’indicateur d’analyse qui génère un [**IAnalysisWarning**](ianalysiswarning.md) est un indicateur d’analyse qui contient un Factoid mal orthographié.</span><span class="sxs-lookup"><span data-stu-id="879e1-113">An example of an analysis hint that generates an [**IAnalysisWarning**](ianalysiswarning.md) is an analysis hint that contains an incorrectly spelled factoid.</span></span> <span data-ttu-id="879e1-114">Dans ce cas, l’analyse des encres retourne un [**IAnalysisStatus**](ianalysisstatus.md) qui contient un **IAnalysisWarning** qui fait référence au nœud de contexte d’indicateur d’analyse avec le Factoid mal orthographié.</span><span class="sxs-lookup"><span data-stu-id="879e1-114">In this case, ink analysis returns an [**IAnalysisStatus**](ianalysisstatus.md) that contains an **IAnalysisWarning** that references the analysis hint context node with the misspelled factoid.</span></span> <span data-ttu-id="879e1-115">En outre, dans ce cas, la méthode [**IAnalysisWarning :: GetWarningCode**](ianalysiswarning-getwarningcode.md) de l’avertissement d’analyse retourne une valeur [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) de **AnalysisWarningCode \_ FactoidNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="879e1-115">Also, in this case, the analysis warning's [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md) method returns an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) value of **AnalysisWarningCode\_FactoidNotSupported**.</span></span>

## <a name="requirements"></a><span data-ttu-id="879e1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="879e1-116">Requirements</span></span>



| <span data-ttu-id="879e1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="879e1-117">Requirement</span></span> | <span data-ttu-id="879e1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="879e1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="879e1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="879e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="879e1-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="879e1-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="879e1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="879e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="879e1-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="879e1-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="879e1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="879e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="879e1-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="879e1-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="879e1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="879e1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="879e1-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="879e1-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="879e1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="879e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879e1-128">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="879e1-128">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="879e1-129">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="879e1-129">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="879e1-130">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="879e1-130">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="879e1-131">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="879e1-131">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="879e1-132">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="879e1-132">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="879e1-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="879e1-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

