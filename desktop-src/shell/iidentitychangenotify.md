---
description: Obsolète. Fournit une notification des modifications apportées aux identités des utilisateurs sur le système, ainsi que les demandes des utilisateurs pour changer l’identité de l’utilisateur actuel.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interface IIdentityChangeNotify (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202769"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="e798b-104">Interface IIdentityChangeNotify</span><span class="sxs-lookup"><span data-stu-id="e798b-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="e798b-105">\[L’interface **IIdentityChangeNotify** peut être utilisée dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="e798b-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="e798b-106">Dans Windows XP, cette fonctionnalité a été remplacée par [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md)et peut être modifiée ou non disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="e798b-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="e798b-107">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e798b-107">Deprecated.</span></span> <span data-ttu-id="e798b-108">Fournit une notification des modifications apportées aux identités des utilisateurs sur le système, ainsi que les demandes des utilisateurs pour changer l’identité de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="e798b-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="e798b-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e798b-109">Members</span></span>

<span data-ttu-id="e798b-110">L’interface **IIdentityChangeNotify** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e798b-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e798b-111">**IIdentityChangeNotify** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e798b-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="e798b-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e798b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e798b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e798b-113">Methods</span></span>

<span data-ttu-id="e798b-114">L’interface **IIdentityChangeNotify** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e798b-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="e798b-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e798b-115">Method</span></span>                                                                                 | <span data-ttu-id="e798b-116">Description</span><span class="sxs-lookup"><span data-stu-id="e798b-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e798b-117">**IdentityInformationChanged**</span><span class="sxs-lookup"><span data-stu-id="e798b-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="e798b-118">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e798b-118">Deprecated.</span></span> <span data-ttu-id="e798b-119">Appelée lorsque les informations relatives à l’identité d’un utilisateur ont changé ou lorsqu’une identité d’utilisateur a été ajoutée ou supprimée.</span><span class="sxs-lookup"><span data-stu-id="e798b-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="e798b-120">**QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="e798b-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="e798b-121">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e798b-121">Deprecated.</span></span> <span data-ttu-id="e798b-122">Appelé lorsque l’utilisateur actuel a demandé que son identité d’utilisateur soit basculée, mais avant que le commutateur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="e798b-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="e798b-123">**SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="e798b-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="e798b-124">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e798b-124">Deprecated.</span></span> <span data-ttu-id="e798b-125">Appelé lorsque les identités des utilisateurs sont basculées.</span><span class="sxs-lookup"><span data-stu-id="e798b-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="e798b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="e798b-126">Remarks</span></span>

<span data-ttu-id="e798b-127">Pour implémenter des notifications, une interface dérivée doit se connecter au [**IUserIdentityManager**](iuseridentitymanager.md) en appelant [**IConnectionPoint :: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) et en passant un pointeur vers l’interface.</span><span class="sxs-lookup"><span data-stu-id="e798b-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e798b-128">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e798b-128">Requirements</span></span>



| <span data-ttu-id="e798b-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e798b-129">Requirement</span></span> | <span data-ttu-id="e798b-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e798b-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e798b-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e798b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e798b-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e798b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e798b-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e798b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e798b-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e798b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e798b-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="e798b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e798b-136"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="e798b-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e798b-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="e798b-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e798b-138"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e798b-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e798b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e798b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e798b-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e798b-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e798b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e798b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e798b-142">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="e798b-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="e798b-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="e798b-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
