---
description: Enregistre les résultats d’analyse pour les traits spécifiés associés à un IInkAnalyzer.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer :: SaveResultsForStrokes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318446"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a><span data-ttu-id="cd272-103">IInkAnalyzer :: SaveResultsForStrokes, méthode</span><span class="sxs-lookup"><span data-stu-id="cd272-103">IInkAnalyzer::SaveResultsForStrokes method</span></span>

<span data-ttu-id="cd272-104">Enregistre les résultats d’analyse pour les traits spécifiés associés à un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="cd272-104">Saves analysis results for the specified strokes associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd272-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd272-105">Syntax</span></span>


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="cd272-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd272-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd272-107">*ulStrokeIdsCount* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd272-107">*ulStrokeIdsCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd272-108">Nombre d’identificateurs de trait dans **plStrokeIds**.</span><span class="sxs-lookup"><span data-stu-id="cd272-108">The number of stroke identifiers in **plStrokeIds**.</span></span>

</dd> <dt>

<span data-ttu-id="cd272-109">*plStrokeIds* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd272-109">*plStrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd272-110">Tableau d’identificateurs de trait.</span><span class="sxs-lookup"><span data-stu-id="cd272-110">The array of stroke identifiers.</span></span>

</dd> <dt>

<span data-ttu-id="cd272-111">*pulSerializedDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cd272-111">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd272-112">Nombre d’octets dans *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="cd272-112">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="cd272-113">*ppbSerializedData* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cd272-113">*ppbSerializedData* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cd272-114">Pointeur vers les données d’analyse sérialisées.</span><span class="sxs-lookup"><span data-stu-id="cd272-114">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd272-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd272-115">Return value</span></span>

<span data-ttu-id="cd272-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="cd272-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd272-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cd272-117">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cd272-118">Pour éviter une fuite de mémoire, appelez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) sur \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="cd272-118">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="cd272-119">Cette méthode enregistre les résultats de l’analyse actuelle pour les traits spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cd272-119">This method saves the current analysis results for the specified strokes.</span></span> <span data-ttu-id="cd272-120">Cette méthode enregistre les objets [**IContextNode**](icontextnode.md) feuille manuscrits contenant les traits et tous les ancêtres de ces nœuds de contexte.</span><span class="sxs-lookup"><span data-stu-id="cd272-120">This method saves the ink leaf [**IContextNode**](icontextnode.md) objects containing the strokes and all of the ancestors of those context nodes.</span></span> <span data-ttu-id="cd272-121">Cette méthode n’enregistre aucune donnée de trait ni aucun nœud d’indicateur d’analyse.</span><span class="sxs-lookup"><span data-stu-id="cd272-121">This method does not save any stroke data or analysis hint nodes.</span></span> <span data-ttu-id="cd272-122">Il incombe à votre application de synchroniser les résultats de l’analyse et les données de trait correspondantes, si elle persiste.</span><span class="sxs-lookup"><span data-stu-id="cd272-122">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="cd272-123">Cette méthode retourne un code d’erreur lorsqu’un objet [**IContextNode**](icontextnode.md) à enregistrer est partiellement rempli (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="cd272-123">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd272-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd272-124">Requirements</span></span>



| <span data-ttu-id="cd272-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd272-125">Requirement</span></span> | <span data-ttu-id="cd272-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd272-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd272-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd272-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cd272-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd272-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cd272-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd272-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cd272-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd272-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cd272-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd272-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd272-132"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cd272-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cd272-133">DLL</span><span class="sxs-lookup"><span data-stu-id="cd272-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd272-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd272-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cd272-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd272-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd272-136">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="cd272-136">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="cd272-137">**IInkAnalyzer :: LoadResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="cd272-137">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="cd272-138">**IInkAnalyzer :: SaveResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="cd272-138">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="cd272-139">**IInkAnalyzer :: SaveResultsForNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="cd272-139">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="cd272-140">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="cd272-140">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cd272-141">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="cd272-141">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

