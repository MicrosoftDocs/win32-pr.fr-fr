---
description: Enregistre tous les résultats d’analyse pour un IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer :: SaveResults, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318449"
---
# <a name="iinkanalyzersaveresults-method"></a><span data-ttu-id="f3392-103">IInkAnalyzer :: SaveResults, méthode</span><span class="sxs-lookup"><span data-stu-id="f3392-103">IInkAnalyzer::SaveResults method</span></span>

<span data-ttu-id="f3392-104">Enregistre tous les résultats d’analyse pour un [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f3392-104">Saves all analysis results for an [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3392-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3392-105">Syntax</span></span>


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a><span data-ttu-id="f3392-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3392-107">*pulSerializedDataSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f3392-107">*pulSerializedDataSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3392-108">Nombre d’octets dans *ppbSerializedData*.</span><span class="sxs-lookup"><span data-stu-id="f3392-108">The number of bytes in *ppbSerializedData*.</span></span>

</dd> <dt>

<span data-ttu-id="f3392-109">*ppbSerializedData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f3392-109">*ppbSerializedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3392-110">Tableau contenant les résultats d’analyse enregistrés.</span><span class="sxs-lookup"><span data-stu-id="f3392-110">An array containing the saved analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3392-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3392-111">Return value</span></span>

<span data-ttu-id="f3392-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f3392-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3392-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f3392-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f3392-114">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbSerializedData* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="f3392-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbSerializedData* when you no longer need the information.</span></span>

 

<span data-ttu-id="f3392-115">Cette méthode enregistre tous les résultats d’analyse actuels, qui incluent l’indicateur d’analyse actuel et les nœuds de reconnaissance personnalisés (consultez [**IContextNode :: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="f3392-115">This method saves all the current analysis results, which include current analysis hint and custom recognizer nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="f3392-116">Cette méthode n’enregistre aucune donnée de trait.</span><span class="sxs-lookup"><span data-stu-id="f3392-116">This method does not save any stroke data.</span></span> <span data-ttu-id="f3392-117">Il incombe à votre application de synchroniser les résultats de l’analyse et les traits correspondants si elle conserve les données.</span><span class="sxs-lookup"><span data-stu-id="f3392-117">It is the responsibility of your application to synchronize any analysis results and corresponding strokes if it persists data.</span></span>

<span data-ttu-id="f3392-118">Cette méthode retourne un code d’erreur lorsqu’un objet [**IContextNode**](icontextnode.md) à enregistrer est partiellement rempli (consultez [**IContextNode :: GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span><span class="sxs-lookup"><span data-stu-id="f3392-118">This method returns an error code when an [**IContextNode**](icontextnode.md) object to save is partially populated (see [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3392-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3392-119">Requirements</span></span>



| <span data-ttu-id="f3392-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3392-120">Requirement</span></span> | <span data-ttu-id="f3392-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3392-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3392-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3392-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3392-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3392-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f3392-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3392-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3392-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3392-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f3392-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3392-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3392-127"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f3392-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f3392-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f3392-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3392-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3392-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f3392-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3392-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3392-131">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f3392-131">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f3392-132">**IInkAnalyzer :: LoadResults, méthode**</span><span class="sxs-lookup"><span data-stu-id="f3392-132">**IInkAnalyzer::LoadResults Method**</span></span>](iinkanalyzer-loadresults.md)
</dt> <dt>

[<span data-ttu-id="f3392-133">**IInkAnalyzer :: SaveResultsForNodes, méthode**</span><span class="sxs-lookup"><span data-stu-id="f3392-133">**IInkAnalyzer::SaveResultsForNodes Method**</span></span>](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[<span data-ttu-id="f3392-134">**IInkAnalyzer :: SaveResultsForStrokes, méthode**</span><span class="sxs-lookup"><span data-stu-id="f3392-134">**IInkAnalyzer::SaveResultsForStrokes Method**</span></span>](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[<span data-ttu-id="f3392-135">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="f3392-135">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="f3392-136">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="f3392-136">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

