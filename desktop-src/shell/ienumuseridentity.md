---
description: IEnumUserIdentity n’est pas pris en charge et peut être modifié ou non disponible à l’avenir. Utilisez plutôt des comptes d’utilisateur avec changement rapide d’utilisateur et Bureau à distance.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interface IEnumUserIdentity (msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973123"
---
# <a name="ienumuseridentity-interface"></a><span data-ttu-id="7051e-104">Interface IEnumUserIdentity</span><span class="sxs-lookup"><span data-stu-id="7051e-104">IEnumUserIdentity interface</span></span>

<span data-ttu-id="7051e-105">\[**IEnumUserIdentity** n’est pas pris en charge et peut être modifié ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="7051e-105">\[**IEnumUserIdentity** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7051e-106">Utilisez plutôt [des comptes d’utilisateur avec changement rapide d’utilisateur et bureau à distance](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7051e-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7051e-107">Fournit l’énumération de toutes les identités d’utilisateur présentes sur le système.</span><span class="sxs-lookup"><span data-stu-id="7051e-107">Provides enumeration of all user identities present on the system.</span></span>

## <a name="members"></a><span data-ttu-id="7051e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7051e-108">Members</span></span>

<span data-ttu-id="7051e-109">L’interface **IEnumUserIdentity** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7051e-109">The **IEnumUserIdentity** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7051e-110">**IEnumUserIdentity** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7051e-110">**IEnumUserIdentity** also has these types of members:</span></span>

-   [<span data-ttu-id="7051e-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7051e-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7051e-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7051e-112">Methods</span></span>

<span data-ttu-id="7051e-113">L’interface **IEnumUserIdentity** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7051e-113">The **IEnumUserIdentity** interface has these methods.</span></span>



| <span data-ttu-id="7051e-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="7051e-114">Method</span></span>                                         | <span data-ttu-id="7051e-115">Description</span><span class="sxs-lookup"><span data-stu-id="7051e-115">Description</span></span>                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7051e-116">**Clone**</span><span class="sxs-lookup"><span data-stu-id="7051e-116">**Clone**</span></span>](ienumuseridentity-clone.md)       | <span data-ttu-id="7051e-117">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7051e-117">Deprecated.</span></span> <span data-ttu-id="7051e-118">Obtient une copie de l’énumération actuelle.</span><span class="sxs-lookup"><span data-stu-id="7051e-118">Gets a copy of the current enumeration.</span></span><br/>                                                               |
| [<span data-ttu-id="7051e-119">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="7051e-119">**GetCount**</span></span>](ienumuseridentity-getcount.md) | <span data-ttu-id="7051e-120">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7051e-120">Deprecated.</span></span> <span data-ttu-id="7051e-121">Obtient le nombre d’identités d’utilisateur actuellement sur le système.</span><span class="sxs-lookup"><span data-stu-id="7051e-121">Gets the count of user identities currently on the system.</span></span><br/>                                            |
| [<span data-ttu-id="7051e-122">**Suivant**</span><span class="sxs-lookup"><span data-stu-id="7051e-122">**Next**</span></span>](ienumuseridentity-next.md)         | <span data-ttu-id="7051e-123">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7051e-123">Deprecated.</span></span> <span data-ttu-id="7051e-124">Récupère un tableau d’interfaces d’identité d’utilisateur à partir de l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7051e-124">Retrieves an array of user identity interfaces from the enumeration.</span></span><br/>                                  |
| [<span data-ttu-id="7051e-125">**Réinitialiser**</span><span class="sxs-lookup"><span data-stu-id="7051e-125">**Reset**</span></span>](ienumuseridentity-reset.md)       | <span data-ttu-id="7051e-126">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7051e-126">Deprecated.</span></span> <span data-ttu-id="7051e-127">Réinitialise le nombre interne d’interfaces récupérées dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7051e-127">Resets the internal count of retrieved interfaces in the enumeration.</span></span><br/>                                 |
| [<span data-ttu-id="7051e-128">**Saut**</span><span class="sxs-lookup"><span data-stu-id="7051e-128">**Skip**</span></span>](ienumuseridentity-skip.md)         | <span data-ttu-id="7051e-129">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7051e-129">Deprecated.</span></span> <span data-ttu-id="7051e-130">Ignore un nombre donné d’interfaces d’identité utilisateur dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="7051e-130">Skips a given number of user identity interfaces in the enumeration.</span></span> <span data-ttu-id="7051e-131">Utilisé lors de la récupération des interfaces.</span><span class="sxs-lookup"><span data-stu-id="7051e-131">Used when retrieving interfaces.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7051e-132">Notes</span><span class="sxs-lookup"><span data-stu-id="7051e-132">Remarks</span></span>

<span data-ttu-id="7051e-133">Pour récupérer des informations sur les identités des utilisateurs présentes sur le système, vous pouvez utiliser cette interface.</span><span class="sxs-lookup"><span data-stu-id="7051e-133">To retrieve information about user identities present on the system, you can use this interface.</span></span> <span data-ttu-id="7051e-134">À partir d’une interface [**IUserIdentityManager**](iuseridentitymanager.md) , vous pouvez appeler [**IUserIdentityManager :: EnumIdentities**](iuseridentitymanager-enumidentities.md) pour récupérer cette interface.</span><span class="sxs-lookup"><span data-stu-id="7051e-134">From a [**IUserIdentityManager**](iuseridentitymanager.md) interface, you can call [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) to retrieve this interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="7051e-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="7051e-135">Requirements</span></span>



| <span data-ttu-id="7051e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7051e-136">Requirement</span></span> | <span data-ttu-id="7051e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="7051e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7051e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7051e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7051e-139">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7051e-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7051e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7051e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7051e-141">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7051e-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7051e-142">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="7051e-142">End of client support</span></span><br/>    | <span data-ttu-id="7051e-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7051e-143">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="7051e-144">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="7051e-144">End of server support</span></span><br/>    | <span data-ttu-id="7051e-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7051e-145">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="7051e-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="7051e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="7051e-147"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7051e-147"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7051e-148">MIDL</span><span class="sxs-lookup"><span data-stu-id="7051e-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7051e-149"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7051e-149"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7051e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7051e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7051e-151"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7051e-151"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7051e-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7051e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7051e-153">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="7051e-153">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> </dl>

 

 
