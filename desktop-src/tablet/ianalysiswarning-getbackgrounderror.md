---
description: Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.
ms.assetid: 0255751e-9b2a-46f1-aa45-6509f9d1c658
title: 'IAnalysisWarning :: GetBackgroundError, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetBackgroundError
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4367b1d52ee5d2a3bb65af0e4edd4922b8ae9a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201515"
---
# <a name="ianalysiswarninggetbackgrounderror-method"></a><span data-ttu-id="b1f18-103">IAnalysisWarning :: GetBackgroundError, méthode</span><span class="sxs-lookup"><span data-stu-id="b1f18-103">IAnalysisWarning::GetBackgroundError method</span></span>

<span data-ttu-id="b1f18-104">Récupère le code d’erreur de l’opération d’analyse de l’encre en arrière-plan si une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="b1f18-104">Retrieves the error code for the background ink analysis operation if an error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f18-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1f18-105">Syntax</span></span>


```C++
HRESULT GetBackgroundError();
```



## <a name="parameters"></a><span data-ttu-id="b1f18-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b1f18-106">Parameters</span></span>

<span data-ttu-id="b1f18-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b1f18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1f18-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b1f18-108">Return value</span></span>

<span data-ttu-id="b1f18-109">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b1f18-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1f18-110">Notes</span><span class="sxs-lookup"><span data-stu-id="b1f18-110">Remarks</span></span>

<span data-ttu-id="b1f18-111">Si une erreur se produit dans une opération d’analyse en arrière-plan, le [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas retourner le code d’erreur, car il se produit dans un thread différent.</span><span class="sxs-lookup"><span data-stu-id="b1f18-111">If an error occurs within a background analysis operation, the [**IInkAnalyzer**](iinkanalyzer.md) cannot return the error code because it is occurring in a different thread.</span></span> <span data-ttu-id="b1f18-112">Au lieu de cela, le gestionnaire d’événements [**\_ IAnalysisEvents :: Results**](-ianalysisevents-results.md) reçoit un [**IAnalysisStatus**](ianalysisstatus.md) qui contient un [**IAnalysisWarning**](ianalysiswarning.md) avec [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) **AnalysisWarningCode \_ BackgroundException**.</span><span class="sxs-lookup"><span data-stu-id="b1f18-112">Instead, the [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event handler receives an [**IAnalysisStatus**](ianalysisstatus.md) that contains an [**IAnalysisWarning**](ianalysiswarning.md) with an [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) of **AnalysisWarningCode\_BackgroundException**.</span></span> <span data-ttu-id="b1f18-113">Ce **IAnalysisWarning** contient le code d’erreur de l’opération d’analyse en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b1f18-113">This **IAnalysisWarning** contains the error code for the background analysis operation.</span></span> <span data-ttu-id="b1f18-114">En général, votre gestionnaire d’événements **\_ IAnalysisEvents :: Results** retourne ce code d’erreur afin qu’il puisse être géré ailleurs dans votre application.</span><span class="sxs-lookup"><span data-stu-id="b1f18-114">In general, your **\_IAnalysisEvents::Results** event handler will return this error code so that it can be handled elsewhere in your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1f18-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1f18-115">Requirements</span></span>



| <span data-ttu-id="b1f18-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1f18-116">Requirement</span></span> | <span data-ttu-id="b1f18-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1f18-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f18-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f18-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1f18-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1f18-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f18-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1f18-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1f18-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1f18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f18-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1f18-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1f18-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b1f18-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f18-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1f18-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1f18-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1f18-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f18-127">**IAnalysisWarning**</span><span class="sxs-lookup"><span data-stu-id="b1f18-127">**IAnalysisWarning**</span></span>](ianalysiswarning.md)
</dt> <dt>

[<span data-ttu-id="b1f18-128">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="b1f18-128">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="b1f18-129">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="b1f18-129">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="b1f18-130">**\_IAnalysisEvents :: Results**</span><span class="sxs-lookup"><span data-stu-id="b1f18-130">**\_IAnalysisEvents::Results**</span></span>](-ianalysisevents-results.md)
</dt> <dt>

[<span data-ttu-id="b1f18-131">**AnalysisWarningCode**</span><span class="sxs-lookup"><span data-stu-id="b1f18-131">**AnalysisWarningCode**</span></span>](/windows/desktop/tablet/analysiswarningcode)
</dt> <dt>

[<span data-ttu-id="b1f18-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b1f18-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

