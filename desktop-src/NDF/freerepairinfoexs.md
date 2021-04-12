---
title: FreeRepairInfoExs, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- FreeRepairInfoExs fonction NDF
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508674"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="ef11c-104">FreeRepairInfoExs fonction)</span><span class="sxs-lookup"><span data-stu-id="ef11c-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="ef11c-105">La fonction **FreeRepairInfoExs** libère la mémoire allouée en interne à un tableau de structures [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) .</span><span class="sxs-lookup"><span data-stu-id="ef11c-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="ef11c-106">Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ef11c-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef11c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef11c-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="ef11c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef11c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef11c-109">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ef11c-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef11c-110">Tapez : \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="ef11c-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="ef11c-111">Tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="ef11c-111">The array of structures.</span></span> <span data-ttu-id="ef11c-112">La mémoire allouée pointée par ces structures sera libérée.</span><span class="sxs-lookup"><span data-stu-id="ef11c-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="ef11c-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="ef11c-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="ef11c-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ef11c-114">Type: **ULONG**</span></span>

<span data-ttu-id="ef11c-115">Nombre de structures dans le tableau pointé par *pinfo*.</span><span class="sxs-lookup"><span data-stu-id="ef11c-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="ef11c-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="ef11c-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="ef11c-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="ef11c-117">Type: **BOOL**</span></span>

<span data-ttu-id="ef11c-118">True si le tableau de structures doit également être supprimé ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="ef11c-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef11c-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ef11c-119">Return value</span></span>

<span data-ttu-id="ef11c-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ef11c-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef11c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef11c-121">Requirements</span></span>



| <span data-ttu-id="ef11c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef11c-122">Requirement</span></span> | <span data-ttu-id="ef11c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef11c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef11c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef11c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ef11c-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef11c-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ef11c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef11c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ef11c-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef11c-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ef11c-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef11c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef11c-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef11c-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef11c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef11c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef11c-131">**RepairInfoEx**</span><span class="sxs-lookup"><span data-stu-id="ef11c-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="ef11c-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="ef11c-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

