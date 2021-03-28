---
description: 'IUserIdentityManager :: ManageIdentities n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'IUserIdentityManager :: ManageIdentities, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317950"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="b51a5-104">IUserIdentityManager :: ManageIdentities, méthode</span><span class="sxs-lookup"><span data-stu-id="b51a5-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="b51a5-105">\[**IUserIdentityManager :: ManageIdentities** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="b51a5-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b51a5-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b51a5-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b51a5-107">Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de gérer les identités des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b51a5-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="b51a5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b51a5-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b51a5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b51a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b51a5-110">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b51a5-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51a5-111">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="b51a5-111">Type: **HWND**</span></span>

<span data-ttu-id="b51a5-112">Valeur **HWND** qui identifie une fenêtre qui sera placée au premier plan après la fermeture de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b51a5-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="b51a5-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b51a5-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b51a5-114">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="b51a5-114">Type: **DWORD**</span></span>

<span data-ttu-id="b51a5-115">Indicateurs facultatifs pour définir le comportement de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b51a5-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="b51a5-116">Définissez sur UIMI \_ créer \_ \_ une identité pour inviter l’utilisateur à créer une nouvelle identité.</span><span class="sxs-lookup"><span data-stu-id="b51a5-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b51a5-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b51a5-117">Return value</span></span>

<span data-ttu-id="b51a5-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b51a5-118">Type: **HRESULT**</span></span>

<span data-ttu-id="b51a5-119">Résultat de l’opération de gestion.</span><span class="sxs-lookup"><span data-stu-id="b51a5-119">The result of the management operation.</span></span> <span data-ttu-id="b51a5-120">En cas de réussite, elle retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b51a5-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="b51a5-121">Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="b51a5-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="b51a5-122">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b51a5-122">Return code</span></span>                                                                                            | <span data-ttu-id="b51a5-123">Description</span><span class="sxs-lookup"><span data-stu-id="b51a5-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="b51a5-124"><dt>**\_identités E \_ désactivées**</dt></span><span class="sxs-lookup"><span data-stu-id="b51a5-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="b51a5-125">La gestion des identités est désactivée sur le système.</span><span class="sxs-lookup"><span data-stu-id="b51a5-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="b51a5-126"><dt>**E \_ utilisateur \_ annulée**</dt></span><span class="sxs-lookup"><span data-stu-id="b51a5-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="b51a5-127">L’utilisateur a annulé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b51a5-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="b51a5-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b51a5-128">Requirements</span></span>



| <span data-ttu-id="b51a5-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b51a5-129">Requirement</span></span> | <span data-ttu-id="b51a5-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="b51a5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b51a5-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51a5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b51a5-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b51a5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b51a5-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b51a5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b51a5-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b51a5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b51a5-135">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b51a5-135">End of client support</span></span><br/>    | <span data-ttu-id="b51a5-136">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="b51a5-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="b51a5-137">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b51a5-137">End of server support</span></span><br/>    | <span data-ttu-id="b51a5-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b51a5-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="b51a5-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="b51a5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="b51a5-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="b51a5-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b51a5-141">MIDL</span><span class="sxs-lookup"><span data-stu-id="b51a5-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b51a5-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b51a5-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b51a5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="b51a5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b51a5-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b51a5-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b51a5-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b51a5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b51a5-146">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="b51a5-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="b51a5-147">**IUserIdentityManager :: Logon**</span><span class="sxs-lookup"><span data-stu-id="b51a5-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="b51a5-148">**IUserIdentityManager :: Logoff**</span><span class="sxs-lookup"><span data-stu-id="b51a5-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




