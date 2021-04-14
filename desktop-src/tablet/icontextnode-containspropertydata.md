---
description: Détermine si l’objet IContextNode contient des données stockées sous l’identificateur spécifié.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'IContextNode :: ContainsPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc45e1ebe519e5988ad73e1481c68e9e9811ba04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485113"
---
# <a name="icontextnodecontainspropertydata-method"></a><span data-ttu-id="2334a-103">IContextNode :: ContainsPropertyData, méthode</span><span class="sxs-lookup"><span data-stu-id="2334a-103">IContextNode::ContainsPropertyData method</span></span>

<span data-ttu-id="2334a-104">Détermine si l’objet [**IContextNode**](icontextnode.md) contient des données stockées sous l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="2334a-104">Determines whether the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="2334a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2334a-105">Syntax</span></span>


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a><span data-ttu-id="2334a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2334a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2334a-107">*pPropertyDataId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2334a-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2334a-108">Identificateur des données.</span><span class="sxs-lookup"><span data-stu-id="2334a-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="2334a-109">*pbContains* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2334a-109">*pbContains* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2334a-110">**Variante \_ TRUE** si l’objet [**IContextNode**](icontextnode.md) contient des données stockées sous l’identificateur spécifié ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="2334a-110">**VARIANT\_TRUE** if the [**IContextNode**](icontextnode.md) object contains data stored under the specified identifier; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2334a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2334a-111">Return value</span></span>

<span data-ttu-id="2334a-112">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="2334a-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2334a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2334a-113">Remarks</span></span>

<span data-ttu-id="2334a-114">Outre les données spécifiques à l’application, vous pouvez également utiliser cette méthode pour déterminer si ce [**IContextNode**](icontextnode.md) contient d’autres données internes (voir Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) et propriétés du nœud de [contexte](context-node-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="2334a-114">In addition to application-specific data, you can also use this method to determine whether this [**IContextNode**](icontextnode.md) contains other internal data (see [Analysis Hint Properties](analysis-hint-properties.md) and [Context Node Properties](context-node-properties.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="2334a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2334a-115">Requirements</span></span>



| <span data-ttu-id="2334a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2334a-116">Requirement</span></span> | <span data-ttu-id="2334a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2334a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2334a-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2334a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2334a-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2334a-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2334a-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2334a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2334a-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2334a-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="2334a-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2334a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2334a-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="2334a-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="2334a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2334a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2334a-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2334a-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="2334a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2334a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2334a-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="2334a-127">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="2334a-128">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2334a-128">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2334a-129">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="2334a-129">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="2334a-130">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="2334a-130">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="2334a-131">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="2334a-131">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="2334a-132">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="2334a-132">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="2334a-133">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="2334a-133">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="2334a-134">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="2334a-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




