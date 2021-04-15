---
description: Efface les données de paquets de trait du IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'IInkAnalyzer :: ClearStrokeData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485081"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="b13f1-103">IInkAnalyzer :: ClearStrokeData, méthode</span><span class="sxs-lookup"><span data-stu-id="b13f1-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="b13f1-104">Efface les données de paquets de trait du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="b13f1-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b13f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b13f1-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="b13f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b13f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b13f1-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b13f1-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b13f1-108">Identificateur du trait pour lequel les données du paquet sont effacées.</span><span class="sxs-lookup"><span data-stu-id="b13f1-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b13f1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b13f1-109">Return value</span></span>

<span data-ttu-id="b13f1-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="b13f1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b13f1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="b13f1-111">Remarks</span></span>

<span data-ttu-id="b13f1-112">Utilisez cette méthode lorsque les données de paquet d’un trait sont modifiées, par exemple lorsqu’un trait est déplacé ou transformé autrement.</span><span class="sxs-lookup"><span data-stu-id="b13f1-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="b13f1-113">[**IInkAnalyzer**](iinkanalyzer.md) déclenche l’événement [**\_ IAnalysisEvents :: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) lorsqu’il a besoin de tracer des données de paquets à partir d’un trait pour lequel les données du paquet ont été effacées.</span><span class="sxs-lookup"><span data-stu-id="b13f1-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="b13f1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b13f1-114">Requirements</span></span>



| <span data-ttu-id="b13f1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b13f1-115">Requirement</span></span> | <span data-ttu-id="b13f1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b13f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b13f1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b13f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b13f1-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b13f1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b13f1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b13f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b13f1-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b13f1-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b13f1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b13f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b13f1-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b13f1-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b13f1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b13f1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b13f1-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b13f1-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b13f1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b13f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b13f1-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b13f1-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="b13f1-127">**IInkAnalyzer :: UpdateStrokesData, méthode**</span><span class="sxs-lookup"><span data-stu-id="b13f1-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="b13f1-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="b13f1-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




