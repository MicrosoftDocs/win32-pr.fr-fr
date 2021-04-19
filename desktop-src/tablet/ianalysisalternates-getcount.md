---
description: Récupère le nombre d’objets IAnalysisAlternate contenus dans la collection IAnalysisAlternates.
ms.assetid: 17b71b5a-638a-4e6e-a43b-4ca3c8eba257
title: 'IAnalysisAlternates :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6300ff994d7bd49461e9be39aa433586ecaabc75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544684"
---
# <a name="ianalysisalternatesgetcount-method"></a><span data-ttu-id="29dfe-103">IAnalysisAlternates :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="29dfe-103">IAnalysisAlternates::GetCount method</span></span>

<span data-ttu-id="29dfe-104">Récupère le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="29dfe-104">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="29dfe-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29dfe-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="29dfe-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29dfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29dfe-107">*pulCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="29dfe-107">*pulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29dfe-108">Entier 32 bits non signé qui a pour valeur le nombre d’objets [**IAnalysisAlternate**](ianalysisalternate.md) contenus dans la collection [**IAnalysisAlternates**](ianalysisalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="29dfe-108">An unsigned 32-bit integer that is set to the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the [**IAnalysisAlternates**](ianalysisalternates.md) collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29dfe-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29dfe-109">Return value</span></span>

<span data-ttu-id="29dfe-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="29dfe-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29dfe-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29dfe-111">Requirements</span></span>



| <span data-ttu-id="29dfe-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29dfe-112">Requirement</span></span> | <span data-ttu-id="29dfe-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="29dfe-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29dfe-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29dfe-114">Minimum supported client</span></span><br/> | <span data-ttu-id="29dfe-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29dfe-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29dfe-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29dfe-116">Minimum supported server</span></span><br/> | <span data-ttu-id="29dfe-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="29dfe-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="29dfe-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="29dfe-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="29dfe-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="29dfe-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="29dfe-120">DLL</span><span class="sxs-lookup"><span data-stu-id="29dfe-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29dfe-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29dfe-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="29dfe-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29dfe-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29dfe-123">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="29dfe-123">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="29dfe-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="29dfe-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




