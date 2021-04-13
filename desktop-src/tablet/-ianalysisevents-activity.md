---
description: 'Se produit lorsque la méthode IInkAnalyzer :: Analyze ou IInkAnalyzer :: BackgroundAnalyze est appelée.'
ms.assetid: 339b41c6-f388-4b81-b2bc-3705b39d9cc9
title: '_IAnalysisEvents :: Activity, événement (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Activity
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f235d3414b0d514f32b4ebd197c04a8721968a2a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321702"
---
# <a name="_ianalysiseventsactivity-event"></a><span data-ttu-id="eeb98-103">\_Événement IAnalysisEvents :: Activity</span><span class="sxs-lookup"><span data-stu-id="eeb98-103">\_IAnalysisEvents::Activity event</span></span>

<span data-ttu-id="eeb98-104">Se produit lorsque la méthode [**IInkAnalyzer :: Analyze**](iinkanalyzer-analyze.md) ou [**IInkAnalyzer :: BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) est appelée.</span><span class="sxs-lookup"><span data-stu-id="eeb98-104">Occurs when the [**IInkAnalyzer::Analyze**](iinkanalyzer-analyze.md) method or [**IInkAnalyzer::BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeb98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eeb98-105">Syntax</span></span>


```C++
HRESULT Activity();
```



## <a name="parameters"></a><span data-ttu-id="eeb98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eeb98-106">Parameters</span></span>

<span data-ttu-id="eeb98-107">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eeb98-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eeb98-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eeb98-108">Return value</span></span>

<span data-ttu-id="eeb98-109">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-109">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eeb98-110">Notes</span><span class="sxs-lookup"><span data-stu-id="eeb98-110">Remarks</span></span>

<span data-ttu-id="eeb98-111">Cet événement indique que le [**IInkAnalyzer**](iinkanalyzer.md) effectue une analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-111">This event indicates that the [**IInkAnalyzer**](iinkanalyzer.md) is performing ink analysis.</span></span> <span data-ttu-id="eeb98-112">Cet événement n’indique pas la progression de l’opération d’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-112">This event does not indicate the progress of the ink analysis operation.</span></span>

<span data-ttu-id="eeb98-113">Pour effectuer l’une des opérations suivantes, implémentez un gestionnaire d’événements **\_ IAnalysisEvents :: Activity** :</span><span class="sxs-lookup"><span data-stu-id="eeb98-113">To do any of the following, implement an **\_IAnalysisEvents::Activity** event handler:</span></span>

-   <span data-ttu-id="eeb98-114">Indiquer à l’utilisateur que l’analyseur d’encre effectue une analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-114">Indicate to the user that the ink analyzer is performing ink analysis.</span></span>
-   <span data-ttu-id="eeb98-115">Traiter l’entrée d’utilisateur pendant l’analyse synchrone.</span><span class="sxs-lookup"><span data-stu-id="eeb98-115">Process user input during synchronous analysis.</span></span>
-   <span data-ttu-id="eeb98-116">Recevoir des notifications de requêtes système, telles que le redessin de la fenêtre de l’application, pendant l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-116">Receive notification of system requests, such as repainting of the application's window, during ink analysis.</span></span>

<span data-ttu-id="eeb98-117">Le [**IInkAnalyzer**](iinkanalyzer.md) déclenche cet événement fréquemment pendant la phase d’analyse de la disposition et la phase de classification de l’écriture et du dessin de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-117">The [**IInkAnalyzer**](iinkanalyzer.md) raises this event frequently during the layout analysis phase and the writing and drawing classification phase of ink analysis.</span></span> <span data-ttu-id="eeb98-118">Le **IInkAnalyzer** déclenche cet événement lors de la phase de reconnaissance de l’écriture manuscrite avant et après l’accès à un module de reconnaissance d’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-118">The **IInkAnalyzer** raises this event during the handwriting recognition phase before and after accessing an ink recognizer.</span></span>

<span data-ttu-id="eeb98-119">Le nombre d’événements d’activité générés par un [**IInkAnalyzer**](iinkanalyzer.md) est affecté par :</span><span class="sxs-lookup"><span data-stu-id="eeb98-119">The number of activity events an [**IInkAnalyzer**](iinkanalyzer.md) generates is affected by:</span></span>

-   <span data-ttu-id="eeb98-120">Module de reconnaissance de l’encre que le [**IInkAnalyzer**](iinkanalyzer.md) applique à la reconnaissance de l’encre.</span><span class="sxs-lookup"><span data-stu-id="eeb98-120">The ink recognizer that the [**IInkAnalyzer**](iinkanalyzer.md) applies to ink recognition.</span></span>
-   <span data-ttu-id="eeb98-121">Nombre et longueur des traits analysés par le [**IInkAnalyzer**](iinkanalyzer.md) .</span><span class="sxs-lookup"><span data-stu-id="eeb98-121">The number and length of strokes that the [**IInkAnalyzer**](iinkanalyzer.md) is analyzing.</span></span>
-   <span data-ttu-id="eeb98-122">Nombre de traits classés comme écrits.</span><span class="sxs-lookup"><span data-stu-id="eeb98-122">The number of strokes that are classified as writing.</span></span>

<span data-ttu-id="eeb98-123">Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="eeb98-123">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeb98-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeb98-124">Requirements</span></span>



| <span data-ttu-id="eeb98-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeb98-125">Requirement</span></span> | <span data-ttu-id="eeb98-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeb98-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeb98-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb98-127">Minimum supported client</span></span><br/> | <span data-ttu-id="eeb98-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eeb98-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="eeb98-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb98-129">Minimum supported server</span></span><br/> | <span data-ttu-id="eeb98-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="eeb98-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="eeb98-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeb98-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeb98-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="eeb98-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="eeb98-133">DLL</span><span class="sxs-lookup"><span data-stu-id="eeb98-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeb98-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeb98-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="eeb98-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeb98-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeb98-136">**\_IAnalysisEvents**</span><span class="sxs-lookup"><span data-stu-id="eeb98-136">**\_IAnalysisEvents**</span></span>](-ianalysisevents.md)
</dt> <dt>

[<span data-ttu-id="eeb98-137">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="eeb98-137">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="eeb98-138">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="eeb98-138">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="eeb98-139">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="eeb98-139">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="eeb98-140">**IInkAnalyzer :: Analyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="eeb98-140">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="eeb98-141">**IInkAnalyzer :: BackgroundAnalyze, méthode**</span><span class="sxs-lookup"><span data-stu-id="eeb98-141">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="eeb98-142">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="eeb98-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




