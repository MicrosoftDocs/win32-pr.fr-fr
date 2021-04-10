---
description: Enregistre les résultats d’analyse pour une collection de nœuds de contexte spécifique associée à un IInkAnalyzer.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer :: SaveResultsForNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113327"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a><span data-ttu-id="950a7-103">IInkAnalyzer :: SaveResultsForNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="950a7-103">IInkAnalyzer::SaveResultsForNodes method</span></span>

<span data-ttu-id="950a7-104">Enregistre les résultats d’analyse pour une collection de nœuds de contexte spécifique associée à un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="950a7-104">Saves analysis results for a specific context node collection associated with an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="950a7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="950a7-105">Syntax</span></span>


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="950a7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="950a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950a7-107">*pContextNodes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="950a7-107">*pContextNodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="950a7-108">Collection [**IContextNode**](icontextnode.md) pour laquelle enregistrer les résultats de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="950a7-108">The [**IContextNode**](icontextnode.md) collection for which to save analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="950a7-109">*pulSerializedDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="950a7-109">*pulSerializedDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="950a7-110">Nombre d’octets dans *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="950a7-110">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="950a7-111">*ppbSerializedData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="950a7-111">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="950a7-112">Pointeur vers les données d’analyse sérialisées.</span><span class="sxs-lookup"><span data-stu-id="950a7-112">Pointer to the serialized analysis data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950a7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="950a7-113">Return value</span></span>

<span data-ttu-id="950a7-114">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="950a7-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="950a7-115">Notes</span><span class="sxs-lookup"><span data-stu-id="950a7-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="950a7-116">Pour éviter une fuite de mémoire, appelez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) sur \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="950a7-116">To avoid a memory leak, call [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) on \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="950a7-117">Cette méthode enregistre les résultats de l’analyse actuelle pour les objets [**IContextNode**](icontextnode.md) dans *pContextNodes* et tous leurs nœuds de contexte ancêtres et descendants.</span><span class="sxs-lookup"><span data-stu-id="950a7-117">This method saves the current analysis results for the [**IContextNode**](icontextnode.md) objects in *pContextNodes* and all of their ancestor and descendant context nodes.</span></span> <span data-ttu-id="950a7-118">Cette méthode n’enregistre aucune donnée de trait.</span><span class="sxs-lookup"><span data-stu-id="950a7-118">This method does not save any stroke data.</span></span> <span data-ttu-id="950a7-119">Il incombe à votre application de synchroniser les résultats de l’analyse et les données de trait correspondantes, si elle persiste.</span><span class="sxs-lookup"><span data-stu-id="950a7-119">It is the responsibility of your application to synchronize any analysis results and corresponding stroke data, if it persists.</span></span>

<span data-ttu-id="950a7-120">Si l’objet [**IContextNode**](icontextnode.md) à enregistrer n’est rempli que partiellement, cette méthode retourne un code d’erreur (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="950a7-120">If the [**IContextNode**](icontextnode.md) object to be saved is only partially populated, this method returns an error code (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="950a7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="950a7-121">Requirements</span></span>



| <span data-ttu-id="950a7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="950a7-122">Requirement</span></span> | <span data-ttu-id="950a7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="950a7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="950a7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="950a7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="950a7-125">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="950a7-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="950a7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="950a7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="950a7-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="950a7-127">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="950a7-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="950a7-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="950a7-129"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="950a7-129"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="950a7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="950a7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="950a7-131"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="950a7-131"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="950a7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="950a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950a7-133">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="950a7-133">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="950a7-134">**IInkAnalyzer :: LoadResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="950a7-134">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="950a7-135">**IInkAnalyzer :: SaveResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="950a7-135">**IInkAnalyzer::SaveResults Method**</span></span>](iinkanalyzer-saveresults.md)
</dt> <dt>

[<span data-ttu-id="950a7-136">**IInkAnalyzer :: SaveResultsForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="950a7-136">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="950a7-137">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="950a7-137">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="950a7-138">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="950a7-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

