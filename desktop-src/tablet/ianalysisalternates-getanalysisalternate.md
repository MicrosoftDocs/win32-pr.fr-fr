---
description: Récupère l’objet IAnalysisAlternate à l’index spécifié dans la collection.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'IAnalysisAlternates :: GetAnalysisAlternate, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516679"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="cd189-103">IAnalysisAlternates :: GetAnalysisAlternate, méthode</span><span class="sxs-lookup"><span data-stu-id="cd189-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="cd189-104">Récupère l’objet [**IAnalysisAlternate**](ianalysisalternate.md) à l’index spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="cd189-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd189-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd189-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="cd189-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd189-107">*ulIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd189-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd189-108">Index de base zéro de l’objet [**IAnalysisAlternate**](ianalysisalternate.md) à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cd189-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="cd189-109">*ppAlternate* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd189-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd189-110">Pointeur vers l’objet [**IAnalysisAlternate**](ianalysisalternate.md) à l’index spécifié dans la collection.</span><span class="sxs-lookup"><span data-stu-id="cd189-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd189-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd189-111">Return value</span></span>

<span data-ttu-id="cd189-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="cd189-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cd189-113">Notes</span><span class="sxs-lookup"><span data-stu-id="cd189-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cd189-114">Pour éviter une fuite de mémoire, appelez [**IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur \* *ppAlternate* lorsque vous n’avez plus besoin d’utiliser l’analyse alternative.</span><span class="sxs-lookup"><span data-stu-id="cd189-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cd189-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd189-115">Requirements</span></span>



| <span data-ttu-id="cd189-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd189-116">Requirement</span></span> | <span data-ttu-id="cd189-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd189-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd189-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd189-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd189-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd189-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cd189-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd189-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd189-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd189-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cd189-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="cd189-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd189-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cd189-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cd189-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cd189-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd189-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd189-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cd189-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd189-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd189-127">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="cd189-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="cd189-128">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="cd189-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

