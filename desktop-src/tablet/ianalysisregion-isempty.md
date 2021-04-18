---
description: Récupère une valeur indiquant si le IAnalysisRegion représente une zone vide.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'IAnalysisRegion :: IsEmpty, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533604"
---
# <a name="ianalysisregionisempty-method"></a><span data-ttu-id="78d4c-103">IAnalysisRegion :: IsEmpty, méthode</span><span class="sxs-lookup"><span data-stu-id="78d4c-103">IAnalysisRegion::IsEmpty method</span></span>

<span data-ttu-id="78d4c-104">Récupère une valeur indiquant si le [**IAnalysisRegion**](ianalysisregion.md) représente une zone vide.</span><span class="sxs-lookup"><span data-stu-id="78d4c-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an empty region.</span></span>

## <a name="syntax"></a><span data-ttu-id="78d4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78d4c-105">Syntax</span></span>


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a><span data-ttu-id="78d4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78d4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78d4c-107">*pfIsEmpty* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="78d4c-107">*pfIsEmpty* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78d4c-108">**Variante \_ TRUE** si la région représentée est vide ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="78d4c-108">**VARIANT\_TRUE** if the represented region is empty; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78d4c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78d4c-109">Return value</span></span>

<span data-ttu-id="78d4c-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="78d4c-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78d4c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78d4c-111">Requirements</span></span>



| <span data-ttu-id="78d4c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78d4c-112">Requirement</span></span> | <span data-ttu-id="78d4c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="78d4c-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78d4c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d4c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="78d4c-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="78d4c-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="78d4c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d4c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="78d4c-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="78d4c-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="78d4c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="78d4c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="78d4c-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="78d4c-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="78d4c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="78d4c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78d4c-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78d4c-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="78d4c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78d4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78d4c-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="78d4c-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="78d4c-124">**IAnalysisRegion :: IsInfinite, méthode**</span><span class="sxs-lookup"><span data-stu-id="78d4c-124">**IAnalysisRegion::IsInfinite Method**</span></span>](ianalysisregion-isinfinite.md)
</dt> <dt>

[<span data-ttu-id="78d4c-125">**IAnalysisRegion :: MakeEmpty, méthode**</span><span class="sxs-lookup"><span data-stu-id="78d4c-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="78d4c-126">**IAnalysisRegion :: MakeInfinite, méthode**</span><span class="sxs-lookup"><span data-stu-id="78d4c-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="78d4c-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="78d4c-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




