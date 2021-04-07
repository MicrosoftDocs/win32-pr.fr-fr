---
description: Le paramètre strPrivilege de la méthode SWbemPrivilegeSet. AddAsString et le paramètre iPrivilege pour SWbemPrivilegeSet. Add requièrent des chaînes de privilège de WbemPrivilegeEnum.
ms.assetid: f9400597-81bb-44a8-80dc-aba0160aea26
ms.tgt_platform: multiple
title: Constantes de privilège (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- wbemPrivilegeCreateToken
- wbemPrivilegePrimaryToken
- wbemPrivilegeLockMemory
- wbemPrivilegeIncreaseQuota
- wbemPrivilegeMachineAccount
- wbemPrivilegeTcb
- wbemPrivilegeSecurity
- wbemPrivilegeTakeOwnership
- wbemPrivilegeLoadDriver
- wbemPrivilegeSystemProfile
- wbemPrivilegeSystemtime
- wbemPrivilegeProfileSingleProcess
- wbemPrivilegeIncreaseBasePriority
- wbemPrivilegeCreatePagefile
- wbemPrivilegeCreatePermanent
- wbemPrivilegeBackup
- wbemPrivilegeRestore
- wbemPrivilegeShutdown
- wbemPrivilegeDebug
- wbemPrivilegeAudit
- wbemPrivilegeSystemEnvironment
- wbemPrivilegeChangeNotify
- wbemPrivilegeRemoteShutdown
- wbemPrivilegeUndock
- wbemPrivilegeSyncAgent
- wbemPrivilegeEnableDelegation
- wbemPrivilegeManageVolume
api_type:
- HeaderDef
api_location:
- Wbemdisp.h
ms.openlocfilehash: 73fb9167af63f40f3a6e1c00470d871f749d228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759766"
---
# <a name="privilege-constants"></a><span data-ttu-id="edf3a-103">Constantes de privilège</span><span class="sxs-lookup"><span data-stu-id="edf3a-103">Privilege Constants</span></span>

<span data-ttu-id="edf3a-104">Le *paramètre strPrivilege* de la [**méthode SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) et le paramètre *iPrivilege* pour [**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md) requièrent des chaînes de privilège de [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="edf3a-104">The *strPrivilege* parameter of the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method and the *iPrivilege* parameter for [**SWbemPrivilegeSet.Add**](swbemprivilegeset-add.md) require privilege strings from [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="edf3a-105">Pour plus d’informations sur l’utilisation des constantes de privilège, consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="edf3a-105">For more information about how to use privilege constants, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="edf3a-106">Les constantes suivantes sont définies dans [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="edf3a-106">The following constants are defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span> <span data-ttu-id="edf3a-107">La liste suivante comprend les constantes équivalentes pour C++ et les chaînes pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="edf3a-107">The following list includes the equivalent constants for C++ and strings for scripting.</span></span> <span data-ttu-id="edf3a-108">Pour former le nom abrégé de script, supprimez le « se » et le « privilège » du nom de la constante C++.</span><span class="sxs-lookup"><span data-stu-id="edf3a-108">To form the scripting short name, remove the "Se" and "Privilege" from the C++ constant name.</span></span>

<span data-ttu-id="edf3a-109">L’exemple de code VBScript suivant montre comment activer le privilège RemoteShutdown dans un script.</span><span class="sxs-lookup"><span data-stu-id="edf3a-109">The following VBScript code example shows how to enable the RemoteShutdown privilege in a script.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (RemoteShutdown)}")
```



<span data-ttu-id="edf3a-110">De nombreuses méthodes WMI requièrent l’activation d’une ou de plusieurs autorisations.</span><span class="sxs-lookup"><span data-stu-id="edf3a-110">Many WMI methods require that one or more permission be enabled.</span></span> <span data-ttu-id="edf3a-111">Si aucun privilège n’a été accordé à un compte, il ne peut pas être activé pour l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="edf3a-111">If an account has not been granted a privilege, it cannot be enabled for the method call.</span></span>

<dl> <dt>

<span data-ttu-id="edf3a-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span><span class="sxs-lookup"><span data-stu-id="edf3a-112"><span id="wbemPrivilegeCreateToken"></span><span id="wbemprivilegecreatetoken"></span><span id="WBEMPRIVILEGECREATETOKEN"></span>**wbemPrivilegeCreateToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="edf3a-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-114">Constante C++ : **se créer une chaîne de \_ \_ \_ nom de jeton** : **SeCreateTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-114">C++ constant: **SE\_CREATE\_TOKEN\_NAME** string: **SeCreateTokenPrivilege**</span></span>

<span data-ttu-id="edf3a-115">Nom abrégé du script : **Okta**</span><span class="sxs-lookup"><span data-stu-id="edf3a-115">Scripting short name: **CreateToken**</span></span>

<span data-ttu-id="edf3a-116">Requis pour créer un objet de jeton principal.</span><span class="sxs-lookup"><span data-stu-id="edf3a-116">Required to create a primary token object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="edf3a-117"><span id="wbemPrivilegePrimaryToken"></span><span id="wbemprivilegeprimarytoken"></span><span id="WBEMPRIVILEGEPRIMARYTOKEN"></span>**wbemPrivilegePrimaryToken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-118">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="edf3a-118">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-119">Constante C++ : **SeAssignPrimaryTokenPrivilege** chaîne : **SeAssignPrimaryTokenPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-119">C++ constant: **SeAssignPrimaryTokenPrivilege** string: **SeAssignPrimaryTokenPrivilege**</span></span>

<span data-ttu-id="edf3a-120">Nom abrégé du script : **AssignPrimaryToken**</span><span class="sxs-lookup"><span data-stu-id="edf3a-120">Scripting short name: **AssignPrimaryToken**</span></span>

<span data-ttu-id="edf3a-121">Requis pour remplacer un jeton au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="edf3a-121">Required to replace a process-level token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span><span class="sxs-lookup"><span data-stu-id="edf3a-122"><span id="wbemPrivilegeLockMemory"></span><span id="wbemprivilegelockmemory"></span><span id="WBEMPRIVILEGELOCKMEMORY"></span>**wbemPrivilegeLockMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-123">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="edf3a-123">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-124">Constante C++ : **\_ Delock \_ Memory \_ Name** String : **SeLockMemoryPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-124">C++ constant: **SE\_LOCK\_MEMORY\_NAME** string: **SeLockMemoryPrivilege**</span></span>

<span data-ttu-id="edf3a-125">Nom abrégé du script : **LockMemory**</span><span class="sxs-lookup"><span data-stu-id="edf3a-125">Scripting short name: **LockMemory**</span></span>

<span data-ttu-id="edf3a-126">Requis pour verrouiller des pages en mémoire.</span><span class="sxs-lookup"><span data-stu-id="edf3a-126">Required to lock pages in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span><span class="sxs-lookup"><span data-stu-id="edf3a-127"><span id="wbemPrivilegeIncreaseQuota"></span><span id="wbemprivilegeincreasequota"></span><span id="WBEMPRIVILEGEINCREASEQUOTA"></span>**wbemPrivilegeIncreaseQuota**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-128">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="edf3a-128">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-129">Constante C++ : **se augmente la chaîne de \_ \_ \_ nom de quota** : **SeIncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-129">C++ constant: **SE\_INCREASE\_QUOTA\_NAME** string: **SeIncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="edf3a-130">Nom abrégé du script : **IncreaseQuotaPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-130">Scripting short name: **IncreaseQuotaPrivilege**</span></span>

<span data-ttu-id="edf3a-131">Requis pour ajuster les quotas de mémoire d’un processus.</span><span class="sxs-lookup"><span data-stu-id="edf3a-131">Required to adjust memory quotas for a process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span><span class="sxs-lookup"><span data-stu-id="edf3a-132"><span id="wbemPrivilegeMachineAccount"></span><span id="wbemprivilegemachineaccount"></span><span id="WBEMPRIVILEGEMACHINEACCOUNT"></span>**wbemPrivilegeMachineAccount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-133">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="edf3a-133">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-134">Constante C++ : chaîne de **\_ \_ \_ nom de compte de se** -même : **SeMachineAccountPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-134">C++ constant: **SE\_MACINE\_ACCOUNT\_NAME** string: **SeMachineAccountPrivilege**</span></span>

<span data-ttu-id="edf3a-135">Nom abrégé du script : **MachineAccount**</span><span class="sxs-lookup"><span data-stu-id="edf3a-135">Scripting short name: **MachineAccount**</span></span>

<span data-ttu-id="edf3a-136">Requis pour ajouter des stations de travail à un domaine.</span><span class="sxs-lookup"><span data-stu-id="edf3a-136">Required to add workstations to a domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span><span class="sxs-lookup"><span data-stu-id="edf3a-137"><span id="wbemPrivilegeTcb"></span><span id="wbemprivilegetcb"></span><span id="WBEMPRIVILEGETCB"></span>**wbemPrivilegeTcb**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-138">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="edf3a-138">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-139">Constante C++ : chaîne de **\_ \_ nom TCB** de la se : **SeTcbPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-139">C++ constant: **SE\_TCB\_NAME** string: **SeTcbPrivilege**</span></span>

<span data-ttu-id="edf3a-140">Nom abrégé du script : **TCB**</span><span class="sxs-lookup"><span data-stu-id="edf3a-140">Scripting short name: **Tcb**</span></span>

<span data-ttu-id="edf3a-141">Requis pour agir en tant que partie du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="edf3a-141">Required to act as part of the operating system.</span></span> <span data-ttu-id="edf3a-142">Le détenteur fait partie de la base de l’ordinateur approuvé.</span><span class="sxs-lookup"><span data-stu-id="edf3a-142">The holder is part of the trusted computer base.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span><span class="sxs-lookup"><span data-stu-id="edf3a-143"><span id="wbemPrivilegeSecurity"></span><span id="wbemprivilegesecurity"></span><span id="WBEMPRIVILEGESECURITY"></span>**wbemPrivilegeSecurity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-144">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="edf3a-144">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-145">Constante C++ : chaîne de **\_ \_ nom de sécurité de se** : **SeSecurityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-145">C++ constant: **SE\_SECURITY\_NAME** string: **SeSecurityPrivilege**</span></span>

<span data-ttu-id="edf3a-146">Nom abrégé du script : **sécurité**</span><span class="sxs-lookup"><span data-stu-id="edf3a-146">Scripting short name: **Security**</span></span>

<span data-ttu-id="edf3a-147">Requis pour gérer l’audit et le journal de sécurité NT.</span><span class="sxs-lookup"><span data-stu-id="edf3a-147">Required to manage auditing and the NT security log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="edf3a-148"><span id="wbemPrivilegeTakeOwnership"></span><span id="wbemprivilegetakeownership"></span><span id="WBEMPRIVILEGETAKEOWNERSHIP"></span>**wbemPrivilegeTakeOwnership**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-149">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="edf3a-149">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-150">Constante C++ : **se \_ prendre \_ possession \_** de la chaîne de nom : **SeTakeOwnershipPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-150">C++ constant: **SE\_TAKE\_OWNERSHIP\_NAME** string: **SeTakeOwnershipPrivilege**</span></span>

<span data-ttu-id="edf3a-151">Nom abrégé du script : **TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="edf3a-151">Scripting short name: **TakeOwnership**</span></span>

<span data-ttu-id="edf3a-152">Obligatoire pour assumer la propriété des fichiers ou d’autres objets sans avoir d' [*entrée de Access Control*](/windows/desktop/SecGloss/a-gly) dans la liste de contrôle d’accès discrétionnaire (DACL, *Discretionary Access Control List* ).</span><span class="sxs-lookup"><span data-stu-id="edf3a-152">Required to assume ownership of files or other objects without having an [*Access Control Entry*](/windows/desktop/SecGloss/a-gly) (ACE) in the *discretionary access control list* (DACL).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span><span class="sxs-lookup"><span data-stu-id="edf3a-153"><span id="wbemPrivilegeLoadDriver"></span><span id="wbemprivilegeloaddriver"></span><span id="WBEMPRIVILEGELOADDRIVER"></span>**wbemPrivilegeLoadDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-154">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="edf3a-154">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-155">Constante C++ : **se \_ charger \_** la chaîne du pilote : **SeLoadDriverPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-155">C++ constant: **SE\_LOAD\_DRIVER** string: **SeLoadDriverPrivilege**</span></span>

<span data-ttu-id="edf3a-156">Nom abrégé du script : **LoadDriver**</span><span class="sxs-lookup"><span data-stu-id="edf3a-156">Scripting short name: **LoadDriver**</span></span>

<span data-ttu-id="edf3a-157">Requis pour charger ou décharger un pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="edf3a-157">Required to load or unload a device driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="edf3a-158"><span id="wbemPrivilegeSystemProfile"></span><span id="wbemprivilegesystemprofile"></span><span id="WBEMPRIVILEGESYSTEMPROFILE"></span>**wbemPrivilegeSystemProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-159">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="edf3a-159">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-160">Constante C++ : chaîne de **\_ \_ \_ nom de profil système se** : **SeSystemProfilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-160">C++ constant: **SE\_SYSTEM\_PROFILE\_NAME** string: **SeSystemProfilePrivilege**</span></span>

<span data-ttu-id="edf3a-161">Nom abrégé du script : **SystemProfile**</span><span class="sxs-lookup"><span data-stu-id="edf3a-161">Scripting short name: **SystemProfile**</span></span>

<span data-ttu-id="edf3a-162">Requis pour collecter des informations de profil sur les performances du système.</span><span class="sxs-lookup"><span data-stu-id="edf3a-162">Required to gather profile information about system performance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span><span class="sxs-lookup"><span data-stu-id="edf3a-163"><span id="wbemPrivilegeSystemtime"></span><span id="wbemprivilegesystemtime"></span><span id="WBEMPRIVILEGESYSTEMTIME"></span>**wbemPrivilegeSystemtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-164">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="edf3a-164">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-165">Constante C++ : chaîne de nom **\_ SystemTime de se** \_ : **SeSystemTimePrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-165">C++ constant: **SE\_SYSTEMTIME**\_NAME string: **SeSystemtimePrivilege**</span></span>

<span data-ttu-id="edf3a-166">Nom abrégé du script : **SystemTime**</span><span class="sxs-lookup"><span data-stu-id="edf3a-166">Scripting short name: **Systemtime**</span></span>

<span data-ttu-id="edf3a-167">Requis pour modifier l’heure système.</span><span class="sxs-lookup"><span data-stu-id="edf3a-167">Required to change the system time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="edf3a-168"><span id="wbemPrivilegeProfileSingleProcess"></span><span id="wbemprivilegeprofilesingleprocess"></span><span id="WBEMPRIVILEGEPROFILESINGLEPROCESS"></span>**wbemPrivilegeProfileSingleProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-169">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="edf3a-169">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-170">Constante C++ : chaîne de **\_ \_ \_ \_ nom de processus unique de se Prof** : **SeProfileSingleProcessPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-170">C++ constant: **SE\_PROF\_SINGLE\_PROCESS\_NAME** string: **SeProfileSingleProcessPrivilege**</span></span>

<span data-ttu-id="edf3a-171">Nom abrégé du script : **ProfileSingleProcess**</span><span class="sxs-lookup"><span data-stu-id="edf3a-171">Scripting short name: **ProfileSingleProcess**</span></span>

<span data-ttu-id="edf3a-172">Requis pour collecter des informations de profil pour un seul processus.</span><span class="sxs-lookup"><span data-stu-id="edf3a-172">Required to gather profile information for a single process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="edf3a-173"><span id="wbemPrivilegeIncreaseBasePriority"></span><span id="wbemprivilegeincreasebasepriority"></span><span id="WBEMPRIVILEGEINCREASEBASEPRIORITY"></span>**wbemPrivilegeIncreaseBasePriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-174">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="edf3a-174">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-175">Constante C++ : chaîne de **nom de priorité de \_ \_ base se \_ \_ Inc** . : **SeIncreaseBasePriorityPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-175">C++ constant: **SE\_INC\_BASE\_PRIORITY\_NAME** string: **SeIncreaseBasePriorityPrivilege**</span></span>

<span data-ttu-id="edf3a-176">Nom abrégé du script : **IncreaseBasePriority**</span><span class="sxs-lookup"><span data-stu-id="edf3a-176">Scripting short name: **IncreaseBasePriority**</span></span>

<span data-ttu-id="edf3a-177">Requis pour augmenter la priorité de planification.</span><span class="sxs-lookup"><span data-stu-id="edf3a-177">Required to increase scheduling priority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="edf3a-178"><span id="wbemPrivilegeCreatePagefile"></span><span id="wbemprivilegecreatepagefile"></span><span id="WBEMPRIVILEGECREATEPAGEFILE"></span>**wbemPrivilegeCreatePagefile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-179">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="edf3a-179">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-180">Constante C++ : **se créer une chaîne de \_ nom de fichier d' \_ échange \_** : **SeCreatePagefilePrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-180">C++ constant: **SE\_CREATE\_PAGEFILE\_NAME** string: **SeCreatePagefilePrivilege**</span></span>

<span data-ttu-id="edf3a-181">Nom abrégé du script : **CreatePagefile**</span><span class="sxs-lookup"><span data-stu-id="edf3a-181">Scripting short name: **CreatePagefile**</span></span>

<span data-ttu-id="edf3a-182">Requis pour créer un fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="edf3a-182">Required to create a pagefile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="edf3a-183"><span id="wbemPrivilegeCreatePermanent"></span><span id="wbemprivilegecreatepermanent"></span><span id="WBEMPRIVILEGECREATEPERMANENT"></span>**wbemPrivilegeCreatePermanent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-184">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="edf3a-184">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-185">Constante C++ : **se créer une chaîne de \_ \_ \_ nom permanente** : **SeCreatePermanentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-185">C++ constant: **SE\_CREATE\_PERMANENT\_NAME** string: **SeCreatePermanentPrivilege**</span></span>

<span data-ttu-id="edf3a-186">Nom abrégé du script : **CreatePermanent**</span><span class="sxs-lookup"><span data-stu-id="edf3a-186">Scripting short name: **CreatePermanent**</span></span>

<span data-ttu-id="edf3a-187">Requis pour créer des objets partagés permanents.</span><span class="sxs-lookup"><span data-stu-id="edf3a-187">Required to create permanent shared objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span><span class="sxs-lookup"><span data-stu-id="edf3a-188"><span id="wbemPrivilegeBackup"></span><span id="wbemprivilegebackup"></span><span id="WBEMPRIVILEGEBACKUP"></span>**wbemPrivilegeBackup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-189">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="edf3a-189">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-190">Constante C++ : chaîne de **\_ \_ nom** de la sauvegarde de se : **SeBackupPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-190">C++ constant: **SE\_BACKUP\_NAME** string: **SeBackupPrivilege**</span></span>

<span data-ttu-id="edf3a-191">Nom abrégé du script : **sauvegarde**</span><span class="sxs-lookup"><span data-stu-id="edf3a-191">Scripting short name: **Backup**</span></span>

<span data-ttu-id="edf3a-192">Requis pour sauvegarder des fichiers et des répertoires, quelle que soit la liste de contrôle d’accès spécifiée pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="edf3a-192">Required to backup files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span><span class="sxs-lookup"><span data-stu-id="edf3a-193"><span id="wbemPrivilegeRestore"></span><span id="wbemprivilegerestore"></span><span id="WBEMPRIVILEGERESTORE"></span>**wbemPrivilegeRestore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-194">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="edf3a-194">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-195">Constante C++ : **se \_ Restore \_ Name** String : **SeRestorePrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-195">C++ constant: **SE\_RESTORE\_NAME** string: **SeRestorePrivilege**</span></span>

<span data-ttu-id="edf3a-196">Nom abrégé du script : **restauration**</span><span class="sxs-lookup"><span data-stu-id="edf3a-196">Scripting short name: **Restore**</span></span>

<span data-ttu-id="edf3a-197">Requis pour restaurer des fichiers et des répertoires, quelle que soit la liste de contrôle d’accès spécifiée pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="edf3a-197">Required to restore files and directories, regardless of the ACL specified for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span><span class="sxs-lookup"><span data-stu-id="edf3a-198"><span id="wbemPrivilegeShutdown"></span><span id="wbemprivilegeshutdown"></span><span id="WBEMPRIVILEGESHUTDOWN"></span>**wbemPrivilegeShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-199">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="edf3a-199">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-200">Constante C++ : **se \_ arrêter \_** chaîne de nom : **SeShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-200">C++ constant: **SE\_SHUTDOWN\_NAME** string: **SeShutdownPrivilege**</span></span>

<span data-ttu-id="edf3a-201">Nom abrégé du script : **Shutdown**</span><span class="sxs-lookup"><span data-stu-id="edf3a-201">Scripting short name: **Shutdown**</span></span>

<span data-ttu-id="edf3a-202">Requis pour arrêter le système local.</span><span class="sxs-lookup"><span data-stu-id="edf3a-202">Required to shut down the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span><span class="sxs-lookup"><span data-stu-id="edf3a-203"><span id="wbemPrivilegeDebug"></span><span id="wbemprivilegedebug"></span><span id="WBEMPRIVILEGEDEBUG"></span>**wbemPrivilegeDebug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-204">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="edf3a-204">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-205">Constante C++ : chaîne de **\_ \_ nom de débogage de se** : **SeDebugPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-205">C++ constant: **SE\_DEBUG\_NAME** string: **SeDebugPrivilege**</span></span>

<span data-ttu-id="edf3a-206">Nom abrégé du script : **débogage**</span><span class="sxs-lookup"><span data-stu-id="edf3a-206">Scripting short name: **Debug**</span></span>

<span data-ttu-id="edf3a-207">Requis pour déboguer et ajuster la mémoire d’un processus appartenant à un autre compte.</span><span class="sxs-lookup"><span data-stu-id="edf3a-207">Required to debug and adjust the memory of a process owned by another account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span><span class="sxs-lookup"><span data-stu-id="edf3a-208"><span id="wbemPrivilegeAudit"></span><span id="wbemprivilegeaudit"></span><span id="WBEMPRIVILEGEAUDIT"></span>**wbemPrivilegeAudit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-209">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="edf3a-209">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-210">Constante C++ : chaîne de **\_ \_ nom d’audit** de la se : **SeAuditPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-210">C++ constant: **SE\_AUDIT\_NAME** string: **SeAuditPrivilege**</span></span>

<span data-ttu-id="edf3a-211">Nom abrégé du script : **audit**</span><span class="sxs-lookup"><span data-stu-id="edf3a-211">Scripting short name: **Audit**</span></span>

<span data-ttu-id="edf3a-212">Requis pour générer des entrées d’audit dans le journal de sécurité NT.</span><span class="sxs-lookup"><span data-stu-id="edf3a-212">Required to generate audit entries in the NT Security log.</span></span> <span data-ttu-id="edf3a-213">Seuls les serveurs sécurisés doivent disposer de ce privilège.</span><span class="sxs-lookup"><span data-stu-id="edf3a-213">Only secure servers should have this privilege.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="edf3a-214"><span id="wbemPrivilegeSystemEnvironment"></span><span id="wbemprivilegesystemenvironment"></span><span id="WBEMPRIVILEGESYSTEMENVIRONMENT"></span>**wbemPrivilegeSystemEnvironment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-215">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="edf3a-215">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-216">Constante C++ : chaîne de nom de l' **\_ \_ environnement \_ système se** : **SeSystemEnvironmentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-216">C++ constant: **SE\_SYSTEM\_ENVIRONMENT\_NAME** string: **SeSystemEnvironmentPrivilege**</span></span>

<span data-ttu-id="edf3a-217">Nom abrégé du script : **SystemEnvironment**</span><span class="sxs-lookup"><span data-stu-id="edf3a-217">Scripting short name: **SystemEnvironment**</span></span>

<span data-ttu-id="edf3a-218">Requis pour modifier la mémoire RAM non volatile des systèmes qui utilisent ce type de mémoire pour stocker les données de configuration.</span><span class="sxs-lookup"><span data-stu-id="edf3a-218">Required to modify the nonvolatile RAM of systems that use this type of memory to store configuration data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="edf3a-219"><span id="wbemPrivilegeChangeNotify"></span><span id="wbemprivilegechangenotify"></span><span id="WBEMPRIVILEGECHANGENOTIFY"></span>**wbemPrivilegeChangeNotify**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-220">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="edf3a-220">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-221">Constante C++ : nom de la chaîne de notification de modification de la **se \_ \_ \_** : **SeChangeNotifyPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-221">C++ constant: **SE\_CHANGE\_NOTIFY\_NAME** string: **SeChangeNotifyPrivilege**</span></span>

<span data-ttu-id="edf3a-222">Nom abrégé du script : **ChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="edf3a-222">Scripting short name: **ChangeNotify**</span></span>

<span data-ttu-id="edf3a-223">Requis pour recevoir des notifications des modifications apportées aux fichiers ou aux répertoires et contourner les vérifications d’accès Traversal.</span><span class="sxs-lookup"><span data-stu-id="edf3a-223">Required to receive notifications of changes to files or directories and bypass traversal access checks.</span></span> <span data-ttu-id="edf3a-224">Ce privilège est activé par défaut pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="edf3a-224">This privilege is enabled by default for all users.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="edf3a-225"><span id="wbemPrivilegeRemoteShutdown"></span><span id="wbemprivilegeremoteshutdown"></span><span id="WBEMPRIVILEGEREMOTESHUTDOWN"></span>**wbemPrivilegeRemoteShutdown**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-226">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="edf3a-226">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-227">Constante C++ : chaîne de **\_ \_ \_ nom d’arrêt à distance de se** : **SeRemoteShutdownPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-227">C++ constant: **SE\_REMOTE\_SHUTDOWN\_NAME** string: **SeRemoteShutdownPrivilege**</span></span>

<span data-ttu-id="edf3a-228">Nom abrégé du script : **RemoteShutdown**</span><span class="sxs-lookup"><span data-stu-id="edf3a-228">Scripting short name: **RemoteShutdown**</span></span>

<span data-ttu-id="edf3a-229">Requis pour arrêter un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="edf3a-229">Required to shut down a remote computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span><span class="sxs-lookup"><span data-stu-id="edf3a-230"><span id="wbemPrivilegeUndock"></span><span id="wbemprivilegeundock"></span><span id="WBEMPRIVILEGEUNDOCK"></span>**wbemPrivilegeUndock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-231">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="edf3a-231">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-232">Constante C++ : **se \_ \_ détacher** la chaîne de nom : **SeUndockPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-232">C++ constant: **SE\_UNDOCK\_NAME** string: **SeUndockPrivilege**</span></span>

<span data-ttu-id="edf3a-233">Nom abrégé du script : **détacher**</span><span class="sxs-lookup"><span data-stu-id="edf3a-233">Scripting short name: **Undock**</span></span>

<span data-ttu-id="edf3a-234">Requis pour retirer un ordinateur portable d’une station d’accueil.</span><span class="sxs-lookup"><span data-stu-id="edf3a-234">Required to remove a laptop from a docking station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span><span class="sxs-lookup"><span data-stu-id="edf3a-235"><span id="wbemPrivilegeSyncAgent"></span><span id="wbemprivilegesyncagent"></span><span id="WBEMPRIVILEGESYNCAGENT"></span>**wbemPrivilegeSyncAgent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-236">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="edf3a-236">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-237">Constante C++ : nom de la chaîne de **\_ \_ l’agent \_ de synchronisation se** : **SeSyncAgentPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-237">C++ constant: **SE\_SYNC\_AGENT\_NAME** string: **SeSyncAgentPrivilege**</span></span>

<span data-ttu-id="edf3a-238">Nom abrégé du script : **SyncAgent**</span><span class="sxs-lookup"><span data-stu-id="edf3a-238">Scripting short name: **SyncAgent**</span></span>

<span data-ttu-id="edf3a-239">Requis pour synchroniser les données du service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="edf3a-239">Required to synchronize directory service data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="edf3a-240"><span id="wbemPrivilegeEnableDelegation"></span><span id="wbemprivilegeenabledelegation"></span><span id="WBEMPRIVILEGEENABLEDELEGATION"></span>**wbemPrivilegeEnableDelegation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-241">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="edf3a-241">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-242">Constante C++ : **se activer la chaîne de \_ \_ \_ nom de délégation** : **SeEnableDelegationPrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-242">C++ constant: **SE\_ENABLE\_DELEGATION\_NAME** string: **SeEnableDelegationPrivilege**</span></span>

<span data-ttu-id="edf3a-243">Nom abrégé du script : **EnableDelegation**</span><span class="sxs-lookup"><span data-stu-id="edf3a-243">Scripting short name: **EnableDelegation**</span></span>

<span data-ttu-id="edf3a-244">Requis pour permettre aux comptes d’ordinateurs et d’utilisateurs d’être approuvés pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="edf3a-244">Required to enable computer and user accounts to be trusted for delegation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="edf3a-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span><span class="sxs-lookup"><span data-stu-id="edf3a-245"><span id="wbemPrivilegeManageVolume"></span><span id="wbemprivilegemanagevolume"></span><span id="WBEMPRIVILEGEMANAGEVOLUME"></span>**wbemPrivilegeManageVolume**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="edf3a-246">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="edf3a-246">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="edf3a-247">Constante C++ : **se gérer la chaîne de \_ \_ \_ nom de volume** : **SeManageVolumePrivilege**</span><span class="sxs-lookup"><span data-stu-id="edf3a-247">C++ constant: **SE\_MANAGE\_VOLUME\_NAME** string: **SeManageVolumePrivilege**</span></span>

<span data-ttu-id="edf3a-248">Nom abrégé du script : **ManageVolume**</span><span class="sxs-lookup"><span data-stu-id="edf3a-248">Scripting short name: **ManageVolume**</span></span>

<span data-ttu-id="edf3a-249">Requis pour effectuer des tâches de maintenance de volume.</span><span class="sxs-lookup"><span data-stu-id="edf3a-249">Required to perform volume maintenance tasks.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="edf3a-250">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edf3a-250">Requirements</span></span>



| <span data-ttu-id="edf3a-251">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edf3a-251">Requirement</span></span> | <span data-ttu-id="edf3a-252">Valeur</span><span class="sxs-lookup"><span data-stu-id="edf3a-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="edf3a-253">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf3a-253">Minimum supported client</span></span><br/> | <span data-ttu-id="edf3a-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edf3a-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="edf3a-255">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="edf3a-255">Minimum supported server</span></span><br/> | <span data-ttu-id="edf3a-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="edf3a-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="edf3a-257">En-tête</span><span class="sxs-lookup"><span data-stu-id="edf3a-257">Header</span></span><br/>                   | <dl> <span data-ttu-id="edf3a-258"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="edf3a-258"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="edf3a-259">MIDL</span><span class="sxs-lookup"><span data-stu-id="edf3a-259">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edf3a-260"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="edf3a-260"><dt>Wbemdisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edf3a-261">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edf3a-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf3a-262">Constantes d’API de script</span><span class="sxs-lookup"><span data-stu-id="edf3a-262">Scripting API Constants</span></span>](scripting-api-constants.md)
</dt> <dt>

[<span data-ttu-id="edf3a-263">**SWbemSecurity**</span><span class="sxs-lookup"><span data-stu-id="edf3a-263">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="edf3a-264">**WbemPrivilegeEnum**</span><span class="sxs-lookup"><span data-stu-id="edf3a-264">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="edf3a-265">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="edf3a-265">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="edf3a-266">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="edf3a-266">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

