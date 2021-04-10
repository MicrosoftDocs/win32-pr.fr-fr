---
title: FreeRepairInfos, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- FreeRepairInfos fonction NDF
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103288"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="33dcb-104">FreeRepairInfos fonction)</span><span class="sxs-lookup"><span data-stu-id="33dcb-104">FreeRepairInfos function</span></span>

<span data-ttu-id="33dcb-105">La fonction **FreeRepairInfos** libère la mémoire allouée en interne à un tableau de structures [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="33dcb-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="33dcb-106">Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="33dcb-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="33dcb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33dcb-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="33dcb-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33dcb-109">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="33dcb-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33dcb-110">Tapez : \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="33dcb-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="33dcb-111">Tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="33dcb-111">The array of structures.</span></span> <span data-ttu-id="33dcb-112">La mémoire allouée pointée par ces structures sera libérée.</span><span class="sxs-lookup"><span data-stu-id="33dcb-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="33dcb-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="33dcb-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="33dcb-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="33dcb-114">Type: **ULONG**</span></span>

<span data-ttu-id="33dcb-115">Nombre de structures dans le tableau pointé par *pinfo*.</span><span class="sxs-lookup"><span data-stu-id="33dcb-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="33dcb-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="33dcb-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="33dcb-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="33dcb-117">Type: **BOOL**</span></span>

<span data-ttu-id="33dcb-118">True si le tableau de structures doit également être supprimé ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="33dcb-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33dcb-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33dcb-119">Return value</span></span>

<span data-ttu-id="33dcb-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="33dcb-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="33dcb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33dcb-121">Requirements</span></span>



| <span data-ttu-id="33dcb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33dcb-122">Requirement</span></span> | <span data-ttu-id="33dcb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="33dcb-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="33dcb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33dcb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="33dcb-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33dcb-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="33dcb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33dcb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="33dcb-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33dcb-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="33dcb-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="33dcb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="33dcb-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="33dcb-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33dcb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33dcb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33dcb-131">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="33dcb-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="33dcb-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="33dcb-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

