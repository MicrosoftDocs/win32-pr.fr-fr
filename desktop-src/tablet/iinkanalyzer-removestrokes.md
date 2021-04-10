---
description: Supprime les traits spécifiés du IInkAnalyzer.
ms.assetid: ea7c8a9f-a427-4781-b5ba-97ffd983dbe5
title: 'IInkAnalyzer :: RemoveStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 00f065e01f9a4ff1459988d76fc9393ba24aa894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113334"
---
# <a name="iinkanalyzerremovestrokes-method"></a><span data-ttu-id="70201-103">IInkAnalyzer :: RemoveStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="70201-103">IInkAnalyzer::RemoveStrokes method</span></span>

<span data-ttu-id="70201-104">Supprime les traits spécifiés du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="70201-104">Removes the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70201-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70201-105">Syntax</span></span>


```C++
HRESULT RemoveStrokes(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="70201-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70201-107">*ulStrokeIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70201-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70201-108">Nombre d’identificateurs de trait dans *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="70201-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="70201-109">*plStrokes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="70201-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70201-110">Identificateurs des traits à supprimer.</span><span class="sxs-lookup"><span data-stu-id="70201-110">The identifiers for the strokes to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70201-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70201-111">Return value</span></span>

<span data-ttu-id="70201-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="70201-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70201-113">Notes</span><span class="sxs-lookup"><span data-stu-id="70201-113">Remarks</span></span>

<span data-ttu-id="70201-114">Cette méthode supprime les données de paquet pour et les références aux traits spécifiés à partir du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="70201-114">This method removes the packet data for and references to the specified strokes from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="70201-115">Cette méthode supprime les traits du nœud de contexte feuille qui référence les traits.</span><span class="sxs-lookup"><span data-stu-id="70201-115">This method removes the strokes from the leaf context node that references the strokes.</span></span> <span data-ttu-id="70201-116">Si un [**IContextNode**](icontextnode.md) ne fait plus référence à aucun trait, cette méthode supprime le **IContextNode** et tout objet **IContextNode** ancêtre qui n’a plus de nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="70201-116">If any [**IContextNode**](icontextnode.md) no longer references any strokes, this method deletes the **IContextNode** and any ancestor **IContextNode** objects that no longer have any child nodes.</span></span>

<span data-ttu-id="70201-117">Une fois que cette méthode a supprimé les traits du [**IContextNode**](icontextnode.md), elle met à jour la région de modification de l’objet [**IInkAnalyzer**](iinkanalyzer.md) (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)) pour inclure le cadre englobant des traits supprimés.</span><span class="sxs-lookup"><span data-stu-id="70201-117">After this method removes the strokes from the [**IContextNode**](icontextnode.md), it updates the [**IInkAnalyzer**](iinkanalyzer.md) object's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)) to include the bounding box of the removed strokes.</span></span>

<span data-ttu-id="70201-118">Si un trait identifié dans *plStrokes* n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="70201-118">If a stroke identified in *plStrokes* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="70201-119">Si aucun des traits identifiés dans *plStrokes* n’est associé à l’analyseur d’encre, cette méthode retourne sans mettre à jour la [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="70201-119">If none of the strokes identified in *plStrokes* are associated with the ink analyzer, this method returns without updating the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="70201-120">Cette méthode retourne le code d’erreur et lorsque *plStrokes* a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="70201-120">This method returns and error code when *plStrokes* is null.</span></span>

## <a name="requirements"></a><span data-ttu-id="70201-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70201-121">Requirements</span></span>



| <span data-ttu-id="70201-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70201-122">Requirement</span></span> | <span data-ttu-id="70201-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="70201-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70201-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70201-124">Minimum supported client</span></span><br/> | <span data-ttu-id="70201-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70201-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="70201-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70201-126">Minimum supported server</span></span><br/> | <span data-ttu-id="70201-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="70201-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="70201-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="70201-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="70201-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="70201-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="70201-130">DLL</span><span class="sxs-lookup"><span data-stu-id="70201-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70201-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70201-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="70201-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70201-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70201-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="70201-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="70201-134">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-134">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="70201-135">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-135">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="70201-136">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-136">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="70201-137">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-137">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="70201-138">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="70201-139">**IInkAnalyzer :: GetDirtyRegion, méthode**</span><span class="sxs-lookup"><span data-stu-id="70201-139">**IInkAnalyzer::GetDirtyRegion Method**</span></span>](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[<span data-ttu-id="70201-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="70201-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




