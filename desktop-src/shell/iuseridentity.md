---
description: IUserIdentity n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interface IUserIdentity (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973114"
---
# <a name="iuseridentity-interface"></a><span data-ttu-id="aa2b0-104">Interface IUserIdentity</span><span class="sxs-lookup"><span data-stu-id="aa2b0-104">IUserIdentity interface</span></span>

<span data-ttu-id="aa2b0-105">\[**IUserIdentity** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-105">\[**IUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="aa2b0-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="aa2b0-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="aa2b0-107">Expose des méthodes qui fournissent des données d’identification, de Registre et de dossier pour une identité d’utilisateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-107">Exposes methods that provide identification, registry, and folder data for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="aa2b0-108">Membres</span><span class="sxs-lookup"><span data-stu-id="aa2b0-108">Members</span></span>

<span data-ttu-id="aa2b0-109">L’interface **IUserIdentity** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aa2b0-109">The **IUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aa2b0-110">**IUserIdentity** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="aa2b0-110">**IUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="aa2b0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aa2b0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aa2b0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aa2b0-112">Methods</span></span>

<span data-ttu-id="aa2b0-113">L’interface **IUserIdentity** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-113">The **IUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="aa2b0-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="aa2b0-114">Method</span></span>                                                         | <span data-ttu-id="aa2b0-115">Description</span><span class="sxs-lookup"><span data-stu-id="aa2b0-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa2b0-116">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-116">**GetCookie**</span></span>](iuseridentity-getcookie.md)                   | <span data-ttu-id="aa2b0-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-117">Deprecated.</span></span> <span data-ttu-id="aa2b0-118">Obtient le cookie utilisé pour identifier de manière unique l’identité de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-118">Gets the cookie used to uniquely identify this user identity.</span></span><br/>             |
| [<span data-ttu-id="aa2b0-119">**GetIdentityFolder**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-119">**GetIdentityFolder**</span></span>](iuseridentity-getidentityfolder.md)   | <span data-ttu-id="aa2b0-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-120">Deprecated.</span></span> <span data-ttu-id="aa2b0-121">Obtient le dossier de fichiers associé à cette identité.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-121">Gets the file folder associated with this identity.</span></span><br/>                       |
| [<span data-ttu-id="aa2b0-122">**GetName**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-122">**GetName**</span></span>](iuseridentity-getname.md)                       | <span data-ttu-id="aa2b0-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-123">Deprecated.</span></span> <span data-ttu-id="aa2b0-124">Obtient le nom associé à cette identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-124">Gets the name associated with this user identity.</span></span><br/>                         |
| [<span data-ttu-id="aa2b0-125">**OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-125">**OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md) | <span data-ttu-id="aa2b0-126">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-126">Deprecated.</span></span> <span data-ttu-id="aa2b0-127">Récupère la clé dans le Registre qui correspond à l’identité de cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-127">Retrieves the key in the registry that corresponds to this user identity.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa2b0-128">Notes</span><span class="sxs-lookup"><span data-stu-id="aa2b0-128">Remarks</span></span>

<span data-ttu-id="aa2b0-129">Cette interface fournit des informations qui correspondent à une identité d’utilisateur spécifique présente sur le système.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-129">This interface provides information that corresponds to a specific user identity present on the system.</span></span> <span data-ttu-id="aa2b0-130">Vous pouvez accéder au dossier d’identité de l’identité de cet utilisateur, à sa clé de Registre et à son cookie d’identification, ainsi qu’à récupérer le nom associé à l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa2b0-130">You can access this user identity's identity folder, its registry key, and its identification cookie, as well as retrieve the name associated with the user identity.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa2b0-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="aa2b0-131">Requirements</span></span>



| <span data-ttu-id="aa2b0-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aa2b0-132">Requirement</span></span> | <span data-ttu-id="aa2b0-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa2b0-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa2b0-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa2b0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="aa2b0-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa2b0-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="aa2b0-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="aa2b0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="aa2b0-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="aa2b0-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aa2b0-138">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="aa2b0-138">End of client support</span></span><br/>    | <span data-ttu-id="aa2b0-139">Windows 2000 Professionnel</span><span class="sxs-lookup"><span data-stu-id="aa2b0-139">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="aa2b0-140">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="aa2b0-140">End of server support</span></span><br/>    | <span data-ttu-id="aa2b0-141">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="aa2b0-141">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="aa2b0-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="aa2b0-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa2b0-143"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa2b0-143"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa2b0-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="aa2b0-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa2b0-145"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa2b0-145"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa2b0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="aa2b0-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa2b0-147"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa2b0-147"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa2b0-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aa2b0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2b0-149">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-149">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="aa2b0-150">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-150">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="aa2b0-151">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="aa2b0-151">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> </dl>

 

 
