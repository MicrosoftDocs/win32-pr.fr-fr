---
description: Supprime une partie des données spécifiques à l’application.
ms.assetid: 41077c2f-39e3-4069-ac05-97f1785e37b7
title: 'IContextNode :: RemovePropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.RemovePropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4c2fd5924b206ee296c066a908d2a59b02019f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526517"
---
# <a name="icontextnoderemovepropertydata-method"></a><span data-ttu-id="65a89-103">IContextNode :: RemovePropertyData, méthode</span><span class="sxs-lookup"><span data-stu-id="65a89-103">IContextNode::RemovePropertyData method</span></span>

<span data-ttu-id="65a89-104">Supprime une partie des données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="65a89-104">Removes a piece of application-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65a89-105">Syntax</span></span>


```C++
HRESULT RemovePropertyData(
  [in] const GUID *pPropertyDataId
);
```



## <a name="parameters"></a><span data-ttu-id="65a89-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65a89-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65a89-107">*pPropertyDataId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65a89-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65a89-108">Identificateur des données à supprimer.</span><span class="sxs-lookup"><span data-stu-id="65a89-108">The identifier of the data to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65a89-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65a89-109">Return value</span></span>

<span data-ttu-id="65a89-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="65a89-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="65a89-111">Notes</span><span class="sxs-lookup"><span data-stu-id="65a89-111">Remarks</span></span>

<span data-ttu-id="65a89-112">**E \_** L’élément INVALIDARG est retourné si le paramètre *pPropertyDataId* est l’une des constantes de [propriété du nœud de contexte](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="65a89-112">**E\_INVALIDARG** is returned if the *pPropertyDataId* parameter is one of the [Context Node Properties](context-node-properties.md) constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a89-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65a89-113">Requirements</span></span>



| <span data-ttu-id="65a89-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65a89-114">Requirement</span></span> | <span data-ttu-id="65a89-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="65a89-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a89-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65a89-116">Minimum supported client</span></span><br/> | <span data-ttu-id="65a89-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65a89-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="65a89-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65a89-118">Minimum supported server</span></span><br/> | <span data-ttu-id="65a89-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65a89-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="65a89-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="65a89-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="65a89-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="65a89-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="65a89-122">DLL</span><span class="sxs-lookup"><span data-stu-id="65a89-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65a89-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65a89-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="65a89-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65a89-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a89-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="65a89-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="65a89-126">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="65a89-126">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="65a89-127">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="65a89-127">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="65a89-128">**IContextNode::GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="65a89-128">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="65a89-129">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="65a89-129">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="65a89-130">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="65a89-130">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="65a89-131">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="65a89-131">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="65a89-132">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="65a89-132">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




