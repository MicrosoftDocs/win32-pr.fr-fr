---
description: Supprime le trait spécifié du IInkAnalyzer.
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'IInkAnalyzer :: RemoveStroke, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 03952e6e14679c53f7b65f21463fc0457f302b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526487"
---
# <a name="iinkanalyzerremovestroke-method"></a><span data-ttu-id="59fc3-103">IInkAnalyzer :: RemoveStroke, méthode</span><span class="sxs-lookup"><span data-stu-id="59fc3-103">IInkAnalyzer::RemoveStroke method</span></span>

<span data-ttu-id="59fc3-104">Supprime le trait spécifié du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="59fc3-104">Removes the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="59fc3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59fc3-105">Syntax</span></span>


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="59fc3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59fc3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fc3-107">*plStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fc3-107">*plStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fc3-108">Identificateur du trait.</span><span class="sxs-lookup"><span data-stu-id="59fc3-108">The stroke identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fc3-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59fc3-109">Return value</span></span>

<span data-ttu-id="59fc3-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="59fc3-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59fc3-111">Notes</span><span class="sxs-lookup"><span data-stu-id="59fc3-111">Remarks</span></span>

<span data-ttu-id="59fc3-112">Cette méthode supprime les données de paquet pour, et les références à, le trait spécifié à partir du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="59fc3-112">This method removes the packet data for, and references to, the specified stroke from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="59fc3-113">Cette méthode supprime le trait du nœud de contexte feuille qui référence le trait.</span><span class="sxs-lookup"><span data-stu-id="59fc3-113">This method removes the stroke from the leaf context node that references the stroke.</span></span> <span data-ttu-id="59fc3-114">Si le [**IContextNode**](icontextnode.md) ne fait plus référence à aucun trait, cette méthode supprime le **IContextNode** et tout objet **IContextNode** ancêtre qui n’a plus de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="59fc3-114">If the [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="59fc3-115">Une fois que cette méthode a supprimé le trait du [**IContextNode**](icontextnode.md), il met à jour la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) pour inclure le cadre englobant du trait supprimé.</span><span class="sxs-lookup"><span data-stu-id="59fc3-115">After this method removes the stroke from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed stroke.</span></span>

<span data-ttu-id="59fc3-116">Si *plStrokeId* n’identifie pas un trait associé au [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour l’analyseur d’encre.</span><span class="sxs-lookup"><span data-stu-id="59fc3-116">If *plStrokeId* does not identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the ink analyzer.</span></span>

## <a name="requirements"></a><span data-ttu-id="59fc3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59fc3-117">Requirements</span></span>



| <span data-ttu-id="59fc3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59fc3-118">Requirement</span></span> | <span data-ttu-id="59fc3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fc3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59fc3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59fc3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="59fc3-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59fc3-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="59fc3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59fc3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="59fc3-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="59fc3-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="59fc3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="59fc3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="59fc3-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="59fc3-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="59fc3-126">DLL</span><span class="sxs-lookup"><span data-stu-id="59fc3-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59fc3-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59fc3-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="59fc3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59fc3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fc3-129">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="59fc3-129">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="59fc3-130">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-130">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="59fc3-131">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-131">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="59fc3-132">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-132">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="59fc3-133">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-133">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="59fc3-134">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-134">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="59fc3-135">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="59fc3-135">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="59fc3-136">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="59fc3-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




