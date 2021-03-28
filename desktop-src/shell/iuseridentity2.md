---
description: IUserIdentity2 n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interface IUserIdentity2 (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524444"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="54595-104">Interface IUserIdentity2</span><span class="sxs-lookup"><span data-stu-id="54595-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="54595-105">\[**IUserIdentity2** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="54595-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="54595-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="54595-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="54595-107">Expose des méthodes qui fournissent la dénomination, le mot de passe et le contrôle ordinal pour une identité d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="54595-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="54595-108">Membres</span><span class="sxs-lookup"><span data-stu-id="54595-108">Members</span></span>

<span data-ttu-id="54595-109">L’interface **IUserIdentity2** hérite de [**IUserIdentity**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="54595-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="54595-110">**IUserIdentity2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="54595-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="54595-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54595-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54595-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="54595-112">Methods</span></span>

<span data-ttu-id="54595-113">L’interface **IUserIdentity2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="54595-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="54595-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="54595-114">Method</span></span>                                                  | <span data-ttu-id="54595-115">Description</span><span class="sxs-lookup"><span data-stu-id="54595-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="54595-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="54595-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="54595-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="54595-117">Deprecated.</span></span> <span data-ttu-id="54595-118">Définit un nouveau mot de passe pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="54595-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="54595-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="54595-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="54595-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="54595-120">Deprecated.</span></span> <span data-ttu-id="54595-121">Obtient le nombre ordinal pour cette identité.</span><span class="sxs-lookup"><span data-stu-id="54595-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="54595-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="54595-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="54595-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="54595-123">Deprecated.</span></span> <span data-ttu-id="54595-124">Définit le nom d’affichage de l’identité.</span><span class="sxs-lookup"><span data-stu-id="54595-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="54595-125">Notes</span><span class="sxs-lookup"><span data-stu-id="54595-125">Remarks</span></span>

<span data-ttu-id="54595-126">Cette interface fournit également les méthodes de l’interface [**IUserIdentity**](iuseridentity.md) , dont elle hérite.</span><span class="sxs-lookup"><span data-stu-id="54595-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="54595-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54595-127">Requirements</span></span>



| <span data-ttu-id="54595-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54595-128">Requirement</span></span> | <span data-ttu-id="54595-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="54595-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54595-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54595-130">Minimum supported client</span></span><br/> | <span data-ttu-id="54595-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54595-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="54595-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54595-132">Minimum supported server</span></span><br/> | <span data-ttu-id="54595-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54595-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54595-134">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="54595-134">End of client support</span></span><br/>    | <span data-ttu-id="54595-135">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="54595-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="54595-136">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="54595-136">End of server support</span></span><br/>    | <span data-ttu-id="54595-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="54595-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="54595-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="54595-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="54595-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="54595-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="54595-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="54595-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54595-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54595-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="54595-142">DLL</span><span class="sxs-lookup"><span data-stu-id="54595-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54595-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54595-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54595-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54595-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54595-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="54595-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




