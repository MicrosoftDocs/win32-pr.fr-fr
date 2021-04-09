---
description: Récupère un tableau d’identificateurs pour les traits dans l’objet IContextNode.
ms.assetid: 2420afec-6859-449b-92d8-0f4327281852
title: 'IContextNode :: GetStrokeIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 25592cd245eba135fa7e459ff3c5c5207fc6ff0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113383"
---
# <a name="icontextnodegetstrokeids-method"></a><span data-ttu-id="1acda-103">IContextNode :: GetStrokeIds, méthode</span><span class="sxs-lookup"><span data-stu-id="1acda-103">IContextNode::GetStrokeIds method</span></span>

<span data-ttu-id="1acda-104">Récupère un tableau d’identificateurs pour les traits dans l’objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1acda-104">Retrieves an array of identifiers for the strokes within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1acda-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1acda-105">Syntax</span></span>


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokes
);
```



## <a name="parameters"></a><span data-ttu-id="1acda-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1acda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1acda-107">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1acda-107">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1acda-108">Nombre de traits.</span><span class="sxs-lookup"><span data-stu-id="1acda-108">The number of strokes.</span></span> <span data-ttu-id="1acda-109">La valeur transmise n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="1acda-109">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1acda-110">*pplStrokes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1acda-110">*pplStrokes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1acda-111">Pointeur vers le tableau d’identificateurs de trait pour cet objet [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="1acda-111">A pointer to the array of stroke identifiers for this [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1acda-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1acda-112">Return value</span></span>

<span data-ttu-id="1acda-113">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="1acda-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1acda-114">Notes</span><span class="sxs-lookup"><span data-stu-id="1acda-114">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="1acda-115">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *pplStrokes* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="1acda-115">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**pplStrokes* when you no longer need the information.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1acda-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1acda-116">Requirements</span></span>



| <span data-ttu-id="1acda-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1acda-117">Requirement</span></span> | <span data-ttu-id="1acda-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1acda-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acda-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1acda-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1acda-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1acda-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1acda-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1acda-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1acda-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1acda-122">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1acda-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1acda-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1acda-124"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="1acda-124"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1acda-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1acda-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1acda-126"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1acda-126"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1acda-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1acda-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acda-128">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="1acda-128">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="1acda-129">**IContextNode::GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="1acda-129">**IContextNode::GetStrokeId**</span></span>](icontextnode-getstrokeid.md)
</dt> <dt>

[<span data-ttu-id="1acda-130">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="1acda-130">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="1acda-131">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="1acda-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

