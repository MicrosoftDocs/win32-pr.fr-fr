---
description: Spécifie la manière dont le IInkAnalyzer effectue l’analyse de l’encre.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Énumération AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393239"
---
# <a name="analysismodes-enumeration"></a><span data-ttu-id="7bc82-103">Énumération AnalysisModes</span><span class="sxs-lookup"><span data-stu-id="7bc82-103">AnalysisModes enumeration</span></span>

<span data-ttu-id="7bc82-104">Spécifie la manière dont le [**IInkAnalyzer**](iinkanalyzer.md) effectue l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="7bc82-104">Specifies how the [**IInkAnalyzer**](iinkanalyzer.md) performs ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bc82-105">Syntax</span></span>


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a><span data-ttu-id="7bc82-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="7bc82-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7bc82-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="7bc82-107"><span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes\_None**</span></span>
</dt> <dd>

<span data-ttu-id="7bc82-108">Aucun mode n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="7bc82-108">No modes are specified.</span></span>

</dd> <dt>

<span data-ttu-id="7bc82-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**</span><span class="sxs-lookup"><span data-stu-id="7bc82-109"><span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes\_AutomaticReconciliation**</span></span>
</dt> <dd>

<span data-ttu-id="7bc82-110">Indique si le [**IInkAnalyzer**](iinkanalyzer.md) démarre automatiquement l’opération de rapprochement dès que les résultats intermédiaires ou finaux sont prêts.</span><span class="sxs-lookup"><span data-stu-id="7bc82-110">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically starts the reconciliation operation as soon as the intermediate or final results are ready.</span></span>

<span data-ttu-id="7bc82-111">Si ce mode est activé, l’événement [**\_ IAnalysisEvents :: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) n’est pas déclenché.</span><span class="sxs-lookup"><span data-stu-id="7bc82-111">If this mode is enabled, the [**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) event is not raised.</span></span> <span data-ttu-id="7bc82-112">Si ce mode est désactivé, l’événement **\_ IAnalysisEvents :: ReadyToReconcile** est déclenché.</span><span class="sxs-lookup"><span data-stu-id="7bc82-112">If this mode is disabled, the **\_IAnalysisEvents::ReadyToReconcile** event is raised.</span></span>

</dd> <dt>

<span data-ttu-id="7bc82-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**</span><span class="sxs-lookup"><span data-stu-id="7bc82-113"><span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes\_StrokeCacheAutoCleanup**</span></span>
</dt> <dd>

<span data-ttu-id="7bc82-114">Indique si le [**IInkAnalyzer**](iinkanalyzer.md) efface automatiquement les traits inutiles du cache de trait avant d’effectuer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7bc82-114">Whether the [**IInkAnalyzer**](iinkanalyzer.md) automatically clears unneeded strokes from the stroke cache before performing analysis.</span></span>

<span data-ttu-id="7bc82-115">Si ce mode est activé, le [**IInkAnalyzer**](iinkanalyzer.md) efface les données de trait avant d’effectuer l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7bc82-115">If this mode is enabled, the [**IInkAnalyzer**](iinkanalyzer.md) clears the stroke data before performing analysis.</span></span> <span data-ttu-id="7bc82-116">Votre code doit également gérer l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) .</span><span class="sxs-lookup"><span data-stu-id="7bc82-116">Your code must also then handle the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event.</span></span> <span data-ttu-id="7bc82-117">Si l’événement **\_ IAnalysisEvents :: UpdateStrokesCache** n’est pas géré, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="7bc82-117">If the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span> <span data-ttu-id="7bc82-118">Cette vérification s’effectue à la fois au niveau des phases Analyze (ou BackgroundAnalyze) et de la réconciliation.</span><span class="sxs-lookup"><span data-stu-id="7bc82-118">This check is done both at the Analyze (or BackgroundAnalyze) and Reconciliation phases.</span></span>

<span data-ttu-id="7bc82-119">Si ce mode est désactivé, [**IInkAnalyzer**](iinkanalyzer.md) n’efface pas les données du trait.</span><span class="sxs-lookup"><span data-stu-id="7bc82-119">If this mode is disabled, the [**IInkAnalyzer**](iinkanalyzer.md) does not clear the stroke data.</span></span> <span data-ttu-id="7bc82-120">Pour effacer les données de trait, appelez la [**méthode IInkAnalyzer :: ClearStrokeData**](iinkanalyzer-clearstrokedata.md).</span><span class="sxs-lookup"><span data-stu-id="7bc82-120">To clear the stroke data, call [**IInkAnalyzer::ClearStrokeData Method**](iinkanalyzer-clearstrokedata.md).</span></span> <span data-ttu-id="7bc82-121">Si ce mode est désactivé, l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) est déclenché afin que le **IInkAnalyzer** puisse récupérer les données de trait les plus récentes pour tous les traits dont le cache a été effacé.</span><span class="sxs-lookup"><span data-stu-id="7bc82-121">If this mode is disabled, the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event is raised so the **IInkAnalyzer** can retrieve the latest stroke data for any strokes that have had their cache cleared.</span></span> <span data-ttu-id="7bc82-122">Si le cache de trait est effacé, mais que l’événement **\_ IAnalysisEvents :: UpdateStrokesCache** n’est pas géré, une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="7bc82-122">If the stroke cache is cleared, but the **\_IAnalysisEvents::UpdateStrokesCache** event is not handled, an exception is raised.</span></span>

</dd> <dt>

<span data-ttu-id="7bc82-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**</span><span class="sxs-lookup"><span data-stu-id="7bc82-123"><span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes\_PersonalizationEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="7bc82-124">La personnalisation de la reconnaissance de l’écriture manuscrite est activée.</span><span class="sxs-lookup"><span data-stu-id="7bc82-124">Personalization of handwriting recognition is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7bc82-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="7bc82-125"><span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes\_Default**</span></span>
</dt> <dd>

<span data-ttu-id="7bc82-126">Tous les modes sont activés.</span><span class="sxs-lookup"><span data-stu-id="7bc82-126">All modes are enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bc82-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7bc82-127">Remarks</span></span>

<span data-ttu-id="7bc82-128">Cette énumération permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="7bc82-128">This enumeration allows a bitwise combination of its member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc82-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bc82-129">Requirements</span></span>



| <span data-ttu-id="7bc82-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bc82-130">Requirement</span></span> | <span data-ttu-id="7bc82-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bc82-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bc82-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc82-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7bc82-133">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bc82-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7bc82-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc82-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7bc82-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bc82-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7bc82-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bc82-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bc82-137"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7bc82-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bc82-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bc82-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc82-139">**IInkAnalyzer :: GetAnalysisModes, méthode**</span><span class="sxs-lookup"><span data-stu-id="7bc82-139">**IInkAnalyzer::GetAnalysisModes Method**</span></span>](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7bc82-140">**IInkAnalyzer :: SetAnalysisModes, méthode**</span><span class="sxs-lookup"><span data-stu-id="7bc82-140">**IInkAnalyzer::SetAnalysisModes Method**</span></span>](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[<span data-ttu-id="7bc82-141">**\_IAnalysisEvents::IntermediateResults**</span><span class="sxs-lookup"><span data-stu-id="7bc82-141">**\_IAnalysisEvents::IntermediateResults**</span></span>](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[<span data-ttu-id="7bc82-142">**\_IAnalysisEvents::ReadyToReconcile**</span><span class="sxs-lookup"><span data-stu-id="7bc82-142">**\_IAnalysisEvents::ReadyToReconcile**</span></span>](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[<span data-ttu-id="7bc82-143">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="7bc82-143">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="7bc82-144">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="7bc82-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




