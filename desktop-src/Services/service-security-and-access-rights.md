---
description: Le modèle de sécurité Windows vous permet de contrôler l’accès au gestionnaire de contrôle des services (SCM) et aux objets de service.
ms.assetid: 23d1c382-6ba4-49e2-8039-c2a91471076c
title: Sécurité des services et droits d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7677b8a9f7a5e1fadf8231999d266a9474fb731
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518895"
---
# <a name="service-security-and-access-rights"></a><span data-ttu-id="d025c-103">Sécurité des services et droits d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-103">Service Security and Access Rights</span></span>

<span data-ttu-id="d025c-104">Le modèle de sécurité Windows vous permet de contrôler l’accès au gestionnaire de contrôle des services (SCM) et aux objets de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-104">The Windows security model enables you to control access to the service control manager (SCM) and service objects.</span></span> <span data-ttu-id="d025c-105">Les sections suivantes fournissent des informations détaillées :</span><span class="sxs-lookup"><span data-stu-id="d025c-105">The following sections provide detailed information:</span></span>

-   [<span data-ttu-id="d025c-106">Droits d’accès pour le gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="d025c-106">Access Rights for the Service Control Manager</span></span>](#access-rights-for-the-service-control-manager)
-   [<span data-ttu-id="d025c-107">Droits d’accès pour un service</span><span class="sxs-lookup"><span data-stu-id="d025c-107">Access Rights for a Service</span></span>](#access-rights-for-a-service)

## <a name="access-rights-for-the-service-control-manager"></a><span data-ttu-id="d025c-108">Droits d’accès pour le gestionnaire de contrôle des services</span><span class="sxs-lookup"><span data-stu-id="d025c-108">Access Rights for the Service Control Manager</span></span>

<span data-ttu-id="d025c-109">Voici les droits d’accès spécifiques au SCM.</span><span class="sxs-lookup"><span data-stu-id="d025c-109">The following are the specific access rights for the SCM.</span></span>



| <span data-ttu-id="d025c-110">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-110">Access right</span></span>                                   | <span data-ttu-id="d025c-111">Description</span><span class="sxs-lookup"><span data-stu-id="d025c-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d025c-112">**SC \_ \_Tous les \_ accès au gestionnaire** (0xF003F)</span><span class="sxs-lookup"><span data-stu-id="d025c-112">**SC\_MANAGER\_ALL\_ACCESS** (0xF003F)</span></span>         | <span data-ttu-id="d025c-113">Comprend **les \_ droits standard \_ requis**, ainsi que tous les droits d’accès figurant dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="d025c-113">Includes **STANDARD\_RIGHTS\_REQUIRED**, in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d025c-114">**SC \_ \_ \_ Service de création de gestionnaire** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="d025c-114">**SC\_MANAGER\_CREATE\_SERVICE** (0x0002)</span></span>      | <span data-ttu-id="d025c-115">Obligatoire pour appeler la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) afin de créer un objet de service et de l’ajouter à la base de données.</span><span class="sxs-lookup"><span data-stu-id="d025c-115">Required to call the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to create a service object and add it to the database.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="d025c-116">**SC \_ Gestionnaire de \_ connexion** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="d025c-116">**SC\_MANAGER\_CONNECT** (0x0001)</span></span>              | <span data-ttu-id="d025c-117">Requis pour se connecter au gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="d025c-117">Required to connect to the service control manager.</span></span>                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d025c-118">**SC \_ \_ \_ Service d’énumération du gestionnaire** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="d025c-118">**SC\_MANAGER\_ENUMERATE\_SERVICE** (0x0004)</span></span>   | <span data-ttu-id="d025c-119">Requis pour appeler la fonction [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) ou [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) pour répertorier les services qui se trouvent dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d025c-119">Required to call the [**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa) or [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to list the services that are in the database.</span></span><br/> <span data-ttu-id="d025c-120">Requis pour appeler la fonction [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) pour recevoir une notification lorsqu’un service est créé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="d025c-120">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when any service is created or deleted.</span></span><br/> |
| <span data-ttu-id="d025c-121">**SC \_ \_Verrou du gestionnaire** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="d025c-121">**SC\_MANAGER\_LOCK** (0x0008)</span></span>                 | <span data-ttu-id="d025c-122">Requis pour appeler la fonction [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) pour acquérir un verrou sur la base de données.</span><span class="sxs-lookup"><span data-stu-id="d025c-122">Required to call the [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) function to acquire a lock on the database.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d025c-123">**SC \_ Gestionnaire de modification de la \_ \_ \_ configuration de démarrage** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="d025c-123">**SC\_MANAGER\_MODIFY\_BOOT\_CONFIG** (0x0020)</span></span> | <span data-ttu-id="d025c-124">Requis pour appeler la fonction [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .</span><span class="sxs-lookup"><span data-stu-id="d025c-124">Required to call the [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) function.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d025c-125">**SC \_ \_État du \_ verrou \_ de requête du gestionnaire** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="d025c-125">**SC\_MANAGER\_QUERY\_LOCK\_STATUS** (0x0010)</span></span>  | <span data-ttu-id="d025c-126">Requis pour appeler la fonction [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) pour récupérer les informations d’état de verrouillage de la base de données.</span><span class="sxs-lookup"><span data-stu-id="d025c-126">Required to call the [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) function to retrieve the lock status information for the database.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="d025c-127">Vous trouverez ci-dessous les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="d025c-127">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for the SCM.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d025c-128">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-128">Access right</span></span></th>
<th><span data-ttu-id="d025c-129">Description</span><span class="sxs-lookup"><span data-stu-id="d025c-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d025c-130"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-130"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-131"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-131"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="d025c-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-132">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="d025c-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-133">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-134"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-134"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-135"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-135"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="d025c-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-136">
<strong>SC_MANAGER_CREATE_SERVICE</strong></span></span><br /><span data-ttu-id="d025c-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-137">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d025c-138"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-138"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-139"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="d025c-140">
<strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-140">
<strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="d025c-141">
<strong>SC_MANAGER_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-141">
<strong>SC_MANAGER_LOCK</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-142"><strong>GENERIC_ALL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-142"><strong>GENERIC_ALL</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-143"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d025c-144">Un processus avec les droits d’accès corrects peut ouvrir un handle vers le SCM qui peut être utilisé dans les fonctions [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)et [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) .</span><span class="sxs-lookup"><span data-stu-id="d025c-144">A process with the correct access rights can open a handle to the SCM that can be used in the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea), [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa), and [**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa) functions.</span></span> <span data-ttu-id="d025c-145">Seuls les processus avec des privilèges d’administrateur peuvent ouvrir des descripteurs sur le SCM qui peuvent être utilisés par les fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) .</span><span class="sxs-lookup"><span data-stu-id="d025c-145">Only processes with Administrator privileges are able to open handles to the SCM that can be used by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase) functions.</span></span>

