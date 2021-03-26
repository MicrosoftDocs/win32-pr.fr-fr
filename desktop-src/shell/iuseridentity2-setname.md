---
description: 'IUserIdentity2 :: SetName n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'IUserIdentity2 :: SetName, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973391"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="0ef88-104">IUserIdentity2 :: SetName, méthode</span><span class="sxs-lookup"><span data-stu-id="0ef88-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="0ef88-105">\[**IUserIdentity2 :: SetName** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0ef88-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0ef88-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="0ef88-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="0ef88-107">Définit le nom d’affichage de l’identité.</span><span class="sxs-lookup"><span data-stu-id="0ef88-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ef88-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ef88-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="0ef88-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ef88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ef88-110">*pszName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0ef88-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ef88-111">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="0ef88-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="0ef88-112">Chaîne de caractères larges qui contient le nouveau nom de l’identité.</span><span class="sxs-lookup"><span data-stu-id="0ef88-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ef88-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ef88-113">Return value</span></span>

<span data-ttu-id="0ef88-114">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0ef88-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0ef88-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0ef88-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0ef88-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ef88-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef88-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ef88-117">Requirements</span></span>



| <span data-ttu-id="0ef88-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ef88-118">Requirement</span></span> | <span data-ttu-id="0ef88-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ef88-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef88-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef88-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef88-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ef88-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ef88-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef88-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef88-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ef88-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0ef88-124">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0ef88-124">End of client support</span></span><br/>    | <span data-ttu-id="0ef88-125">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="0ef88-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="0ef88-126">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0ef88-126">End of server support</span></span><br/>    | <span data-ttu-id="0ef88-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0ef88-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="0ef88-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ef88-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef88-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef88-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ef88-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="0ef88-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ef88-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ef88-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0ef88-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0ef88-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ef88-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ef88-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef88-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ef88-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef88-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="0ef88-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="0ef88-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="0ef88-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




