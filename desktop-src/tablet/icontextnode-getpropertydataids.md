---
description: Récupère les identificateurs pour lesquels il existe des données de propriété.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'IContextNode :: GetPropertyDataIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cdbc0ec0a613feccb4064a88f4723538439f4532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516482"
---
# <a name="icontextnodegetpropertydataids-method"></a><span data-ttu-id="214a8-103">IContextNode :: GetPropertyDataIds, méthode</span><span class="sxs-lookup"><span data-stu-id="214a8-103">IContextNode::GetPropertyDataIds method</span></span>

<span data-ttu-id="214a8-104">Récupère les identificateurs pour lesquels il existe des données de propriété.</span><span class="sxs-lookup"><span data-stu-id="214a8-104">Retrieves the identifiers for which there is property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="214a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="214a8-105">Syntax</span></span>


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a><span data-ttu-id="214a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="214a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214a8-107">*pulGuidCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="214a8-107">*pulGuidCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a8-108">Nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="214a8-108">The number of properties.</span></span>

</dd> <dt>

<span data-ttu-id="214a8-109">*ppGuids* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="214a8-109">*ppGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="214a8-110">Identificateurs pour lesquels il existe des données de propriété.</span><span class="sxs-lookup"><span data-stu-id="214a8-110">The identifiers for which there is property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214a8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="214a8-111">Return value</span></span>

<span data-ttu-id="214a8-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="214a8-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="214a8-113">Notes</span><span class="sxs-lookup"><span data-stu-id="214a8-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="214a8-114">Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppGuids* lorsque vous n’avez plus besoin des informations.</span><span class="sxs-lookup"><span data-stu-id="214a8-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppGuids* when you no longer need the information.</span></span>

 

<span data-ttu-id="214a8-115">Cette méthode retourne les identificateurs spécifiques à l’application pour les données de propriété qui ont été ajoutées.</span><span class="sxs-lookup"><span data-stu-id="214a8-115">This method returns the application-specific identifiers for property data that has been added.</span></span> <span data-ttu-id="214a8-116">Elle retourne également les identificateurs pour les données de propriété internes, qui sont décrites par les constantes des [Propriétés du nœud de contexte](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="214a8-116">It also returns the identifiers for the internal property data, which are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="214a8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="214a8-117">Requirements</span></span>



| <span data-ttu-id="214a8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="214a8-118">Requirement</span></span> | <span data-ttu-id="214a8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="214a8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="214a8-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="214a8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="214a8-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="214a8-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="214a8-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="214a8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="214a8-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="214a8-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="214a8-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="214a8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="214a8-125"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="214a8-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="214a8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="214a8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214a8-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214a8-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="214a8-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="214a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="214a8-129">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="214a8-129">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="214a8-130">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="214a8-130">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="214a8-131">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="214a8-131">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="214a8-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="214a8-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="214a8-133">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="214a8-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