<span data-ttu-id="d025c-146">Le système crée le descripteur de sécurité pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="d025c-146">The system creates the security descriptor for the SCM.</span></span> <span data-ttu-id="d025c-147">Pour obtenir ou définir le descripteur de sécurité pour le SCM, utilisez les fonctions [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) et [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) avec un handle vers l’objet SCManager.</span><span class="sxs-lookup"><span data-stu-id="d025c-147">To get or set the security descriptor for the SCM, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions with a handle to the SCManager object.</span></span>

<span data-ttu-id="d025c-148">**Windows Server 2003 et Windows XP :** Contrairement à la plupart des autres objets sécurisables, le descripteur de sécurité du SCM ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="d025c-148">**Windows Server 2003 and Windows XP:** Unlike most other securable objects, the security descriptor for the SCM cannot be modified.</span></span> <span data-ttu-id="d025c-149">Ce comportement a été modifié à partir de Windows Server 2003 avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d025c-149">This behavior has changed as of Windows Server 2003 with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="d025c-150">Les droits d’accès suivants sont accordés.</span><span class="sxs-lookup"><span data-stu-id="d025c-150">The following access rights are granted.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d025c-151">Compte</span><span class="sxs-lookup"><span data-stu-id="d025c-151">Account</span></span></th>
<th><span data-ttu-id="d025c-152">Droits d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-152">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d025c-153">Utilisateurs authentifiés distants</span><span class="sxs-lookup"><span data-stu-id="d025c-153">Remote authenticated users</span></span></td>
<td><dl> <span data-ttu-id="d025c-154"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-154"><strong>SC_MANAGER_CONNECT</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-155">Utilisateurs authentifiés locaux (y compris LocalService et NetworkService)</span><span class="sxs-lookup"><span data-stu-id="d025c-155">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="d025c-156"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-156"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="d025c-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-157">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="d025c-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-158">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="d025c-159">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-159">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d025c-160">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="d025c-160">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="d025c-161"><strong>SC_MANAGER_CONNECT</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-161"><strong>SC_MANAGER_CONNECT</strong></span></span><br /><span data-ttu-id="d025c-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-162">
<strong>SC_MANAGER_ENUMERATE_SERVICE</strong></span></span><br /><span data-ttu-id="d025c-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-163">
<strong>SC_MANAGER_MODIFY_BOOT_CONFIG</strong></span></span><br /><span data-ttu-id="d025c-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-164">
<strong>SC_MANAGER_QUERY_LOCK_STATUS</strong></span></span><br /><span data-ttu-id="d025c-165">
<strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-165">
<strong>STANDARD_RIGHTS_READ</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-166">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="d025c-166">Administrators</span></span></td>
<td><dl> <span data-ttu-id="d025c-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-167"><strong>SC_MANAGER_ALL_ACCESS</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d025c-168">Notez que les utilisateurs distants authentifiés sur le réseau mais non connectés de manière interactive peuvent se connecter au SCM mais pas effectuer des opérations qui nécessitent d’autres droits d’accès.</span><span class="sxs-lookup"><span data-stu-id="d025c-168">Notice that remote users authenticated over the network but not interactively logged on can connect to the SCM but not perform operations that require other access rights.</span></span> <span data-ttu-id="d025c-169">Pour effectuer ces opérations, l’utilisateur doit être connecté de manière interactive ou le service doit utiliser l’un des comptes de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-169">To perform these operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="d025c-170">**Windows Server 2003 et Windows XP :** Les utilisateurs authentifiés distants reçoivent les droits de **\_ \_ connexion du gestionnaire** SC, du **\_ \_ \_ service d’énumération SC** Manager, de l' **\_ État du verrou de \_ requête \_ \_ SC Manager** et des droits d’accès **\_ \_ en lecture des droits standard** .</span><span class="sxs-lookup"><span data-stu-id="d025c-170">**Windows Server 2003 and Windows XP:** Remote authenticated users are granted the **SC\_MANAGER\_CONNECT**, **SC\_MANAGER\_ENUMERATE\_SERVICE**, **SC\_MANAGER\_QUERY\_LOCK\_STATUS**, and **STANDARD\_RIGHTS\_READ** access rights.</span></span> <span data-ttu-id="d025c-171">Ces droits d’accès sont limités, comme décrit dans le tableau précédent à compter de Windows Server 2003 avec SP1.</span><span class="sxs-lookup"><span data-stu-id="d025c-171">These access rights are restricted as described in the previous table as of Windows Server 2003 with SP1</span></span>

