---
description: Met à jour les données du paquet pour les traits spécifiés.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'IInkAnalyzer :: UpdateStrokesData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514629"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a><span data-ttu-id="c6968-103">IInkAnalyzer :: UpdateStrokesData, méthode</span><span class="sxs-lookup"><span data-stu-id="c6968-103">IInkAnalyzer::UpdateStrokesData method</span></span>

<span data-ttu-id="c6968-104">Met à jour les données du paquet pour les traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="c6968-104">Updates the packet data for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6968-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6968-105">Syntax</span></span>


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c6968-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c6968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6968-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-108">Nombre de traits à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c6968-108">The number of strokes to update.</span></span>

</dd> <dt>

<span data-ttu-id="c6968-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-110">Tableau contenant les identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="c6968-110">An array containing the stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="c6968-111">*ulStrokePacketDescriptionCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-111">*ulStrokePacketDescriptionCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-112">Nombre de propriétés dans chaque paquet.</span><span class="sxs-lookup"><span data-stu-id="c6968-112">The number of properties in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="c6968-113">*pStrokePacketDescriptionGuids* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-113">*pStrokePacketDescriptionGuids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-114">Tableau contenant les identificateurs de propriété de paquet.</span><span class="sxs-lookup"><span data-stu-id="c6968-114">An array containing the packet property identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="c6968-115">*pulPacketDataCountPerStroke* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-115">*pulPacketDataCountPerStroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-116">Tableau contenant le nombre de paquets dans chaque trait.</span><span class="sxs-lookup"><span data-stu-id="c6968-116">An array containing the number of packets in each stroke.</span></span>

</dd> <dt>

<span data-ttu-id="c6968-117">*plStrokePacketData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c6968-117">*plStrokePacketData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6968-118">Tableau contenant les données du paquet pour les traits.</span><span class="sxs-lookup"><span data-stu-id="c6968-118">An array containing the packet data for the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6968-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c6968-119">Return value</span></span>

<span data-ttu-id="c6968-120">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c6968-120">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c6968-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c6968-121">Remarks</span></span>

<span data-ttu-id="c6968-122">le paramètre *plStrokePacketData* contient des données de paquet pour tous les traits.</span><span class="sxs-lookup"><span data-stu-id="c6968-122">the *plStrokePacketData* parameter contains packet data for all of the strokes.</span></span> <span data-ttu-id="c6968-123">Le paramètre *pStrokePacketDescriptionGuids* contient les identificateurs globaux uniques (Guid) qui décrivent les types de données de paquets inclus pour chaque point de chaque trait.</span><span class="sxs-lookup"><span data-stu-id="c6968-123">The *pStrokePacketDescriptionGuids* parameter contains the globally unique identifiers (GUIDs) that describe the types of packet data included for each point in each stroke.</span></span> <span data-ttu-id="c6968-124">Pour obtenir la liste complète des propriétés de paquet disponibles, consultez [constantes PacketPropertyGuids](packetpropertyguids-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c6968-124">For a complete list of available packet properties, see [PacketPropertyGuids Constants](packetpropertyguids-constants.md).</span></span>

<span data-ttu-id="c6968-125">Seuls les traits avec les mêmes descriptions de paquets peuvent être mis à jour dans un seul appel à la **méthode IInkAnalyzer :: UpdateStrokesData**.</span><span class="sxs-lookup"><span data-stu-id="c6968-125">Only strokes with the same packet descriptions can be updated in a single call to **IInkAnalyzer::UpdateStrokesData Method**.</span></span>

<span data-ttu-id="c6968-126">Cette méthode ne met pas à jour la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="c6968-126">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="c6968-127">Si un trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="c6968-127">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="c6968-128">Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="c6968-128">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="c6968-129">Cette méthode retourne un code d’erreur lorsque *plStrokeIds* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c6968-129">This method returns an error code when *plStrokeIds* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6968-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6968-130">Requirements</span></span>



| <span data-ttu-id="c6968-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6968-131">Requirement</span></span> | <span data-ttu-id="c6968-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6968-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6968-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6968-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c6968-134">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6968-134">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c6968-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6968-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c6968-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6968-136">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c6968-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6968-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6968-138"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c6968-138"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c6968-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c6968-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6968-140"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6968-140"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c6968-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6968-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6968-142">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c6968-142">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c6968-143">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-143">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="c6968-144">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-144">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c6968-145">**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-145">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c6968-146">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-146">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="c6968-147">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-147">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="c6968-148">**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-148">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c6968-149">**IInkAnalyzer :: ClearStrokeData, méthode**</span><span class="sxs-lookup"><span data-stu-id="c6968-149">**IInkAnalyzer::ClearStrokeData Method**</span></span>](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[<span data-ttu-id="c6968-150">**\_IAnalysisEvents::UpdateStrokesCache**</span><span class="sxs-lookup"><span data-stu-id="c6968-150">**\_IAnalysisEvents::UpdateStrokesCache**</span></span>](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[<span data-ttu-id="c6968-151">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="c6968-151">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




