---
description: Récupère une valeur indiquant si le IAnalysisRegion représente une région infinie.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'IAnalysisRegion :: IsInfinite, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201519"
---
# <a name="ianalysisregionisinfinite-method"></a><span data-ttu-id="c21be-103">IAnalysisRegion :: IsInfinite, méthode</span><span class="sxs-lookup"><span data-stu-id="c21be-103">IAnalysisRegion::IsInfinite method</span></span>

<span data-ttu-id="c21be-104">Récupère une valeur indiquant si le [**IAnalysisRegion**](ianalysisregion.md) représente une région infinie.</span><span class="sxs-lookup"><span data-stu-id="c21be-104">Retrieves a value indicating whether the [**IAnalysisRegion**](ianalysisregion.md) represents an infinite region.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21be-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c21be-105">Syntax</span></span>


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a><span data-ttu-id="c21be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c21be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c21be-107">*pfIsInfinite* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c21be-107">*pfIsInfinite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c21be-108">**Variante \_ TRUE** si la zone représentée est infinie ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="c21be-108">**VARIANT\_TRUE** if the represented region is infinite; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c21be-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c21be-109">Return value</span></span>

<span data-ttu-id="c21be-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c21be-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c21be-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c21be-111">Requirements</span></span>



| <span data-ttu-id="c21be-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c21be-112">Requirement</span></span> | <span data-ttu-id="c21be-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c21be-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c21be-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21be-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c21be-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c21be-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c21be-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21be-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c21be-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c21be-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c21be-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c21be-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c21be-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c21be-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c21be-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c21be-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c21be-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c21be-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c21be-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c21be-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c21be-123">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c21be-123">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c21be-124">**IAnalysisRegion :: IsEmpty, méthode**</span><span class="sxs-lookup"><span data-stu-id="c21be-124">**IAnalysisRegion::IsEmpty Method**</span></span>](ianalysisregion-isempty.md)
</dt> <dt>

[<span data-ttu-id="c21be-125">**IAnalysisRegion :: MakeEmpty, méthode**</span><span class="sxs-lookup"><span data-stu-id="c21be-125">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
</dt> <dt>

[<span data-ttu-id="c21be-126">**IAnalysisRegion :: MakeInfinite, méthode**</span><span class="sxs-lookup"><span data-stu-id="c21be-126">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
</dt> <dt>

[<span data-ttu-id="c21be-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="c21be-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