<span data-ttu-id="d025c-172">Lorsqu’un processus utilise la fonction [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) pour ouvrir un handle vers une base de données de services installés, il peut demander des droits d’accès.</span><span class="sxs-lookup"><span data-stu-id="d025c-172">When a process uses the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to open a handle to a database of installed services, it can request access rights.</span></span> <span data-ttu-id="d025c-173">Le système effectue une vérification de sécurité par rapport au descripteur de sécurité du SCM avant d’accorder les droits d’accès demandés.</span><span class="sxs-lookup"><span data-stu-id="d025c-173">The system performs a security check against the security descriptor for the SCM before granting the requested access rights.</span></span>

## <a name="access-rights-for-a-service"></a><span data-ttu-id="d025c-174">Droits d’accès pour un service</span><span class="sxs-lookup"><span data-stu-id="d025c-174">Access Rights for a Service</span></span>

<span data-ttu-id="d025c-175">Les droits d’accès spécifiques à un service sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d025c-175">The following are the specific access rights for a service.</span></span>



| <span data-ttu-id="d025c-176">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-176">Access right</span></span>                                | <span data-ttu-id="d025c-177">Description</span><span class="sxs-lookup"><span data-stu-id="d025c-177">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d025c-178">**Service \_ TOUT \_ accès** (0xF01FF)</span><span class="sxs-lookup"><span data-stu-id="d025c-178">**SERVICE\_ALL\_ACCESS** (0xF01FF)</span></span>          | <span data-ttu-id="d025c-179">Comprend **les \_ droits standard \_ requis** en plus de tous les droits d’accès de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="d025c-179">Includes **STANDARD\_RIGHTS\_REQUIRED** in addition to all access rights in this table.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d025c-180">**Service \_ MODIFIER la \_ configuration** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="d025c-180">**SERVICE\_CHANGE\_CONFIG** (0x0002)</span></span>        | <span data-ttu-id="d025c-181">Requis pour appeler la fonction [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) ou [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) pour modifier la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="d025c-181">Required to call the [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) or [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) function to change the service configuration.</span></span> <span data-ttu-id="d025c-182">Étant donné que l’appelant a le droit de modifier le fichier exécutable exécuté par le système, il doit être accordé uniquement aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="d025c-182">Because this grants the caller the right to change the executable file that the system runs, it should be granted only to administrators.</span></span>                                                              |
| <span data-ttu-id="d025c-183">**Service \_ ÉNUMÉRer les \_ dépendants** (0x0008)</span><span class="sxs-lookup"><span data-stu-id="d025c-183">**SERVICE\_ENUMERATE\_DEPENDENTS** (0x0008)</span></span> | <span data-ttu-id="d025c-184">Requis pour appeler la fonction [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) pour énumérer tous les services dépendants du service.</span><span class="sxs-lookup"><span data-stu-id="d025c-184">Required to call the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate all the services dependent on the service.</span></span>                                                                                                                                                                                                                                         |
| <span data-ttu-id="d025c-185">**Service \_ Interroger** (0x0080)</span><span class="sxs-lookup"><span data-stu-id="d025c-185">**SERVICE\_INTERROGATE** (0x0080)</span></span>           | <span data-ttu-id="d025c-186">Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour demander au service de signaler son état immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d025c-186">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to ask the service to report its status immediately.</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d025c-187">**Service \_ PAUSE \_ continue** (0x0040)</span><span class="sxs-lookup"><span data-stu-id="d025c-187">**SERVICE\_PAUSE\_CONTINUE** (0x0040)</span></span>       | <span data-ttu-id="d025c-188">Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour suspendre ou poursuivre le service.</span><span class="sxs-lookup"><span data-stu-id="d025c-188">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to pause or continue the service.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d025c-189">**Service \_ \_Configuration** de la requête (0x0001)</span><span class="sxs-lookup"><span data-stu-id="d025c-189">**SERVICE\_QUERY\_CONFIG** (0x0001)</span></span>         | <span data-ttu-id="d025c-190">Requis pour appeler les fonctions [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) et [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) pour interroger la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="d025c-190">Required to call the [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) and [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) functions to query the service configuration.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="d025c-191">**Service \_ \_État** de la requête (0x0004)</span><span class="sxs-lookup"><span data-stu-id="d025c-191">**SERVICE\_QUERY\_STATUS** (0x0004)</span></span>         | <span data-ttu-id="d025c-192">Requis pour appeler la fonction [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) ou [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) pour demander au gestionnaire de contrôle des services l’état du service.</span><span class="sxs-lookup"><span data-stu-id="d025c-192">Required to call the [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) or [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) function to ask the service control manager about the status of the service.</span></span><br/> <span data-ttu-id="d025c-193">Requis pour appeler la fonction [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) pour recevoir une notification quand un service change d’État.</span><span class="sxs-lookup"><span data-stu-id="d025c-193">Required to call the [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea) function to receive notification when a service changes status.</span></span><br/> |
| <span data-ttu-id="d025c-194">**Service \_ DÉBUT** (0x0010)</span><span class="sxs-lookup"><span data-stu-id="d025c-194">**SERVICE\_START** (0x0010)</span></span>                 | <span data-ttu-id="d025c-195">Requis pour appeler la fonction [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) pour démarrer le service.</span><span class="sxs-lookup"><span data-stu-id="d025c-195">Required to call the [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) function to start the service.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d025c-196">**Service \_ ARRÊTER** (0x0020)</span><span class="sxs-lookup"><span data-stu-id="d025c-196">**SERVICE\_STOP** (0x0020)</span></span>                  | <span data-ttu-id="d025c-197">Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="d025c-197">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to stop the service.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d025c-198">**Service \_ \_ \_ Contrôle défini par l’utilisateur**(0x0100)</span><span class="sxs-lookup"><span data-stu-id="d025c-198">**SERVICE\_USER\_DEFINED\_CONTROL**(0x0100)</span></span> | <span data-ttu-id="d025c-199">Requis pour appeler la fonction [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) pour spécifier un code de contrôle défini par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d025c-199">Required to call the [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) function to specify a user-defined control code.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="d025c-200">Les [droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights) pour un service sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d025c-200">The following are the [standard access rights](/windows/desktop/SecAuthZ/standard-access-rights) for a service.</span></span>



