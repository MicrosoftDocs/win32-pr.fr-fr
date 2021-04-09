---
description: Détermine si le IAnalysisRegion spécifié contient la même valeur que l’objet IAnalysisRegion actuel.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion :: EqualsRegion, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113407"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="f432b-103">IAnalysisRegion :: EqualsRegion, méthode</span><span class="sxs-lookup"><span data-stu-id="f432b-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="f432b-104">Détermine si le [**IAnalysisRegion**](ianalysisregion.md) spécifié contient la même valeur que l’objet **IAnalysisRegion** actuel.</span><span class="sxs-lookup"><span data-stu-id="f432b-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f432b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f432b-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="f432b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f432b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f432b-107">*pOtherRegion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f432b-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f432b-108">Objet [**IAnalysisRegion**](ianalysisregion.md) à comparer avec le **IAnalysisRegion** actif.</span><span class="sxs-lookup"><span data-stu-id="f432b-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="f432b-109">*pfRegionsEqual* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f432b-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f432b-110">**Variante \_ TRUE** si le [**IAnalysisRegion**](ianalysisregion.md) spécifié contient la même valeur que le IAnalysisRegion en cours ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="f432b-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f432b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f432b-111">Return value</span></span>

<span data-ttu-id="f432b-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="f432b-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f432b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f432b-113">Requirements</span></span>



| <span data-ttu-id="f432b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f432b-114">Requirement</span></span> | <span data-ttu-id="f432b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f432b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f432b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f432b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f432b-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f432b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f432b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f432b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f432b-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f432b-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f432b-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f432b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f432b-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f432b-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f432b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f432b-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f432b-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f432b-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f432b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f432b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f432b-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="f432b-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




