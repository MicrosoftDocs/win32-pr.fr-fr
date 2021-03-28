---
description: GetIdentityByCookie n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'IUserIdentityManager :: GetIdentityByCookie, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524439"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="8eff6-104">IUserIdentityManager :: GetIdentityByCookie, méthode</span><span class="sxs-lookup"><span data-stu-id="8eff6-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="8eff6-105">\[**GetIdentityByCookie** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="8eff6-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="8eff6-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="8eff6-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="8eff6-107">Obtient une identité d’utilisateur spécifique par le cookie utilisé pour l’identifier de manière unique.</span><span class="sxs-lookup"><span data-stu-id="8eff6-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eff6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8eff6-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="8eff6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8eff6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eff6-110">*uidCookie* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8eff6-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff6-111">Type : \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="8eff6-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="8eff6-112">Adresse d’une valeur _ *GUID*\* qui représente le cookie de l’identité que vous souhaitez récupérer.</span><span class="sxs-lookup"><span data-stu-id="8eff6-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="8eff6-113">*ppIdentity* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8eff6-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8eff6-114">Type : **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="8eff6-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="8eff6-115">Adresse du pointeur qui recevra l’objet d’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8eff6-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eff6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8eff6-116">Return value</span></span>

<span data-ttu-id="8eff6-117">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8eff6-117">Type: **HRESULT**</span></span>

<span data-ttu-id="8eff6-118">Résultat de la requête de récupération.</span><span class="sxs-lookup"><span data-stu-id="8eff6-118">The result of the retrieval request.</span></span> <span data-ttu-id="8eff6-119">En cas de réussite, elle retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8eff6-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="8eff6-120">Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="8eff6-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="8eff6-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8eff6-121">Return code</span></span>                                                                                            | <span data-ttu-id="8eff6-122">Description</span><span class="sxs-lookup"><span data-stu-id="8eff6-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="8eff6-123"><dt>**\_identité E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="8eff6-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="8eff6-124">L’identité demandée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8eff6-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="8eff6-125"><dt>**\_identités E \_ désactivées**</dt></span><span class="sxs-lookup"><span data-stu-id="8eff6-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="8eff6-126">La gestion des identités est désactivée sur le système.</span><span class="sxs-lookup"><span data-stu-id="8eff6-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8eff6-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8eff6-127">Requirements</span></span>



| <span data-ttu-id="8eff6-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8eff6-128">Requirement</span></span> | <span data-ttu-id="8eff6-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8eff6-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eff6-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8eff6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="8eff6-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8eff6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8eff6-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8eff6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="8eff6-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8eff6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8eff6-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="8eff6-134">End of client support</span></span><br/>    | <span data-ttu-id="8eff6-135">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="8eff6-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="8eff6-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="8eff6-136">End of server support</span></span><br/>    | <span data-ttu-id="8eff6-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8eff6-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="8eff6-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="8eff6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eff6-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eff6-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="8eff6-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="8eff6-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8eff6-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8eff6-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="8eff6-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8eff6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8eff6-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8eff6-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




