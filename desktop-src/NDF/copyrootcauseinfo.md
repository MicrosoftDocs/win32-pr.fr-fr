---
title: CopyRootCauseInfo, fonction (Ndattributils. h)
description: Crée une copie d’une structure RootCauseInfo.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- CopyRootCauseInfo fonction NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941910"
---
# <a name="copyrootcauseinfo-function"></a><span data-ttu-id="3235c-104">CopyRootCauseInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="3235c-104">CopyRootCauseInfo function</span></span>

<span data-ttu-id="3235c-105">La fonction **CopyRootCauseInfo** crée une copie d’une structure [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="3235c-105">The **CopyRootCauseInfo** function creates a copy of a [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3235c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3235c-106">Syntax</span></span>


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a><span data-ttu-id="3235c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3235c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3235c-108">*Dest* \[ . à\]</span><span class="sxs-lookup"><span data-stu-id="3235c-108">*Dest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3235c-109">Tapez : \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3235c-109">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="3235c-110">Structure à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="3235c-110">The structure to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="3235c-111">_Source \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3235c-111">_Source\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3235c-112">Type : \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="3235c-112">Type: \**const [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="3235c-113">Structure existante à copier.</span><span class="sxs-lookup"><span data-stu-id="3235c-113">The existing structure to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3235c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3235c-114">Return value</span></span>

<span data-ttu-id="3235c-115">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3235c-115">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3235c-116">Les valeurs de retour possibles incluent, mais ne sont pas limitées à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="3235c-116">Possible return values include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3235c-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3235c-117">Return code</span></span>                                                                                   | <span data-ttu-id="3235c-118">Description</span><span class="sxs-lookup"><span data-stu-id="3235c-118">Description</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3235c-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3235c-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3235c-120">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3235c-120">The operation succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="3235c-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3235c-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3235c-122">Un ou plusieurs paramètres n’ont pas été fournis correctement.</span><span class="sxs-lookup"><span data-stu-id="3235c-122">One or more parameters has not been provided correctly.</span></span><br/>          |
| <dl> <span data-ttu-id="3235c-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3235c-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3235c-124">La mémoire disponible est insuffisante pour terminer cette opération.</span><span class="sxs-lookup"><span data-stu-id="3235c-124">There is not enough memory available to complete this operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3235c-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3235c-125">Requirements</span></span>



| <span data-ttu-id="3235c-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3235c-126">Requirement</span></span> | <span data-ttu-id="3235c-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="3235c-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3235c-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3235c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3235c-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3235c-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3235c-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3235c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3235c-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3235c-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3235c-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3235c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3235c-133"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="3235c-133"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3235c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3235c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3235c-135">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="3235c-135">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





