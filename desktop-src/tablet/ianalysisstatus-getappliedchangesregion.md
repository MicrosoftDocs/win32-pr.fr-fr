---
description: Récupère la région du document qui correspond aux modifications apportées à l’arborescence du nœud de contexte de l’objet IInkAnalyzer à la suite de l’analyse de l’encre.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus :: GetAppliedChangesRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526547"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="9cd3b-103">IAnalysisStatus :: GetAppliedChangesRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="9cd3b-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="9cd3b-104">Récupère la région du document qui correspond aux modifications apportées à l’arborescence du nœud de contexte de l’objet [**IInkAnalyzer**](iinkanalyzer.md) à la suite de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9cd3b-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd3b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cd3b-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="9cd3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cd3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd3b-107">*pAppliedChangesRegion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9cd3b-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd3b-108">Pointeur vers le [**IAnalysisRegion**](ianalysisregion.md) du document où des modifications ont été apportées.</span><span class="sxs-lookup"><span data-stu-id="9cd3b-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd3b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9cd3b-109">Return value</span></span>

<span data-ttu-id="9cd3b-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9cd3b-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9cd3b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9cd3b-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="9cd3b-112">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pAppliedChangesRegion* lorsque vous n’avez plus besoin d’utiliser la région d’analyse.</span><span class="sxs-lookup"><span data-stu-id="9cd3b-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="9cd3b-113">Cette méthode est la plus fréquemment utilisée lorsque l’application reçoit des informations à des fins de débogage et qu’elle doit invalider la zone dans laquelle des modifications peuvent se produire afin que les informations de débogage soient peintes.</span><span class="sxs-lookup"><span data-stu-id="9cd3b-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd3b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9cd3b-114">Requirements</span></span>



| <span data-ttu-id="9cd3b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9cd3b-115">Requirement</span></span> | <span data-ttu-id="9cd3b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9cd3b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd3b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cd3b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd3b-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9cd3b-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9cd3b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cd3b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd3b-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9cd3b-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9cd3b-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9cd3b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cd3b-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9cd3b-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9cd3b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9cd3b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd3b-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd3b-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9cd3b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cd3b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd3b-126">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="9cd3b-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="9cd3b-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="9cd3b-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="9cd3b-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="9cd3b-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

