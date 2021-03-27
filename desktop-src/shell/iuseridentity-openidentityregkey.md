---
description: Obsolète. Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity :: OpenIdentityRegKey, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972319"
---
# <a name="iuseridentityopenidentityregkey-method"></a><span data-ttu-id="d785d-104">IUserIdentity :: OpenIdentityRegKey, méthode</span><span class="sxs-lookup"><span data-stu-id="d785d-104">IUserIdentity::OpenIdentityRegKey method</span></span>

<span data-ttu-id="d785d-105">\[La méthode **IUserIdentity :: OpenIdentityRegKey** est disponible pour une utilisation dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d785d-105">\[The **IUserIdentity::OpenIdentityRegKey** method is available for use in Windows 2000.</span></span> <span data-ttu-id="d785d-106">Dans Windows XP, cette fonctionnalité a été remplacée par [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md)et peut être modifiée ou non disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="d785d-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d785d-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d785d-107">Deprecated.</span></span> <span data-ttu-id="d785d-108">Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d785d-108">Retrieves the key in the registry that corresponds to this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="d785d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d785d-109">Syntax</span></span>


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a><span data-ttu-id="d785d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d785d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d785d-111">*dwDesiredAccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d785d-111">*dwDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d785d-112">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d785d-112">Type: **DWORD**</span></span>

<span data-ttu-id="d785d-113">Valeur qui décrit le niveau d’accès demandé pour la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d785d-113">A value that describes the access level requested of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="d785d-114">*phKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d785d-114">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d785d-115">Tapez : \**HKEY \** _</span><span class="sxs-lookup"><span data-stu-id="d785d-115">Type: \**HKEY\** _</span></span>

<span data-ttu-id="d785d-116">Pointeur qui reçoit la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d785d-116">A pointer that receives the registry key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d785d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d785d-117">Return value</span></span>

<span data-ttu-id="d785d-118">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d785d-118">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d785d-119">Résultat de la demande de registre.</span><span class="sxs-lookup"><span data-stu-id="d785d-119">The result of the registry request.</span></span> <span data-ttu-id="d785d-120">En cas de réussite, elle retourne **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d785d-120">If successful, it returns **S\_OK**.</span></span> <span data-ttu-id="d785d-121">Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="d785d-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="d785d-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d785d-122">Return code</span></span>                                                                                            | <span data-ttu-id="d785d-123">Description</span><span class="sxs-lookup"><span data-stu-id="d785d-123">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d785d-124"><dt>**\_identité E \_ \_ introuvable**</dt></span><span class="sxs-lookup"><span data-stu-id="d785d-124"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="d785d-125">Cette identité n’a pas de clé de registre associée.</span><span class="sxs-lookup"><span data-stu-id="d785d-125">This identity does not have an associated registry key.</span></span><br/> |
| <dl> <span data-ttu-id="d785d-126"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d785d-126"><dt>**E\_FAIL**</dt></span></span> </dl>                 | <span data-ttu-id="d785d-127">Impossible d’accéder à la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d785d-127">The registry key was unable to be accessed.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d785d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d785d-128">Remarks</span></span>

<span data-ttu-id="d785d-129">Le paramètre *dwDesiredAccess* est un descripteur de sécurité d’accès au registre standard qui décrit l’accès que vous souhaitez obtenir à la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="d785d-129">The *dwDesiredAccess* parameter is a standard registry access security descriptor that describes the access you want to gain to the registry key.</span></span> <span data-ttu-id="d785d-130">Pour plus d’informations sur la sécurité du Registre, y compris une liste de valeurs acceptables pour ce paramètre, consultez sécurité de la [clé de Registre et droits d’accès](../sysinfo/registry-key-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="d785d-130">For more information on registry security, including a list of acceptable values for this parameter, see [Registry Key Security and Access Rights](../sysinfo/registry-key-security-and-access-rights.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d785d-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d785d-131">Requirements</span></span>



| <span data-ttu-id="d785d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d785d-132">Requirement</span></span> | <span data-ttu-id="d785d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d785d-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d785d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d785d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d785d-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d785d-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d785d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d785d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d785d-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d785d-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d785d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="d785d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d785d-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="d785d-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="d785d-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="d785d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d785d-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d785d-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="d785d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d785d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d785d-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d785d-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d785d-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d785d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d785d-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="d785d-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="d785d-146">**IUserIdentity::GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="d785d-146">**IUserIdentity::GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
