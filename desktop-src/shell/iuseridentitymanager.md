---
description: IUserIdentityManager n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interface IUserIdentityManager (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861782"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="213a7-104">Interface IUserIdentityManager</span><span class="sxs-lookup"><span data-stu-id="213a7-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="213a7-105">\[**IUserIdentityManager** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="213a7-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="213a7-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="213a7-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="213a7-107">Expose des méthodes qui identifient, énumèrent et gèrent les identités des utilisateurs sur le système.</span><span class="sxs-lookup"><span data-stu-id="213a7-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="213a7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="213a7-108">Members</span></span>

<span data-ttu-id="213a7-109">L’interface **IUserIdentityManager** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="213a7-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="213a7-110">**IUserIdentityManager** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="213a7-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="213a7-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="213a7-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="213a7-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="213a7-112">Methods</span></span>

<span data-ttu-id="213a7-113">L’interface **IUserIdentityManager** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="213a7-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="213a7-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="213a7-114">Method</span></span>                                                                  | <span data-ttu-id="213a7-115">Description</span><span class="sxs-lookup"><span data-stu-id="213a7-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="213a7-116">**EnumIdentities**</span><span class="sxs-lookup"><span data-stu-id="213a7-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="213a7-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="213a7-117">Deprecated.</span></span> <span data-ttu-id="213a7-118">Obtient un objet [**IEnumUserIdentity**](ienumuseridentity.md) , qui peut être utilisé pour énumérer les identités utilisateur présentes sur le système.</span><span class="sxs-lookup"><span data-stu-id="213a7-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="213a7-119">**GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="213a7-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="213a7-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="213a7-120">Deprecated.</span></span> <span data-ttu-id="213a7-121">Obtient une identité d’utilisateur spécifique par le cookie utilisé pour l’identifier de manière unique.</span><span class="sxs-lookup"><span data-stu-id="213a7-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="213a7-122">**Fermeture**</span><span class="sxs-lookup"><span data-stu-id="213a7-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="213a7-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="213a7-123">Deprecated.</span></span> <span data-ttu-id="213a7-124">Déconnectez l’identité actuelle.</span><span class="sxs-lookup"><span data-stu-id="213a7-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="213a7-125">**Horaire**</span><span class="sxs-lookup"><span data-stu-id="213a7-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="213a7-126">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="213a7-126">Deprecated.</span></span> <span data-ttu-id="213a7-127">Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de choisir une identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="213a7-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="213a7-128">En cas de réussite, l’identité de l’utilisateur est connectée et récupérée.</span><span class="sxs-lookup"><span data-stu-id="213a7-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="213a7-129">**ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="213a7-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="213a7-130">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="213a7-130">Deprecated.</span></span> <span data-ttu-id="213a7-131">Affiche une interface utilisateur pour l’utilisateur, ce qui permet à l’utilisateur de gérer les identités des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="213a7-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="213a7-132">Spécifications</span><span class="sxs-lookup"><span data-stu-id="213a7-132">Requirements</span></span>



| <span data-ttu-id="213a7-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="213a7-133">Requirement</span></span> | <span data-ttu-id="213a7-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="213a7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="213a7-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="213a7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="213a7-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="213a7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="213a7-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="213a7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="213a7-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="213a7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="213a7-139">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="213a7-139">End of client support</span></span><br/>    | <span data-ttu-id="213a7-140">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="213a7-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="213a7-141">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="213a7-141">End of server support</span></span><br/>    | <span data-ttu-id="213a7-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="213a7-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="213a7-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="213a7-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="213a7-144"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="213a7-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="213a7-145">MIDL</span><span class="sxs-lookup"><span data-stu-id="213a7-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="213a7-146"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="213a7-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="213a7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="213a7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="213a7-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="213a7-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="213a7-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="213a7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="213a7-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="213a7-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="213a7-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="213a7-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="213a7-152">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="213a7-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="213a7-153">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="213a7-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
