---
description: GetCookie n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'IUserIdentity :: GetCookie, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972330"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="5d75f-104">IUserIdentity :: GetCookie, méthode</span><span class="sxs-lookup"><span data-stu-id="5d75f-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="5d75f-105">\[**GetCookie** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="5d75f-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5d75f-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5d75f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5d75f-107">Obtient le cookie utilisé pour identifier de manière unique l’identité de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d75f-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d75f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d75f-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="5d75f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d75f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d75f-110">*puidCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5d75f-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d75f-111">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="5d75f-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="5d75f-112">Pointeur vers une valeur _ *GUID*\* qui reçoit le cookie utilisé pour identifier de manière unique l’identité de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d75f-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d75f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d75f-113">Return value</span></span>

<span data-ttu-id="5d75f-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5d75f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="5d75f-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d75f-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d75f-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d75f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d75f-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5d75f-117">Requirements</span></span>



| <span data-ttu-id="5d75f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d75f-118">Requirement</span></span> | <span data-ttu-id="5d75f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d75f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d75f-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d75f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d75f-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d75f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d75f-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d75f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d75f-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d75f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5d75f-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5d75f-124">End of client support</span></span><br/>    | <span data-ttu-id="5d75f-125">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="5d75f-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5d75f-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5d75f-126">End of server support</span></span><br/>    | <span data-ttu-id="5d75f-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d75f-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5d75f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d75f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d75f-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d75f-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d75f-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="5d75f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d75f-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d75f-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d75f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5d75f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d75f-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d75f-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d75f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d75f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d75f-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="5d75f-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="5d75f-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="5d75f-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




