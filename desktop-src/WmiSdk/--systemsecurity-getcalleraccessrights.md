---
description: Définit le paramètre rights en tant que bitmap avec chaque bit correspondant à un droit d’accès.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Méthode GetCallerAccessRights de la classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526195"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="76172-103">Méthode GetCallerAccessRights de la \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="76172-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="76172-104">La méthode **\_ \_ SystemSecurity :: GetCallerAccessRights** définit le paramètre *Rights* comme une image bitmap avec chaque bit correspondant à un droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="76172-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="76172-105">N’importe quel client peut l’appeler pour déterminer les droits dont dispose le client.</span><span class="sxs-lookup"><span data-stu-id="76172-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="76172-106">Cette méthode est utile pour les clients qui activent ou désactivent des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="76172-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="76172-107">Par exemple, une application GUI peut désactiver un bouton si l’utilisateur actuellement connecté ne dispose pas des droits d’exécution de méthode.</span><span class="sxs-lookup"><span data-stu-id="76172-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="76172-108">Tout client activé a le droit d’appeler **GetCallerAccessRights**, même si ce client ne dispose pas des droits d’exécution de méthode généraux.</span><span class="sxs-lookup"><span data-stu-id="76172-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="76172-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76172-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="76172-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76172-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76172-111">*droits* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76172-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76172-112">Droits d’accès du client.</span><span class="sxs-lookup"><span data-stu-id="76172-112">Access rights of the client.</span></span> <span data-ttu-id="76172-113">Pour plus d’informations, consultez [**\_ \_ SystemSecurity**](--systemsecurity.md) et [constantes de sécurité WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="76172-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="76172-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ACTIVER** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="76172-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="76172-115">Active le compte et accorde des autorisations de lecture à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="76172-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="76172-116">Il s’agit du droit d’accès par défaut pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="76172-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="76172-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTHODE \_ Execute** (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="76172-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="76172-118">Autorise l’exécution des méthodes.</span><span class="sxs-lookup"><span data-stu-id="76172-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="76172-119">Les fournisseurs peuvent effectuer des vérifications d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="76172-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="76172-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ REP en écriture complète** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="76172-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="76172-121">Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire dans les classes et les instances, à l’exception des classes système.</span><span class="sxs-lookup"><span data-stu-id="76172-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="76172-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ REP en écriture partielle** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="76172-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="76172-123">Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire des instances de fournisseur, mais pas des classes statiques ou des instances statiques dans le référentiel.</span><span class="sxs-lookup"><span data-stu-id="76172-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="76172-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Fournisseur d’écriture** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="76172-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="76172-125">Permet à l’appelant, au contexte de sécurité ou à l’utilisateur d’écrire des classes et des instances sur les fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="76172-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="76172-126">L’emprunt d’identité des fournisseurs peut effectuer des vérifications d’accès supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="76172-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="76172-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Accès à distance** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="76172-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="76172-128">Permet à un compte d’utilisateur d’effectuer à distance les opérations autorisées par les autres bits.</span><span class="sxs-lookup"><span data-stu-id="76172-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="76172-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Lecture \_ CONTRÔLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="76172-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="76172-130">Autorise l’accès en lecture aux descripteurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="76172-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="76172-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Écriture \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="76172-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="76172-132">Autorise l’accès en écriture à des listes de contrôle d’accès discrétionnaire (DACL).</span><span class="sxs-lookup"><span data-stu-id="76172-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76172-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76172-133">Return value</span></span>

<span data-ttu-id="76172-134">Cette méthode retourne un **HRESULT** qui indique l’état de l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="76172-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="76172-135">La liste suivante répertorie les valeurs de retour dont l’importance est de [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span><span class="sxs-lookup"><span data-stu-id="76172-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="76172-136">Pour les applications de script et de Visual Basic, le résultat peut être obtenu à partir de out- [Parameters. returnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="76172-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="76172-137">Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="76172-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="76172-138">**\_méthode WBEM \_ E \_ désactivée**</span><span class="sxs-lookup"><span data-stu-id="76172-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="76172-139">Cette méthode n’est pas prise en charge sur les versions prises en charge de Windows.</span><span class="sxs-lookup"><span data-stu-id="76172-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76172-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76172-140">Requirements</span></span>



| <span data-ttu-id="76172-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76172-141">Requirement</span></span> | <span data-ttu-id="76172-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="76172-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="76172-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76172-143">Minimum supported client</span></span><br/> | <span data-ttu-id="76172-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76172-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="76172-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76172-145">Minimum supported server</span></span><br/> | <span data-ttu-id="76172-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76172-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="76172-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="76172-147">Namespace</span></span><br/>                | <span data-ttu-id="76172-148">Tous les espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="76172-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="76172-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76172-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76172-150">Classes système WMI</span><span class="sxs-lookup"><span data-stu-id="76172-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="76172-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="76172-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="76172-152">**\_\_SystemSecurity :: est**</span><span class="sxs-lookup"><span data-stu-id="76172-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="76172-153">**\_\_SystemSecurity :: SetS**</span><span class="sxs-lookup"><span data-stu-id="76172-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="76172-154">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="76172-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="76172-155">**\_ACE Win32**</span><span class="sxs-lookup"><span data-stu-id="76172-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="76172-156">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="76172-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="76172-157">Sécurisation des espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="76172-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="76172-158">Constantes de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="76172-158">WMI Security Constants</span></span>
</dt> </dl>

 

