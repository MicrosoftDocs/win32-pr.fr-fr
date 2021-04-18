---
description: Modifie le type des traits spécifiés.
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'IInkAnalyzer :: SetStrokesType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543087"
---
# <a name="iinkanalyzersetstrokestype-method"></a><span data-ttu-id="da76a-103">IInkAnalyzer :: SetStrokesType, méthode</span><span class="sxs-lookup"><span data-stu-id="da76a-103">IInkAnalyzer::SetStrokesType method</span></span>

<span data-ttu-id="da76a-104">Modifie le type des traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="da76a-104">Changes the type of the specified strokes.</span></span>

## <a name="syntax"></a><span data-ttu-id="da76a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da76a-105">Syntax</span></span>


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="da76a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="da76a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da76a-107">*strokeIdCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da76a-107">*strokeIdCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da76a-108">Nombre d’identificateurs de trait dans *plStrokes*.</span><span class="sxs-lookup"><span data-stu-id="da76a-108">The number of stroke identifiers in *plStrokes*.</span></span>

</dd> <dt>

<span data-ttu-id="da76a-109">*plStrokes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da76a-109">*plStrokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da76a-110">Tableau contenant les identificateurs de trait des traits auxquels assigner *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="da76a-110">An array containing the stroke identifiers of the strokes to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="da76a-111">*StrokeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="da76a-111">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da76a-112">Valeur [**StrokeType**](stroketype.md) à assigner aux traits.</span><span class="sxs-lookup"><span data-stu-id="da76a-112">The [**StrokeType**](stroketype.md) value to assign to the strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da76a-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="da76a-113">Return value</span></span>

<span data-ttu-id="da76a-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="da76a-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da76a-115">Notes</span><span class="sxs-lookup"><span data-stu-id="da76a-115">Remarks</span></span>

<span data-ttu-id="da76a-116">Si le type du trait est la [](stroketype.md) valeur StrokeType **StrokeType non \_ classifiée**, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="da76a-116">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="da76a-117">Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.</span><span class="sxs-lookup"><span data-stu-id="da76a-117">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="da76a-118">[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="da76a-118">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="da76a-119">Pour spécifier ou modifier le type de trait, utilisez la méthode [**IInkAnalyzer :: SetStrokeType**](iinkanalyzer-setstroketype.md) ou **IInkAnalyzer :: SetStrokesType**.</span><span class="sxs-lookup"><span data-stu-id="da76a-119">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or **IInkAnalyzer::SetStrokesType Method**.</span></span>

<span data-ttu-id="da76a-120">Si un trait est associé à un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)), cette méthode déplace le trait vers un nœud d’encre non classifié qui contient des traits du même langage.</span><span class="sxs-lookup"><span data-stu-id="da76a-120">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="da76a-121">Si ce nœud de contexte n’existe pas, cette méthode crée un nouveau nœud d’encre non classifié et lui ajoute le trait.</span><span class="sxs-lookup"><span data-stu-id="da76a-121">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="da76a-122">Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="da76a-122">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="da76a-123">Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="da76a-123">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="da76a-124">Cette méthode ne déplace pas un trait si le paramètre *StrokeType* correspond au type actuel du trait.</span><span class="sxs-lookup"><span data-stu-id="da76a-124">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="da76a-125">Si un trait identifié dans *strokeIds* n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode ignore l’identificateur.</span><span class="sxs-lookup"><span data-stu-id="da76a-125">If a stroke identified in *strokeIds* is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method ignores the identifier.</span></span>

<span data-ttu-id="da76a-126">Si aucun des traits spécifiés n’identifie un trait associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="da76a-126">If none of the specified strokes identify a stroke associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

<span data-ttu-id="da76a-127">La définition du type de trait sur les traits associés à un ContextNode qui a NodeTypeAndProperties Confirm lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="da76a-127">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="da76a-128">Cette méthode retourne un code d’erreur lorsque *plStrokes* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="da76a-128">This method returns an error code when *plStrokes* is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="da76a-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da76a-129">Requirements</span></span>



| <span data-ttu-id="da76a-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da76a-130">Requirement</span></span> | <span data-ttu-id="da76a-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="da76a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da76a-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da76a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="da76a-133">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da76a-133">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da76a-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da76a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="da76a-135">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="da76a-135">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="da76a-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="da76a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="da76a-137"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="da76a-137"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="da76a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="da76a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da76a-139"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da76a-139"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="da76a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da76a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da76a-141">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="da76a-141">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="da76a-142">**IInkAnalyzer :: GetStrokeType, méthode**</span><span class="sxs-lookup"><span data-stu-id="da76a-142">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="da76a-143">**IInkAnalyzer :: SetStrokeType, méthode**</span><span class="sxs-lookup"><span data-stu-id="da76a-143">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="da76a-144">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="da76a-144">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




