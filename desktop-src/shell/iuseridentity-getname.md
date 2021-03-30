---
description: 'IUserIdentity :: GetName n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'IUserIdentity :: GetName, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973115"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="49182-104">IUserIdentity :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="49182-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="49182-105">\[**IUserIdentity :: GetName** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="49182-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="49182-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="49182-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="49182-107">Obtient le nom associé à cette identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49182-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="49182-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49182-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="49182-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49182-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49182-110">*pszName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49182-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49182-111">Type : \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="49182-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="49182-112">Pointeur vers une chaîne de caractères larges qui reçoit le nom de cette identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49182-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="49182-113">_ulBuffSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49182-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49182-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="49182-114">Type: **ULONG**</span></span>

<span data-ttu-id="49182-115">Valeur qui spécifie la taille de *pszName*.</span><span class="sxs-lookup"><span data-stu-id="49182-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49182-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49182-116">Return value</span></span>

<span data-ttu-id="49182-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="49182-117">Type: **HRESULT**</span></span>

<span data-ttu-id="49182-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="49182-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="49182-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="49182-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="49182-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="49182-120">Requirements</span></span>



| <span data-ttu-id="49182-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49182-121">Requirement</span></span> | <span data-ttu-id="49182-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="49182-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49182-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49182-123">Minimum supported client</span></span><br/> | <span data-ttu-id="49182-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49182-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="49182-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49182-125">Minimum supported server</span></span><br/> | <span data-ttu-id="49182-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49182-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="49182-127">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="49182-127">End of client support</span></span><br/>    | <span data-ttu-id="49182-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="49182-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="49182-129">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="49182-129">End of server support</span></span><br/>    | <span data-ttu-id="49182-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="49182-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="49182-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="49182-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="49182-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="49182-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="49182-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="49182-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="49182-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="49182-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="49182-135">DLL</span><span class="sxs-lookup"><span data-stu-id="49182-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49182-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49182-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49182-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49182-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49182-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="49182-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="49182-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="49182-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




