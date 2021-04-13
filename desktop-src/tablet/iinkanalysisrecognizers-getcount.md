---
description: Récupère le nombre d’objets IInkAnalysisRecognizer dans cette collection.
ms.assetid: dfb5c530-b481-4c60-b7fe-87fe162de270
title: 'IInkAnalysisRecognizers :: GetCount, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers.GetCount
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e65f8399c661d551e805abe5f1c5db33eb0b154a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526511"
---
# <a name="iinkanalysisrecognizersgetcount-method"></a><span data-ttu-id="7dbca-103">IInkAnalysisRecognizers :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="7dbca-103">IInkAnalysisRecognizers::GetCount method</span></span>

<span data-ttu-id="7dbca-104">Récupère le nombre d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="7dbca-104">Retrieves the number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dbca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7dbca-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [out, retval] ULONG *pulCount
);
```



## <a name="parameters"></a><span data-ttu-id="7dbca-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7dbca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbca-107">*pulCount* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7dbca-107">*pulCount* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7dbca-108">Nombre d’objets [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) dans cette collection.</span><span class="sxs-lookup"><span data-stu-id="7dbca-108">The number of [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) objects in this collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbca-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7dbca-109">Return value</span></span>

<span data-ttu-id="7dbca-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="7dbca-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbca-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7dbca-111">Requirements</span></span>



| <span data-ttu-id="7dbca-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7dbca-112">Requirement</span></span> | <span data-ttu-id="7dbca-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7dbca-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbca-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dbca-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbca-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7dbca-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7dbca-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dbca-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbca-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7dbca-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7dbca-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="7dbca-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dbca-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7dbca-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7dbca-120">DLL</span><span class="sxs-lookup"><span data-stu-id="7dbca-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dbca-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dbca-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7dbca-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7dbca-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbca-123">**InkAnalysisRecognizers**</span><span class="sxs-lookup"><span data-stu-id="7dbca-123">**InkAnalysisRecognizers**</span></span>](iinkanalysisrecognizers.md)
</dt> <dt>

[<span data-ttu-id="7dbca-124">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="7dbca-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




