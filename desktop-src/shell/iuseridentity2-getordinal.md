---
description: GetOrdinal n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'IUserIdentity2 :: GetOrdinal, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973395"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="5360e-104">IUserIdentity2 :: GetOrdinal, méthode</span><span class="sxs-lookup"><span data-stu-id="5360e-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="5360e-105">\[**GetOrdinal** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="5360e-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5360e-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5360e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5360e-107">Obtient le nombre ordinal pour cette identité.</span><span class="sxs-lookup"><span data-stu-id="5360e-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="5360e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5360e-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="5360e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5360e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5360e-110">*dwOrdinal* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5360e-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5360e-111">Type : \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="5360e-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="5360e-112">Pointeur vers une valeur _ *DWORD*\* qui reçoit le nombre ordinal pour cette identité.</span><span class="sxs-lookup"><span data-stu-id="5360e-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5360e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5360e-113">Return value</span></span>

<span data-ttu-id="5360e-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5360e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5360e-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5360e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5360e-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5360e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5360e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5360e-117">Remarks</span></span>

<span data-ttu-id="5360e-118">L’ordinal détermine l’ordre des identités dans la liste d’identités, mais il peut ne pas être persistant dans les opérations sur les identités.</span><span class="sxs-lookup"><span data-stu-id="5360e-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="5360e-119">Pour obtenir une valeur unique pour une identité, appelez [**getCookie**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="5360e-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5360e-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5360e-120">Requirements</span></span>



| <span data-ttu-id="5360e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5360e-121">Requirement</span></span> | <span data-ttu-id="5360e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="5360e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5360e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5360e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5360e-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5360e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5360e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5360e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5360e-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5360e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5360e-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5360e-127">End of client support</span></span><br/>    | <span data-ttu-id="5360e-128">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="5360e-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5360e-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5360e-129">End of server support</span></span><br/>    | <span data-ttu-id="5360e-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5360e-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5360e-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="5360e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5360e-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5360e-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5360e-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="5360e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5360e-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5360e-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5360e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5360e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5360e-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5360e-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5360e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5360e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5360e-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="5360e-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="5360e-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="5360e-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




