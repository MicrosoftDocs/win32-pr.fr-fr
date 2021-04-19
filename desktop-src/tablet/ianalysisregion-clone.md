---
description: Crée une copie du IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'IAnalysisRegion :: Clone, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536117"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="20a71-103">IAnalysisRegion :: Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="20a71-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="20a71-104">Crée une copie du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="20a71-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20a71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20a71-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="20a71-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20a71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a71-107">*pClonedRegion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="20a71-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20a71-108">Pointeur vers une copie du [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="20a71-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a71-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="20a71-109">Return value</span></span>

<span data-ttu-id="20a71-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="20a71-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="20a71-111">Notes</span><span class="sxs-lookup"><span data-stu-id="20a71-111">Remarks</span></span>

<span data-ttu-id="20a71-112">Cette méthode est eqivalent à theSystem. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone dans le .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="20a71-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="20a71-113">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *pClonedRegion* lorsque vous n’avez plus besoin d’utiliser la région d’analyse clonée.</span><span class="sxs-lookup"><span data-stu-id="20a71-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="20a71-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a71-114">Requirements</span></span>



| <span data-ttu-id="20a71-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a71-115">Requirement</span></span> | <span data-ttu-id="20a71-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a71-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20a71-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a71-117">Minimum supported client</span></span><br/> | <span data-ttu-id="20a71-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="20a71-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="20a71-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a71-119">Minimum supported server</span></span><br/> | <span data-ttu-id="20a71-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="20a71-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="20a71-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="20a71-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="20a71-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="20a71-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="20a71-123">DLL</span><span class="sxs-lookup"><span data-stu-id="20a71-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20a71-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20a71-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="20a71-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a71-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a71-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="20a71-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="20a71-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="20a71-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

