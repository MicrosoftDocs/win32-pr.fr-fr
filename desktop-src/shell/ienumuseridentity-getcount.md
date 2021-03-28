---
description: GetCount n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'IEnumUserIdentity :: GetCount, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319130"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="23707-104">IEnumUserIdentity :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="23707-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="23707-105">\[**GetCount** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="23707-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="23707-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="23707-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="23707-107">Obtient le nombre d’identités d’utilisateur actuellement sur le système.</span><span class="sxs-lookup"><span data-stu-id="23707-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="23707-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23707-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="23707-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23707-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23707-110">*pnCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="23707-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23707-111">Type : \**ULong \** _</span><span class="sxs-lookup"><span data-stu-id="23707-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="23707-112">Pointeur vers un _ *ULong*\* qui reçoit le nombre.</span><span class="sxs-lookup"><span data-stu-id="23707-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23707-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23707-113">Return value</span></span>

<span data-ttu-id="23707-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="23707-114">Type: **HRESULT**</span></span>

<span data-ttu-id="23707-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23707-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23707-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23707-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23707-117">Notes</span><span class="sxs-lookup"><span data-stu-id="23707-117">Remarks</span></span>

<span data-ttu-id="23707-118">Si la prise en charge de plusieurs identités d’utilisateur est désactivée, *pnCount* reçoit la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="23707-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="23707-119">Spécifications</span><span class="sxs-lookup"><span data-stu-id="23707-119">Requirements</span></span>



| <span data-ttu-id="23707-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23707-120">Requirement</span></span> | <span data-ttu-id="23707-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="23707-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23707-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23707-122">Minimum supported client</span></span><br/> | <span data-ttu-id="23707-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23707-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="23707-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23707-124">Minimum supported server</span></span><br/> | <span data-ttu-id="23707-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23707-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23707-126">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="23707-126">End of client support</span></span><br/>    | <span data-ttu-id="23707-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="23707-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="23707-128">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="23707-128">End of server support</span></span><br/>    | <span data-ttu-id="23707-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="23707-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="23707-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="23707-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23707-131"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="23707-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="23707-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="23707-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23707-133"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23707-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="23707-134">DLL</span><span class="sxs-lookup"><span data-stu-id="23707-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23707-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23707-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23707-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23707-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23707-137">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="23707-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="23707-138">**IEnumUserIdentity :: Skip**</span><span class="sxs-lookup"><span data-stu-id="23707-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="23707-139">**IEnumUserIdentity :: Reset**</span><span class="sxs-lookup"><span data-stu-id="23707-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="23707-140">**IEnumUserIdentity :: suivant**</span><span class="sxs-lookup"><span data-stu-id="23707-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




