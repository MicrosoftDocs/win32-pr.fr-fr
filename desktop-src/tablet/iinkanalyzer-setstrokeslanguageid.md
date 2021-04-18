---
description: Modifie l’identificateur de paramètres régionaux pour les traits spécifiés.
ms.assetid: 39dd24d5-4381-4b51-8d95-7d936fd69d47
title: 'IInkAnalyzer :: SetStrokesLanguageId, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 84d2e4b9e3ac24fc73eddc4f84bcc9337cb4c372
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516267"
---
# <a name="iinkanalyzersetstrokeslanguageid-method"></a><span data-ttu-id="30c56-103">IInkAnalyzer :: SetStrokesLanguageId, méthode</span><span class="sxs-lookup"><span data-stu-id="30c56-103">IInkAnalyzer::SetStrokesLanguageId method</span></span>

<span data-ttu-id="30c56-104">Modifie l’identificateur de paramètres régionaux pour les traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="30c56-104">Changes the locale identifier for the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30c56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30c56-105">Syntax</span></span>


```C++
HRESULT SetStrokesLanguageId(
  [in] ULONG ulStrokeIdCount,
  [in] LONG  *plStrokes,
  [in] LONG  lStrokesLCID
);
```



## <a name="parameters"></a><span data-ttu-id="30c56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30c56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30c56-107">*ulStrokeIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c56-107">*ulStrokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c56-108">Nombre d’identificateurs de trait dans *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="30c56-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="30c56-109">*plStrokes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c56-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c56-110">Tableau d’identificateurs pour les traits auxquels assigner l’identificateur de paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="30c56-110">The array of identifiers for the strokes to which to assign the locale identifier.</span></span>

</dd> <dt>

<span data-ttu-id="30c56-111">*lStrokesLCID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="30c56-111">*lStrokesLCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30c56-112">Identificateur de paramètres régionaux à assigner aux traits.</span><span class="sxs-lookup"><span data-stu-id="30c56-112">The locale identifier to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30c56-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30c56-113">Return value</span></span>

<span data-ttu-id="30c56-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="30c56-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30c56-115">Notes</span><span class="sxs-lookup"><span data-stu-id="30c56-115">Remarks</span></span>

<span data-ttu-id="30c56-116">Les paramètres régionaux d’un trait sont définis lorsque vous ajoutez le trait en appelant la méthode [**IInkAnalyzer :: AddStroke**](iinkanalyzer-addstroke.md), méthode [**IInkAnalyzer :: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer :: AddStrokes**](iinkanalyzer-addstrokes.md)ou [**IInkAnalyzer :: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md).</span><span class="sxs-lookup"><span data-stu-id="30c56-116">A stroke's locale is set when you add the stroke by calling [**IInkAnalyzer::AddStroke Method**](iinkanalyzer-addstroke.md), [**IInkAnalyzer::AddStrokeForLanguage Method**](iinkanalyzer-addstrokeforlanguage.md), [**IInkAnalyzer::AddStrokes Method**](iinkanalyzer-addstrokes.md), or [**IInkAnalyzer::AddStrokesForLanguage Method**](iinkanalyzer-addstrokesforlanguage.md).</span></span> <span data-ttu-id="30c56-117">Pour obtenir les paramètres régionaux actuellement assignés à un trait, appelez la [**méthode IInkAnalyzer :: GetStrokeLanguageId**](iinkanalyzer-getstrokelanguageid.md).</span><span class="sxs-lookup"><span data-stu-id="30c56-117">To get the locale currently assigned to a stroke, call [**IInkAnalyzer::GetStrokeLanguageId Method**](iinkanalyzer-getstrokelanguageid.md).</span></span>

<span data-ttu-id="30c56-118">Les traits spécifiés sont déplacés vers un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)) qui contient des traits de la même langue.</span><span class="sxs-lookup"><span data-stu-id="30c56-118">The specified strokes are moved to an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)) that contains strokes of the same language.</span></span> <span data-ttu-id="30c56-119">S’il n’existe pas de [**IContextNode**](icontextnode.md) de ce type, cette méthode crée un nouveau nœud d’encre non classifié et y déplace les traits.</span><span class="sxs-lookup"><span data-stu-id="30c56-119">If no such [**IContextNode**](icontextnode.md) exists, this method creates a new unclassified ink node and moves the strokes to it.</span></span> <span data-ttu-id="30c56-120">Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="30c56-120">An unclassified ink node is an **IContextNode** that has a type of UnclassifiedInk.</span></span>

<span data-ttu-id="30c56-121">Si cette méthode déplace les traits d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également les zones englobantes des traits à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="30c56-121">If this method moves strokes from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the strokes' bounding boxes to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="30c56-122">Cette méthode ne déplace pas un trait si le paramètre *lStrokeLCID* correspond à l’identificateur de langue actuel du trait.</span><span class="sxs-lookup"><span data-stu-id="30c56-122">This method does not move a stroke if the *lStrokeLCID* parameter matches the stroke's current language identifier.</span></span>

<span data-ttu-id="30c56-123">Si un trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="30c56-123">If a specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="30c56-124">Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="30c56-124">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="30c56-125">Cette méthode retourne un code d’erreur lorsque strokeIds a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30c56-125">This method returns an error code when strokeIds is **NULL**.</span></span>

<span data-ttu-id="30c56-126">Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="30c56-126">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="30c56-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30c56-127">Requirements</span></span>



| <span data-ttu-id="30c56-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30c56-128">Requirement</span></span> | <span data-ttu-id="30c56-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="30c56-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30c56-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c56-130">Minimum supported client</span></span><br/> | <span data-ttu-id="30c56-131">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30c56-131">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="30c56-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c56-132">Minimum supported server</span></span><br/> | <span data-ttu-id="30c56-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30c56-133">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="30c56-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="30c56-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="30c56-135"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="30c56-135"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="30c56-136">DLL</span><span class="sxs-lookup"><span data-stu-id="30c56-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30c56-137"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30c56-137"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="30c56-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30c56-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30c56-139">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="30c56-139">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="30c56-140">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-140">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="30c56-141">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-141">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="30c56-142">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-142">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="30c56-143">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-143">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="30c56-144">**IInkAnalyzer :: GetStrokeLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-144">**IInkAnalyzer::GetStrokeLanguageId Method**</span></span>](iinkanalyzer-getstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="30c56-145">**IInkAnalyzer :: SetStrokeLanguageId, méthode**</span><span class="sxs-lookup"><span data-stu-id="30c56-145">**IInkAnalyzer::SetStrokeLanguageId Method**</span></span>](iinkanalyzer-setstrokelanguageid.md)
</dt> <dt>

[<span data-ttu-id="30c56-146">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="30c56-146">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

