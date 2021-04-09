---
title: FreeRootCauseInfos, fonction (Ndattributils. h)
description: Libère la mémoire allouée en interne à un tableau de structures RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- FreeRootCauseInfos fonction NDF
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740893"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="a9685-104">FreeRootCauseInfos fonction)</span><span class="sxs-lookup"><span data-stu-id="a9685-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="a9685-105">La fonction **FreeRootCauseInfos** libère la mémoire allouée en interne à un tableau de structures [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="a9685-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="a9685-106">Cette fonction appelle [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="a9685-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9685-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a9685-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="a9685-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a9685-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9685-109">*pinfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a9685-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9685-110">Tapez : \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="a9685-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="a9685-111">Tableau de structures.</span><span class="sxs-lookup"><span data-stu-id="a9685-111">The array of structures.</span></span> <span data-ttu-id="a9685-112">La mémoire allouée pointée par ces structures sera libérée.</span><span class="sxs-lookup"><span data-stu-id="a9685-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="a9685-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="a9685-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="a9685-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="a9685-114">Type: **ULONG**</span></span>

<span data-ttu-id="a9685-115">Nombre de structures dans le tableau pointé par *pinfo*.</span><span class="sxs-lookup"><span data-stu-id="a9685-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="a9685-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="a9685-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="a9685-117">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="a9685-117">Type: **BOOL**</span></span>

<span data-ttu-id="a9685-118">True si le tableau de structures doit également être supprimé ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="a9685-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9685-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a9685-119">Return value</span></span>

<span data-ttu-id="a9685-120">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a9685-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9685-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9685-121">Requirements</span></span>



| <span data-ttu-id="a9685-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9685-122">Requirement</span></span> | <span data-ttu-id="a9685-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9685-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9685-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9685-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9685-125">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9685-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a9685-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9685-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9685-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9685-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a9685-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9685-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9685-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9685-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9685-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9685-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9685-131">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="a9685-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="a9685-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="a9685-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

