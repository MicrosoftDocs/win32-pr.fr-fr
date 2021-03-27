---
description: La fermeture de session n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'IUserIdentityManager :: Logoff, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971867"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="0c40b-104">IUserIdentityManager :: Logoff, méthode</span><span class="sxs-lookup"><span data-stu-id="0c40b-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="0c40b-105">\[La **fermeture de session** n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="0c40b-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="0c40b-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="0c40b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="0c40b-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0c40b-107">Deprecated.</span></span> <span data-ttu-id="0c40b-108">Déconnectez l’identité actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c40b-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c40b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c40b-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="0c40b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c40b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c40b-111">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0c40b-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c40b-112">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="0c40b-112">Type: **HWND**</span></span>

<span data-ttu-id="0c40b-113">Valeur **HWND** qui identifie une fenêtre qui sera placée au premier plan lorsque la déconnexion est terminée.</span><span class="sxs-lookup"><span data-stu-id="0c40b-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c40b-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c40b-114">Return value</span></span>

<span data-ttu-id="0c40b-115">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c40b-115">Type: **HRESULT**</span></span>

<span data-ttu-id="0c40b-116">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0c40b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0c40b-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c40b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c40b-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0c40b-118">Requirements</span></span>



| <span data-ttu-id="0c40b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c40b-119">Requirement</span></span> | <span data-ttu-id="0c40b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c40b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c40b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c40b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c40b-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c40b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0c40b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c40b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c40b-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c40b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0c40b-125">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0c40b-125">End of client support</span></span><br/>    | <span data-ttu-id="0c40b-126">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="0c40b-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="0c40b-127">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="0c40b-127">End of server support</span></span><br/>    | <span data-ttu-id="0c40b-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c40b-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="0c40b-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c40b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c40b-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c40b-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c40b-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="0c40b-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c40b-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c40b-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0c40b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0c40b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c40b-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c40b-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c40b-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c40b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c40b-136">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="0c40b-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="0c40b-137">**IUserIdentityManager :: Logon**</span><span class="sxs-lookup"><span data-stu-id="0c40b-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="0c40b-138">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="0c40b-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




