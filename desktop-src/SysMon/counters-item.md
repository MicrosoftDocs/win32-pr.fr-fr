---
title: Compteurs. Item, propriété
description: Récupère l’instance CounterItem spécifiée de la collection.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Propriétés de l’élément SysMon
- Propriété d’élément SysMon, classe Counters
- Compteurs classe SysMon, propriété Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464714"
---
# <a name="countersitem-property"></a><span data-ttu-id="1521b-106">Compteurs. Item, propriété</span><span class="sxs-lookup"><span data-stu-id="1521b-106">Counters.Item property</span></span>

<span data-ttu-id="1521b-107">Récupère l’instance [**CounterItem**](counteritem.md) spécifiée de la collection.</span><span class="sxs-lookup"><span data-stu-id="1521b-107">Retrieves the specified [**CounterItem**](counteritem.md) instance from the collection.</span></span>

<span data-ttu-id="1521b-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1521b-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1521b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1521b-109">Syntax</span></span>


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a><span data-ttu-id="1521b-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1521b-110">Property value</span></span>

<span data-ttu-id="1521b-111">Instance [**CounterItem**](counteritem.md) qui correspond à la valeur d’index spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1521b-111">[**CounterItem**](counteritem.md) instance that corresponds to the specified index value.</span></span>

## <a name="exceptions"></a><span data-ttu-id="1521b-112">Exceptions</span><span class="sxs-lookup"><span data-stu-id="1521b-112">Exceptions</span></span>



| <span data-ttu-id="1521b-113">Type d'exception</span><span class="sxs-lookup"><span data-stu-id="1521b-113">Exception type</span></span>                                  | <span data-ttu-id="1521b-114">Condition</span><span class="sxs-lookup"><span data-stu-id="1521b-114">Condition</span></span>                         |
|-------------------------------------------------|-----------------------------------|
| <span data-ttu-id="1521b-115">**System. Runtime. InteropServices. COMException**</span><span class="sxs-lookup"><span data-stu-id="1521b-115">**System.Runtime.InteropServices.COMException**</span></span> | <span data-ttu-id="1521b-116">L’index spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1521b-116">The specified index is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1521b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="1521b-117">Remarks</span></span>

<span data-ttu-id="1521b-118">Il s’agit de la propriété par défaut de l’objet [**Counters**](counters.md) .</span><span class="sxs-lookup"><span data-stu-id="1521b-118">This is the default property of the [**Counters**](counters.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1521b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1521b-119">Requirements</span></span>



| <span data-ttu-id="1521b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1521b-120">Requirement</span></span> | <span data-ttu-id="1521b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1521b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1521b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1521b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1521b-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1521b-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1521b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1521b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1521b-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1521b-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1521b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="1521b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1521b-127"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1521b-127"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1521b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1521b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1521b-129">**CounterItem**</span><span class="sxs-lookup"><span data-stu-id="1521b-129">**CounterItem**</span></span>](counteritem.md)
</dt> <dt>

[<span data-ttu-id="1521b-130">**Counters**</span><span class="sxs-lookup"><span data-stu-id="1521b-130">**Counters**</span></span>](counters.md)
</dt> </dl>

 

 





