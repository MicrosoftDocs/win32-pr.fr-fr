---
description: 'IUserIdentityManager :: EnumIdentities n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager :: EnumIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111718"
---
# <a name="iuseridentitymanagerenumidentities-method"></a><span data-ttu-id="f62eb-104">IUserIdentityManager :: EnumIdentities, méthode</span><span class="sxs-lookup"><span data-stu-id="f62eb-104">IUserIdentityManager::EnumIdentities method</span></span>

<span data-ttu-id="f62eb-105">\[**IUserIdentityManager :: EnumIdentities** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="f62eb-105">\[**IUserIdentityManager::EnumIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="f62eb-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="f62eb-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="f62eb-107">Obtient un objet [**IEnumUserIdentity**](ienumuseridentity.md) , qui peut être utilisé pour énumérer les identités utilisateur présentes sur le système.</span><span class="sxs-lookup"><span data-stu-id="f62eb-107">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f62eb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f62eb-108">Syntax</span></span>


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a><span data-ttu-id="f62eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f62eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f62eb-110">*ppEnumUser* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f62eb-110">*ppEnumUser* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f62eb-111">Type : **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f62eb-111">Type: **[**IEnumUserIdentity**](ienumuseridentity.md)\*\***</span></span>

<span data-ttu-id="f62eb-112">Adresse du pointeur vers le nouvel objet d’énumération d’identité.</span><span class="sxs-lookup"><span data-stu-id="f62eb-112">The address of the pointer to the new identity enumeration object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f62eb-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f62eb-113">Return value</span></span>

<span data-ttu-id="f62eb-114">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f62eb-114">Type: **HRESULT**</span></span>

<span data-ttu-id="f62eb-115">Résultat de l’opération de récupération.</span><span class="sxs-lookup"><span data-stu-id="f62eb-115">The result of the retrieval operation.</span></span> <span data-ttu-id="f62eb-116">En cas de réussite, elle retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f62eb-116">If successful, it returns S\_OK.</span></span> <span data-ttu-id="f62eb-117">Si l’objet d’énumération n’a pas pu être créé, il retourne E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="f62eb-117">If the enumeration object could not be created, it returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f62eb-118">Notes</span><span class="sxs-lookup"><span data-stu-id="f62eb-118">Remarks</span></span>

<span data-ttu-id="f62eb-119">Cette méthode est utile pour les itérations sur la liste des identités sur le système.</span><span class="sxs-lookup"><span data-stu-id="f62eb-119">This method is useful for iteration over the list of identities on the system.</span></span> <span data-ttu-id="f62eb-120">Pour récupérer une identité unique par son cookie sans accéder à la liste, appelez [**IUserIdentityManager :: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span><span class="sxs-lookup"><span data-stu-id="f62eb-120">To retrieve a single identity by its cookie without accessing the list, call [**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f62eb-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="f62eb-121">Requirements</span></span>



| <span data-ttu-id="f62eb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f62eb-122">Requirement</span></span> | <span data-ttu-id="f62eb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f62eb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f62eb-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f62eb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f62eb-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f62eb-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f62eb-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f62eb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f62eb-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f62eb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f62eb-128">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f62eb-128">End of client support</span></span><br/>    | <span data-ttu-id="f62eb-129">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="f62eb-129">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="f62eb-130">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f62eb-130">End of server support</span></span><br/>    | <span data-ttu-id="f62eb-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f62eb-131">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="f62eb-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="f62eb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f62eb-133"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62eb-133"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="f62eb-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="f62eb-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f62eb-135"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f62eb-135"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="f62eb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f62eb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f62eb-137"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f62eb-137"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62eb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f62eb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62eb-139">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="f62eb-139">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="f62eb-140">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="f62eb-140">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="f62eb-141">**IUserIdentityManager::GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="f62eb-141">**IUserIdentityManager::GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




