---
description: 'WMI a des constantes de sécurité utilisées pour la vérification de l’accès aux espaces de noms par \_ \_ SystemSecurity :: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de droits d’accès à l’espace de noms (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033838"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="f9e6c-103">Constantes de droits d’accès à l’espace de noms</span><span class="sxs-lookup"><span data-stu-id="f9e6c-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="f9e6c-104">WMI a des constantes de sécurité utilisées pour la vérification de l’accès aux espaces de noms par [**\_ \_ SystemSecurity :: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6c-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="f9e6c-105">Pour obtenir des informations de sécurité sur les listes de contrôle d’accès (ACL, DACL ou SACL), consultez [listes de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) et [**droits d’accès standard**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="f9e6c-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="f9e6c-106">Ces constantes sont définies dans l’énumération des **\_ \_ indicateurs de sécurité WBEM** .</span><span class="sxs-lookup"><span data-stu-id="f9e6c-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="f9e6c-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**\_activation WBEM**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-109">Active le compte et accorde des autorisations de lecture à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="f9e6c-110">Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation activer le compte sous l’onglet sécurité du [*contrôle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6c-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="f9e6c-111">Pour plus d’informations, consultez [définition de la sécurité de l’espace de noms avec le contrôle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6c-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9e6c-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**exécution de la \_ méthode WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-113">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-114">Autorise l’exécution des méthodes.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-114">Allows the execution of methods.</span></span> <span data-ttu-id="f9e6c-115">Les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="f9e6c-116">Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation exécuter les méthodes sur l’onglet sécurité du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9e6c-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_REP en \_ écriture \_ complète WBEM**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-119">Permet à un compte d’utilisateur d’écrire dans des classes du référentiel WMI, ainsi que des instances.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="f9e6c-120">Un utilisateur ne peut pas écrire dans les classes système.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-120">A user cannot write to system classes.</span></span> <span data-ttu-id="f9e6c-121">Seuls les membres du groupe administrateurs ont cette autorisation.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="f9e6c-122">**WBEM \_ Le \_ \_ REP en écriture complète** correspond à l’autorisation en écriture complète sur l’onglet sécurité du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9e6c-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_REP- \_ écriture \_ partielle WBEM**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-125">Vous permet d’écrire des données uniquement dans des instances, et non dans des classes.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="f9e6c-126">Un utilisateur ne peut pas écrire des classes dans l' [*espace de stockage WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="f9e6c-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="f9e6c-127">Seuls les membres du groupe administrateurs disposent de ce droit.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="f9e6c-128">**WBEM \_ Le \_ \_ REP en écriture partielle** correspond à l’autorisation écriture partielle sur l’onglet sécurité du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9e6c-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_fournisseur d’écriture WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-131">Permet d’écrire des classes et des instances pour les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="f9e6c-132">Notez que les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires lorsqu’ils empruntent l’identité d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="f9e6c-133">Il s’agit d’un droit d’accès par défaut pour tous les utilisateurs et correspond à l’autorisation d’écriture du fournisseur sur l’onglet sécurité du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f9e6c-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_accès à distance WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="f9e6c-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9e6c-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="f9e6c-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="f9e6c-136">Permet à un compte d’utilisateur d’effectuer à distance les opérations autorisées par les autorisations décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="f9e6c-137">Seuls les membres du groupe administrateurs disposent de ce droit.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="f9e6c-138">**WBEM \_ L' \_ accès à distance** correspond à l’autorisation activation à distance sur l’onglet sécurité du contrôle WMI.</span><span class="sxs-lookup"><span data-stu-id="f9e6c-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f9e6c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9e6c-139">Requirements</span></span>



| <span data-ttu-id="f9e6c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9e6c-140">Requirement</span></span> | <span data-ttu-id="f9e6c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9e6c-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e6c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9e6c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e6c-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9e6c-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="f9e6c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9e6c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e6c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9e6c-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="f9e6c-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9e6c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e6c-147"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e6c-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e6c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9e6c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e6c-149">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="f9e6c-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="f9e6c-150">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="f9e6c-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="f9e6c-151">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="f9e6c-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="f9e6c-152">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="f9e6c-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="f9e6c-153">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="f9e6c-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

