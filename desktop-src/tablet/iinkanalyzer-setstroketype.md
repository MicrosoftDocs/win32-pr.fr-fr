---
description: Modifie le type du trait spécifié.
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer :: SetStrokeType, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113319"
---
# <a name="iinkanalyzersetstroketype-method"></a><span data-ttu-id="44a73-103">IInkAnalyzer :: SetStrokeType, méthode</span><span class="sxs-lookup"><span data-stu-id="44a73-103">IInkAnalyzer::SetStrokeType method</span></span>

<span data-ttu-id="44a73-104">Modifie le type du trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="44a73-104">Changes the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44a73-105">Syntax</span></span>


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="44a73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="44a73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44a73-107">*lStrokeId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44a73-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44a73-108">Identificateur de trait du trait auquel assigner *StrokeType*.</span><span class="sxs-lookup"><span data-stu-id="44a73-108">The stroke identifier of the stroke to which to assign *StrokeType*.</span></span>

</dd> <dt>

<span data-ttu-id="44a73-109">*StrokeType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="44a73-109">*StrokeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44a73-110">Valeur [**StrokeType**](stroketype.md) à assigner au trait.</span><span class="sxs-lookup"><span data-stu-id="44a73-110">The [**StrokeType**](stroketype.md) value to assign to the stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44a73-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="44a73-111">Return value</span></span>

<span data-ttu-id="44a73-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="44a73-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="44a73-113">Notes</span><span class="sxs-lookup"><span data-stu-id="44a73-113">Remarks</span></span>

<span data-ttu-id="44a73-114">Si le type du trait est la [](stroketype.md) valeur StrokeType **StrokeType non \_ classifiée**, le [**IInkAnalyzer**](iinkanalyzer.md) classe le trait pendant l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="44a73-114">If the stroke's type is the [**StrokeType**](stroketype.md) value **StrokeType\_Unclassified**, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="44a73-115">Dans le cas contraire, le **IInkAnalyzer** utilise le type défini sur le trait.</span><span class="sxs-lookup"><span data-stu-id="44a73-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="44a73-116">[**IInkAnalyzer**](iinkanalyzer.md) ne définit pas la valeur de type de trait dans le cadre de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="44a73-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="44a73-117">Pour spécifier ou modifier le type de trait, utilisez la méthode **IInkAnalyzer :: SetStrokeType** ou [**IInkAnalyzer :: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="44a73-117">To specify or change the stroke type, use **IInkAnalyzer::SetStrokeType Method** or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

<span data-ttu-id="44a73-118">Si un trait est associé à un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)), cette méthode déplace le trait vers un nœud d’encre non classifié qui contient des traits du même langage.</span><span class="sxs-lookup"><span data-stu-id="44a73-118">If a stroke is associated with an [**IContextNode**](icontextnode.md) that is not an unclassified ink node (see [**IContextNode::GetType**](icontextnode-gettype.md)), this method moves the stroke to an unclassified ink node that contains strokes of the same language.</span></span> <span data-ttu-id="44a73-119">Si ce nœud de contexte n’existe pas, cette méthode crée un nouveau nœud d’encre non classifié et lui ajoute le trait.</span><span class="sxs-lookup"><span data-stu-id="44a73-119">If no such context node exists, this method creates a new unclassified ink node and adds the stroke to it.</span></span> <span data-ttu-id="44a73-120">Un nœud d’encre non classifié est un **IContextNode** de type UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="44a73-120">An unclassified ink node is an **IContextNode** that is of type UnclassifiedInk.</span></span>

<span data-ttu-id="44a73-121">Si cette méthode déplace un trait d’un [**IContextNode**](icontextnode.md) qui n’est pas un nœud d’encre non classifié, cette méthode ajoute également le cadre englobant du trait à la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="44a73-121">If this method moves a stroke from an [**IContextNode**](icontextnode.md) that is not an unclassified ink node, this method also adds the stroke's bounding box to the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="44a73-122">Cette méthode ne déplace pas un trait si le paramètre *StrokeType* correspond au type actuel du trait.</span><span class="sxs-lookup"><span data-stu-id="44a73-122">This method does not move a stroke if the *StrokeType* parameter matches the stroke's current type.</span></span>

<span data-ttu-id="44a73-123">La définition du type de trait sur les traits associés à un ContextNode qui a NodeTypeAndProperties Confirm lève une exception InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="44a73-123">Setting the stroke type on strokes that are associated with a ContextNode that has NodeTypeAndProperties confirmed will raise an InvalidOperationException.</span></span>

<span data-ttu-id="44a73-124">Si le trait spécifié n’est pas associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne sans mettre à jour le **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="44a73-124">If the specified stroke is not associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns without updating the **IInkAnalyzer**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a73-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="44a73-125">Requirements</span></span>



| <span data-ttu-id="44a73-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44a73-126">Requirement</span></span> | <span data-ttu-id="44a73-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="44a73-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a73-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a73-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44a73-129">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44a73-129">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="44a73-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a73-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44a73-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="44a73-131">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="44a73-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="44a73-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="44a73-133"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="44a73-133"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="44a73-134">DLL</span><span class="sxs-lookup"><span data-stu-id="44a73-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44a73-135"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44a73-135"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="44a73-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44a73-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a73-137">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="44a73-137">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="44a73-138">**IInkAnalyzer :: GetStrokeType, méthode**</span><span class="sxs-lookup"><span data-stu-id="44a73-138">**IInkAnalyzer::GetStrokeType Method**</span></span>](iinkanalyzer-getstroketype.md)
</dt> <dt>

[<span data-ttu-id="44a73-139">**IInkAnalyzer :: SetStrokesType, méthode**</span><span class="sxs-lookup"><span data-stu-id="44a73-139">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="44a73-140">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="44a73-140">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