| <span data-ttu-id="d025c-201">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-201">Access right</span></span>                 | <span data-ttu-id="d025c-202">Description</span><span class="sxs-lookup"><span data-stu-id="d025c-202">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d025c-203">**ACCÉDER à la \_ sécurité du système \_**</span><span class="sxs-lookup"><span data-stu-id="d025c-203">**ACCESS\_SYSTEM\_SECURITY**</span></span> | <span data-ttu-id="d025c-204">Requis pour appeler la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) ou [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour accéder à la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="d025c-204">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) or [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to access the SACL.</span></span> <span data-ttu-id="d025c-205">La méthode appropriée pour obtenir cet accès consiste à activer le [**privilège**](/windows/desktop/SecAuthZ/privileges) **\_ \_ nom de sécurité se** dans le jeton d’accès actuel de l’appelant, à ouvrir le handle pour accès à la **\_ \_ sécurité du système** , puis à désactiver le privilège.</span><span class="sxs-lookup"><span data-stu-id="d025c-205">The proper way to obtain this access is to enable the **SE\_SECURITY\_NAME**[**privilege**](/windows/desktop/SecAuthZ/privileges) in the caller's current access token, open the handle for **ACCESS\_SYSTEM\_SECURITY** access, and then disable the privilege.</span></span> |
| <span data-ttu-id="d025c-206">**Supprimer**   (0x10000)</span><span class="sxs-lookup"><span data-stu-id="d025c-206">**DELETE**   (0x10000)</span></span>       | <span data-ttu-id="d025c-207">Requis pour appeler la fonction [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) pour supprimer le service.</span><span class="sxs-lookup"><span data-stu-id="d025c-207">Required to call the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to delete the service.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d025c-208">**Lecture \_ CONTRÔLE**  (0x20000)</span><span class="sxs-lookup"><span data-stu-id="d025c-208">**READ\_CONTROL**  (0x20000)</span></span>    | <span data-ttu-id="d025c-209">Requis pour appeler la fonction [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) pour interroger le descripteur de sécurité de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-209">Required to call the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) function to query the security descriptor of the service object.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d025c-210">**Écriture \_ DAC**  (0x40000)</span><span class="sxs-lookup"><span data-stu-id="d025c-210">**WRITE\_DAC**  (0x40000)</span></span>    | <span data-ttu-id="d025c-211">Requis pour appeler la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour modifier le membre **DACL** du descripteur de sécurité de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-211">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Dacl** member of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d025c-212">**Écriture \_ PROPRIÉTAIRE** (0x80000)</span><span class="sxs-lookup"><span data-stu-id="d025c-212">**WRITE\_OWNER** (0x80000)</span></span>   | <span data-ttu-id="d025c-213">Requis pour appeler la fonction [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) pour modifier les membres **propriétaire** et **groupe** du descripteur de sécurité de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-213">Required to call the [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) function to modify the **Owner** and **Group** members of the service object's security descriptor.</span></span>                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="d025c-214">Les [droits d’accès génériques](/windows/desktop/SecAuthZ/generic-access-rights) pour un service sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d025c-214">The following are the [generic access rights](/windows/desktop/SecAuthZ/generic-access-rights) for a service.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d025c-215">Droit d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-215">Access right</span></span></th>
<th><span data-ttu-id="d025c-216">Description</span><span class="sxs-lookup"><span data-stu-id="d025c-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d025c-217"><strong>GENERIC_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-217"><strong>GENERIC_READ</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-218"><strong>STANDARD_RIGHTS_READ</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-218"><strong>STANDARD_RIGHTS_READ</strong></span></span><br /><span data-ttu-id="d025c-219">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-219">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="d025c-220">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-220">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="d025c-221">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-221">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="d025c-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-222">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-223"><strong>GENERIC_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-223"><strong>GENERIC_WRITE</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-224"><strong>STANDARD_RIGHTS_WRITE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-224"><strong>STANDARD_RIGHTS_WRITE</strong></span></span><br /><span data-ttu-id="d025c-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-225">
<strong>SERVICE_CHANGE_CONFIG</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d025c-226"><strong>GENERIC_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-226"><strong>GENERIC_EXECUTE</strong></span></span></td>
<td><dl> <span data-ttu-id="d025c-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-227"><strong>STANDARD_RIGHTS_EXECUTE</strong></span></span><br /><span data-ttu-id="d025c-228">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-228">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="d025c-229">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-229">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="d025c-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-230">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="d025c-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-231">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d025c-232">Le SCM crée le descripteur de sécurité d’un objet de service lorsque le service est installé par la fonction [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) .</span><span class="sxs-lookup"><span data-stu-id="d025c-232">The SCM creates a service object's security descriptor when the service is installed by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function.</span></span> <span data-ttu-id="d025c-233">Le descripteur de sécurité par défaut d’un objet de service accorde l’accès suivant.</span><span class="sxs-lookup"><span data-stu-id="d025c-233">The default security descriptor of a service object grants the following access.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d025c-234">Compte</span><span class="sxs-lookup"><span data-stu-id="d025c-234">Account</span></span></th>
<th><span data-ttu-id="d025c-235">Droits d’accès</span><span class="sxs-lookup"><span data-stu-id="d025c-235">Access rights</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d025c-236">Utilisateurs authentifiés distants</span><span class="sxs-lookup"><span data-stu-id="d025c-236">Remote authenticated users</span></span></td>
<td><span data-ttu-id="d025c-237">Non accordé par défaut. <strong>Windows Server 2003 avec SP1 : SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-237">Not granted by default.<strong>Windows Server 2003 with SP1:  SERVICE_USER_DEFINED_CONTROL</strong></span></span><br/> <span data-ttu-id="d025c-238"><strong>Windows Server 2003 et Windows XP :</strong> Les droits d’accès pour les utilisateurs authentifiés distants sont les mêmes que pour les utilisateurs authentifiés locaux.</span><span class="sxs-lookup"><span data-stu-id="d025c-238"><strong>Windows Server 2003 and Windows XP:</strong> The access rights for remote authenticated users are the same as for local authenticated users.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-239">Utilisateurs authentifiés locaux (y compris LocalService et NetworkService)</span><span class="sxs-lookup"><span data-stu-id="d025c-239">Local authenticated users (including LocalService and NetworkService)</span></span></td>
<td><dl> <span data-ttu-id="d025c-240"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-240"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="d025c-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-241">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="d025c-242">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-242">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="d025c-243">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-243">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="d025c-244">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-244">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="d025c-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-245">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d025c-246">LocalSystem</span><span class="sxs-lookup"><span data-stu-id="d025c-246">LocalSystem</span></span></td>
<td><dl> <span data-ttu-id="d025c-247"><strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-247"><strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="d025c-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-248">
<strong>SERVICE_ENUMERATE_DEPENDENTS</strong></span></span><br /><span data-ttu-id="d025c-249">
<strong>SERVICE_INTERROGATE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-249">
<strong>SERVICE_INTERROGATE</strong></span></span><br /><span data-ttu-id="d025c-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-250">
<strong>SERVICE_PAUSE_CONTINUE</strong></span></span><br /><span data-ttu-id="d025c-251">
<strong>SERVICE_QUERY_CONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-251">
<strong>SERVICE_QUERY_CONFIG</strong></span></span><br /><span data-ttu-id="d025c-252">
<strong>SERVICE_QUERY_STATUS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-252">
<strong>SERVICE_QUERY_STATUS</strong></span></span><br /><span data-ttu-id="d025c-253">
<strong>SERVICE_START</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-253">
<strong>SERVICE_START</strong></span></span><br /><span data-ttu-id="d025c-254">
<strong>SERVICE_STOP</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-254">
<strong>SERVICE_STOP</strong></span></span><br /><span data-ttu-id="d025c-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-255">
<strong>SERVICE_USER_DEFINED_CONTROL</strong></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d025c-256">Administrateurs</span><span class="sxs-lookup"><span data-stu-id="d025c-256">Administrators</span></span></td>
<td><dl> <span data-ttu-id="d025c-257"><strong>DELETE</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-257"><strong>DELETE</strong></span></span><br /><span data-ttu-id="d025c-258">
<strong>READ_CONTROL</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-258">
<strong>READ_CONTROL</strong></span></span><br /><span data-ttu-id="d025c-259">
<strong>SERVICE_ALL_ACCESS</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-259">
<strong>SERVICE_ALL_ACCESS</strong></span></span><br /><span data-ttu-id="d025c-260">
<strong>WRITE_DAC</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-260">
<strong>WRITE_DAC</strong></span></span><br /><span data-ttu-id="d025c-261">
<strong>WRITE_OWNER</strong></span><span class="sxs-lookup"><span data-stu-id="d025c-261">
<strong>WRITE_OWNER</strong></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d025c-262">Pour effectuer des opérations, l’utilisateur doit être connecté de manière interactive ou le service doit utiliser l’un des comptes de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-262">To perform any operations, the user must be logged on interactively or the service must use one of the service accounts.</span></span>

