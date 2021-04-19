---
description: Associe les traits spécifiés à ce IContextNode.
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'IContextNode :: SetStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be7fd1645af70e34c747894bc8ab4317b08e2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514446"
---
# <a name="icontextnodesetstrokes-method"></a><span data-ttu-id="2afaf-103">IContextNode :: SetStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="2afaf-103">IContextNode::SetStrokes method</span></span>

<span data-ttu-id="2afaf-104">Associe les traits spécifiés à ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2afaf-104">Associates the specified strokes with this [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2afaf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2afaf-105">Syntax</span></span>


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="2afaf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2afaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afaf-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2afaf-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2afaf-108">Nombre d’identificateurs de trait dans *plStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="2afaf-108">The number of stroke identifiers in *plStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="2afaf-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2afaf-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2afaf-110">Identificateurs des traits à associer à ce [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="2afaf-110">The identifiers of the strokes to associate with this [**IContextNode**](icontextnode.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afaf-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2afaf-111">Return value</span></span>

<span data-ttu-id="2afaf-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2afaf-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2afaf-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2afaf-113">Remarks</span></span>

<span data-ttu-id="2afaf-114">Cette méthode ne met pas à jour la région de modification de l’analyseur d’encre (consultez la [**méthode IInkAnalyzer :: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).</span><span class="sxs-lookup"><span data-stu-id="2afaf-114">This method does not update the ink analyzer's dirty region (see [**IInkAnalyzer::GetDirtyRegion Method**](iinkanalyzer-getdirtyregion.md)).</span></span>

<span data-ttu-id="2afaf-115">Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="2afaf-115">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="2afaf-116">Utilisez cette méthode pour assigner des données de trait à un nœud de contexte spécifique.</span><span class="sxs-lookup"><span data-stu-id="2afaf-116">Use this method to assign stroke data to a specific context node.</span></span> <span data-ttu-id="2afaf-117">Pour plus d’informations sur la synchronisation des données de votre application avec **IInkAnalyzer**, consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="2afaf-117">For more information about synchronizing your application data with the **IInkAnalyzer**, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="2afaf-118">Si l’un des traits spécifiés est déjà associé à [**IInkAnalyzer**](iinkanalyzer.md), cette méthode retourne **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="2afaf-118">If any of the specified strokes are already associated with the [**IInkAnalyzer**](iinkanalyzer.md), this method returns **E\_INVALIDARG**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2afaf-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2afaf-119">Requirements</span></span>



| <span data-ttu-id="2afaf-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2afaf-120">Requirement</span></span> | <span data-ttu-id="2afaf-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2afaf-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2afaf-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afaf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2afaf-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2afaf-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2afaf-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afaf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2afaf-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afaf-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2afaf-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2afaf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2afaf-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2afaf-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2afaf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2afaf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2afaf-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2afaf-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2afaf-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2afaf-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afaf-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2afaf-132">**IInkAnalyzer :: AddStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-132">**IInkAnalyzer::AddStroke Method**</span></span>](iinkanalyzer-addstroke.md)
</dt> <dt>

[<span data-ttu-id="2afaf-133">**IInkAnalyzer :: AddStrokeForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-133">**IInkAnalyzer::AddStrokeForLanguage Method**</span></span>](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[<span data-ttu-id="2afaf-134">**IInkAnalyzer :: AddStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-134">**IInkAnalyzer::AddStrokes Method**</span></span>](iinkanalyzer-addstrokes.md)
</dt> <dt>

[<span data-ttu-id="2afaf-135">**IInkAnalyzer :: AddStrokesForLanguage, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-135">**IInkAnalyzer::AddStrokesForLanguage Method**</span></span>](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[<span data-ttu-id="2afaf-136">**IInkAnalyzer :: AddStrokesToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-136">**IInkAnalyzer::AddStrokesToCustomRecognizer Method**</span></span>](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="2afaf-137">**IInkAnalyzer :: AddStrokeToCustomRecognizer, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-137">**IInkAnalyzer::AddStrokeToCustomRecognizer Method**</span></span>](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="2afaf-138">**IInkAnalyzer :: RemoveStroke, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-138">**IInkAnalyzer::RemoveStroke Method**</span></span>](iinkanalyzer-removestroke.md)
</dt> <dt>

[<span data-ttu-id="2afaf-139">**IInkAnalyzer :: RemoveStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="2afaf-139">**IInkAnalyzer::RemoveStrokes Method**</span></span>](iinkanalyzer-removestrokes.md)
</dt> <dt>

[<span data-ttu-id="2afaf-140">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="2afaf-140">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="2afaf-141">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="2afaf-141">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="2afaf-142">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="2afaf-142">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




