---
title: CopyRepairInfo, fonction (Ndattributils. h)
description: Crée une copie d’une structure RepairInfo.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- CopyRepairInfo fonction NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941909"
---
# <a name="copyrepairinfo-function"></a><span data-ttu-id="8ba1b-104">CopyRepairInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="8ba1b-104">CopyRepairInfo function</span></span>

<span data-ttu-id="8ba1b-105">La fonction **CopyRepairInfo** crée une copie d’une structure [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="8ba1b-105">The **CopyRepairInfo** function creates a copy of a [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba1b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ba1b-106">Syntax</span></span>


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="8ba1b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ba1b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba1b-108">*Dest* \[ . à\]</span><span class="sxs-lookup"><span data-stu-id="8ba1b-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba1b-109">Tapez : \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8ba1b-109">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="8ba1b-110">Structure à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="8ba1b-111">_Source \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ba1b-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba1b-112">Type : \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8ba1b-112">Type: \**const [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="8ba1b-113">Structure existante à copier.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba1b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ba1b-114">Return value</span></span>

<span data-ttu-id="8ba1b-115">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="8ba1b-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="8ba1b-116">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="8ba1b-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8ba1b-117">Return code</span></span>                                                                                   | <span data-ttu-id="8ba1b-118">Description</span><span class="sxs-lookup"><span data-stu-id="8ba1b-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ba1b-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1b-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ba1b-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="8ba1b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8ba1b-122">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="8ba1b-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1b-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ba1b-124">La mémoire disponible est insuffisante pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="8ba1b-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ba1b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ba1b-125">Requirements</span></span>



| <span data-ttu-id="8ba1b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ba1b-126">Requirement</span></span> | <span data-ttu-id="8ba1b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ba1b-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba1b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ba1b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba1b-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ba1b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ba1b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ba1b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba1b-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ba1b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8ba1b-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ba1b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ba1b-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ba1b-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ba1b-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ba1b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba1b-135">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="8ba1b-135">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





