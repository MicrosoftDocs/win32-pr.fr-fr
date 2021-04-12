---
description: Modifie l’identificateur de paramètres régionaux pour le trait spécifié.
ms.assetid: 3714462d-0391-481f-968a-3c121b7dd538
title: 'IInkAnalyzer :: SetStrokeLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e103683d85ff971a8f0daff2574e97672dd5a84b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526475"
---
# <a name="iinkanalyzersetstrokelanguageid-method"></a><span data-ttu-id="e40ac-103">IInkAnalyzer :: SetStrokeLanguageId, méthode</span><span class="sxs-lookup"><span data-stu-id="e40ac-103">IInkAnalyzer::SetStrokeLanguageId method</span></span>

<span data-ttu-id="e40ac-104">Modifie l’identificateur de paramètres régionaux pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="e40ac-104">Changes the locale identifier for the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="e40ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e40ac-105">Syntax</span></span>


```C++
HRESULT SetStrokeLanguageId(
  [in] LONG lStrokeId,
  [in] LONG lStrokeLCID
);
```



## <a name="parameters"></a><span data-ttu-id="e40ac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e40ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e40ac-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e40ac-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40ac-108">Identificateur du trait auquel assigner l’identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="e40ac-108">The identifier of the stroke to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="e40ac-109">*lStrokeLCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e40ac-109">*lStrokeLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e40ac-110">Identificateur de paramètres régionaux à assigner au trait.</span><span class="sxs-lookup"><span data-stu-id="e40ac-110">The locale identifier to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e40ac-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e40ac-111">Return value</span></span>

<span data-ttu-id="e40ac-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="e40ac-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e40ac-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e40ac-113">Remarks</span></span>

<span data-ttu-id="e40ac-114">Les paramètres régionaux d’un trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="e40ac-114">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="e40ac-115">Pour obtenir les paramètres régionaux actuellement assignés à un trait, appelez la [**méthode IInkAnalyzer :: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="e40ac-115">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="e40ac-116">Le trait spécifié est déplacé vers un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)) qui contient des traits de la même langue.</span><span class="sxs-lookup"><span data-stu-id="e40ac-116">The specified stroke is moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="e40ac-117">S’il n’existe pas de [**IContextNode**](icontextnode.md) de ce type, cette méthode crée un nouveau nœud d’encre non classifié et y déplace le trait.</span><span class="sxs-lookup"><span data-stu-id="e40ac-117">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the stroke to it.</span></span> <span data-ttu-id="e40ac-118">Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="e40ac-118">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="e40ac-119">Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="e40ac-119">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="e40ac-120">Cette méthode ne déplace pas un trait si le paramètre *lStrokeLCID* correspond à l’identificateur de langue actuel du trait.</span><span class="sxs-lookup"><span data-stu-id="e40ac-120">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="e40ac-121">Si le trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="e40ac-121">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="e40ac-122">Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="e40ac-122">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="e40ac-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e40ac-123">Requirements</span></span>



| <span data-ttu-id="e40ac-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e40ac-124">Requirement</span></span> | <span data-ttu-id="e40ac-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e40ac-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e40ac-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e40ac-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e40ac-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e40ac-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e40ac-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e40ac-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e40ac-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e40ac-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="e40ac-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="e40ac-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e40ac-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e40ac-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e40ac-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e40ac-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e40ac-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e40ac-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="e40ac-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e40ac-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e40ac-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="e40ac-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="e40ac-136">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-136">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="e40ac-137">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-137">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="e40ac-138">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-138">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="e40ac-139">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-139">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="e40ac-140">**IInkAnalyzer :: GetStrokeLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-140">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="e40ac-141">**IInkAnalyzer :: SetStrokesLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="e40ac-141">**IInkAnalyzer::SetStrokesLanguageId Method**</span></span>](iinkanalyzer-setstrokeslanguageid.md)
</dt> <dt>

[<span data-ttu-id="e40ac-142">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="e40ac-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

