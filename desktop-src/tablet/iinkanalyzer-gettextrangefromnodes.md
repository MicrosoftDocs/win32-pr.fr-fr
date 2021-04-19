---
description: Recherche la plage de texte dans la chaîne reconnue qui correspond à une collection d’objets IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer :: GetTextRangeFromNodes, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527614"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="af43e-103">IInkAnalyzer :: GetTextRangeFromNodes, méthode</span><span class="sxs-lookup"><span data-stu-id="af43e-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="af43e-104">Recherche la plage de texte dans la chaîne reconnue qui correspond à une collection d’objets [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="af43e-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="af43e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="af43e-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="af43e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="af43e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af43e-107">*plStart* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af43e-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af43e-108">Entier signé 32 bits qui indique le début de la plage de texte.</span><span class="sxs-lookup"><span data-stu-id="af43e-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="af43e-109">Ce paramètre est passé sans être initialisé.</span><span class="sxs-lookup"><span data-stu-id="af43e-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="af43e-110">*plLength* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="af43e-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af43e-111">Entier signé 32 bits qui indique la longueur de la plage de texte.</span><span class="sxs-lookup"><span data-stu-id="af43e-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="af43e-112">Ce paramètre est passé sans être initialisé.</span><span class="sxs-lookup"><span data-stu-id="af43e-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="af43e-113">*pNodesToSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="af43e-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af43e-114">Collection d’objets [**IContextNode**](icontextnode.md) pour lesquels rechercher la plage de texte.</span><span class="sxs-lookup"><span data-stu-id="af43e-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af43e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="af43e-115">Return value</span></span>

<span data-ttu-id="af43e-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="af43e-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="af43e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="af43e-117">Remarks</span></span>

<span data-ttu-id="af43e-118">Si *pNodesToSearch* contient des objets [**IContextNode**](icontextnode.md) qui ne sont pas adjacents, cette méthode retourne la plus petite plage de texte qui couvre tous les objets **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="af43e-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="af43e-119">Cette méthode lève une exception E \_ INVALIDARG quand *pNodesToSearch* contient un [**IContextNode**](icontextnode.md) qui n’est pas associé au [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="af43e-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af43e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="af43e-120">Requirements</span></span>



| <span data-ttu-id="af43e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="af43e-121">Requirement</span></span> | <span data-ttu-id="af43e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="af43e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af43e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af43e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="af43e-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="af43e-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="af43e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="af43e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="af43e-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="af43e-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="af43e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="af43e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="af43e-128"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="af43e-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="af43e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="af43e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af43e-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af43e-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="af43e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af43e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af43e-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="af43e-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




