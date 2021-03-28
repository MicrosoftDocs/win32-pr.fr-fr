---
description: 'IUserIdentityManager :: Logon n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'IUserIdentityManager :: Logon, méthode (msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111714"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="5872c-104">IUserIdentityManager :: Logon, méthode</span><span class="sxs-lookup"><span data-stu-id="5872c-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="5872c-105">\[**IUserIdentityManager :: Logon** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="5872c-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="5872c-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="5872c-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="5872c-107">Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de choisir une identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5872c-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="5872c-108">En cas de réussite, l’identité de l’utilisateur est connectée et récupérée.</span><span class="sxs-lookup"><span data-stu-id="5872c-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="5872c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5872c-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="5872c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5872c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5872c-111">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5872c-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5872c-112">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="5872c-112">Type: **HWND**</span></span>

<span data-ttu-id="5872c-113">Valeur **HWND** qui identifie une fenêtre qui sera placée au premier plan après la fermeture de l’interface utilisateur d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="5872c-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="5872c-114">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5872c-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5872c-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="5872c-115">Type: **DWORD**</span></span>

<span data-ttu-id="5872c-116">Indicateurs facultatifs pour définir le comportement de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5872c-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="5872c-117">Définissez sur UIL \_ force \_ UI pour forcer l’affichage de l’interface utilisateur, même si une identité a déjà été choisie.</span><span class="sxs-lookup"><span data-stu-id="5872c-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="5872c-118">*ppIdentity* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5872c-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5872c-119">Type : **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5872c-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="5872c-120">Adresse du pointeur qui reçoit l’identité de l’utilisateur choisi.</span><span class="sxs-lookup"><span data-stu-id="5872c-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5872c-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5872c-121">Return value</span></span>

<span data-ttu-id="5872c-122">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5872c-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5872c-123">Résultat de l’opération d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="5872c-123">Result of the logon operation.</span></span> <span data-ttu-id="5872c-124">En cas de réussite, elle retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5872c-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="5872c-125">Dans le cas contraire, elle renverra l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="5872c-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="5872c-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5872c-126">Return code</span></span>                                                                                            | <span data-ttu-id="5872c-127">Description</span><span class="sxs-lookup"><span data-stu-id="5872c-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5872c-128"><dt>**E \_ utilisateur \_ annulée**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="5872c-129">L’utilisateur a annulé l’opération de connexion à partir de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5872c-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="5872c-130"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="5872c-131">Impossible de créer l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5872c-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="5872c-132"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="5872c-133">L’opération a échoué de façon inattendue.</span><span class="sxs-lookup"><span data-stu-id="5872c-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="5872c-134"><dt>**\_identités E \_ désactivées**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="5872c-135">La gestion des identités est désactivée sur le système.</span><span class="sxs-lookup"><span data-stu-id="5872c-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5872c-136"><dt>**\_identités de S \_ désactivées**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="5872c-137">La gestion des identités est désactivée sur le système.</span><span class="sxs-lookup"><span data-stu-id="5872c-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="5872c-138"><dt>**modification de l' \_ identité E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="5872c-139">Le système bascule actuellement les identités et ne peut pas terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="5872c-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5872c-140">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5872c-140">Requirements</span></span>



| <span data-ttu-id="5872c-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5872c-141">Requirement</span></span> | <span data-ttu-id="5872c-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="5872c-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5872c-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5872c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5872c-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5872c-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5872c-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5872c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5872c-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5872c-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5872c-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="5872c-147">End of client support</span></span><br/>    | <span data-ttu-id="5872c-148">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="5872c-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="5872c-149">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="5872c-149">End of server support</span></span><br/>    | <span data-ttu-id="5872c-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5872c-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="5872c-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="5872c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="5872c-152"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="5872c-153">MIDL</span><span class="sxs-lookup"><span data-stu-id="5872c-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5872c-154"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="5872c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5872c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5872c-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5872c-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5872c-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5872c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5872c-158">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="5872c-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="5872c-159">**IUserIdentityManager :: Logoff**</span><span class="sxs-lookup"><span data-stu-id="5872c-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="5872c-160">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="5872c-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