<span data-ttu-id="d025c-263">Pour obtenir ou définir le descripteur de sécurité d’un objet de service, utilisez les fonctions [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) et [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) .</span><span class="sxs-lookup"><span data-stu-id="d025c-263">To get or set the security descriptor for a service object, use the [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) and [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) functions.</span></span> <span data-ttu-id="d025c-264">Pour plus d’informations, consultez [modification de la liste DACL pour un service](modifying-the-dacl-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="d025c-264">For more information, see [Modifying the DACL for a Service](modifying-the-dacl-for-a-service.md).</span></span>

<span data-ttu-id="d025c-265">Lorsqu’un processus utilise la fonction [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) , le système vérifie les droits d’accès demandés par rapport au descripteur de sécurité de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="d025c-265">When a process uses the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) function, the system checks the requested access rights against the security descriptor for the service object.</span></span>

<span data-ttu-id="d025c-266">L’octroi de certains droits d’accès à des utilisateurs non approuvés (tels que la **\_ \_ configuration** de la modification du service ou l' **\_ arrêt du service**) peut leur permettre d’interférer avec l’exécution de votre service et éventuellement de les autoriser à exécuter des applications sous le compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="d025c-266">Granting certain access rights to untrusted users (such as **SERVICE\_CHANGE\_CONFIG** or **SERVICE\_STOP**) can allow them to interfere with the execution of your service, and possibly allow them to run applications under the LocalSystem account.</span></span>

<span data-ttu-id="d025c-267">Quand la [**fonction EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) est appelée, si l’appelant n’a pas le droit d’accès à l’état de la **\_ requête \_ de service** à un service, le service est omis en mode silencieux de la liste des services renvoyés au client.</span><span class="sxs-lookup"><span data-stu-id="d025c-267">When [**EnumServicesStatusEx function**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) is called, if the caller does not have the **SERVICE\_QUERY\_STATUS** access right to a service, the service is silently omitted from the list of services returned to the client.</span></span>

 

