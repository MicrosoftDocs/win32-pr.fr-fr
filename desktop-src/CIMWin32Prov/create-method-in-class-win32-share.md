---
description: Lance le partage pour une ressource de serveur.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Créer une méthode de la classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950871"
---
# <a name="create-method-of-the-win32_share-class"></a><span data-ttu-id="5f174-103">Créer une méthode de la \_ classe de partage Win32</span><span class="sxs-lookup"><span data-stu-id="5f174-103">Create method of the Win32\_Share class</span></span>

<span data-ttu-id="5f174-104">La méthode **Create**   [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) lance le partage pour une ressource de serveur.</span><span class="sxs-lookup"><span data-stu-id="5f174-104">The **Create**   [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method initiates sharing for a server resource.</span></span>

<span data-ttu-id="5f174-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5f174-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5f174-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5f174-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5f174-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f174-107">Syntax</span></span>


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="5f174-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f174-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f174-109">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f174-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-110">Chemin d’accès local du partage Windows.</span><span class="sxs-lookup"><span data-stu-id="5f174-110">Local path of the Windows share.</span></span>

<span data-ttu-id="5f174-111">Par exemple, « C : \\ Program Files ».</span><span class="sxs-lookup"><span data-stu-id="5f174-111">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="5f174-112">*Nom* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f174-112">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-113">Transmet l’alias à un chemin d’accès configuré en tant que partage sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="5f174-113">Passes the alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="5f174-114">Exemple : « public ».</span><span class="sxs-lookup"><span data-stu-id="5f174-114">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="5f174-115">*Type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5f174-115">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-116">Passe le type de ressource partagé.</span><span class="sxs-lookup"><span data-stu-id="5f174-116">Passes the type of resource being shared.</span></span> <span data-ttu-id="5f174-117">Les types incluent des lecteurs de disque, des files d’attente à l’impression, des communications interprocessus (IPC) et des périphériques généraux.</span><span class="sxs-lookup"><span data-stu-id="5f174-117">Types includes disk drives, print queues, interprocess communications (IPC), and general devices.</span></span> <span data-ttu-id="5f174-118">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="5f174-118">Can be one of the following values.</span></span>

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="5f174-119">**Lecteur de disque** (0)</span><span class="sxs-lookup"><span data-stu-id="5f174-119">**Disk Drive** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

<span data-ttu-id="5f174-120">**File d’attente** à l’impression (1)</span><span class="sxs-lookup"><span data-stu-id="5f174-120">**Print Queue** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

<span data-ttu-id="5f174-121">**Appareil** (2)</span><span class="sxs-lookup"><span data-stu-id="5f174-121">**Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

<span data-ttu-id="5f174-122">**IPC** (3)</span><span class="sxs-lookup"><span data-stu-id="5f174-122">**IPC** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

<span data-ttu-id="5f174-123">**Administrateur de lecteur de disque** (2147483648)</span><span class="sxs-lookup"><span data-stu-id="5f174-123">**Disk Drive Admin** (2147483648)</span></span>


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

<span data-ttu-id="5f174-124">**Administrateur de file d’attente** à l’impression (2147483649)</span><span class="sxs-lookup"><span data-stu-id="5f174-124">**Print Queue Admin** (2147483649)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

<span data-ttu-id="5f174-125">**Administrateur d’appareil** (2147483650)</span><span class="sxs-lookup"><span data-stu-id="5f174-125">**Device Admin** (2147483650)</span></span>


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

<span data-ttu-id="5f174-126">**Administrateur IPC** (2147483651)</span><span class="sxs-lookup"><span data-stu-id="5f174-126">**IPC Admin** (2147483651)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="5f174-127">*MaximumAllowed* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5f174-127">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-128">Limite du nombre maximal d’utilisateurs autorisés à utiliser simultanément cette ressource.</span><span class="sxs-lookup"><span data-stu-id="5f174-128">Limit on the maximum number of users allowed to concurrently use this resource.</span></span>

<span data-ttu-id="5f174-129">Exemple : 10.</span><span class="sxs-lookup"><span data-stu-id="5f174-129">Example: 10.</span></span> <span data-ttu-id="5f174-130">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f174-130">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5f174-131">*Description* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5f174-131">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-132">Commentaire facultatif pour décrire la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="5f174-132">Optional comment to describe the resource being shared.</span></span> <span data-ttu-id="5f174-133">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f174-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5f174-134">*Mot de passe* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5f174-134">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-135">Mot de passe (lorsque le serveur s’exécute avec la sécurité au niveau du partage) pour la ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="5f174-135">Password (when the server is running with share-level security) for the shared resource.</span></span> <span data-ttu-id="5f174-136">Si le serveur s’exécute avec la sécurité au niveau de l’utilisateur, ce paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="5f174-136">If the server is running with user-level security, this parameter is ignored.</span></span> <span data-ttu-id="5f174-137">Ce paramètre est facultatif.</span><span class="sxs-lookup"><span data-stu-id="5f174-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="5f174-138">*Accès* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5f174-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f174-139">Descripteur de sécurité pour les autorisations au niveau de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5f174-139">Security descriptor for user level permissions.</span></span> <span data-ttu-id="5f174-140">Un descripteur de sécurité contient des informations sur les autorisations, le propriétaire et les capacités d’accès de la ressource.</span><span class="sxs-lookup"><span data-stu-id="5f174-140">A security descriptor contains information about the permissions, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="5f174-141">Si ce paramètre n’est pas fourni ou a la **valeur null**, tout le monde dispose d’un accès en lecture au partage.</span><span class="sxs-lookup"><span data-stu-id="5f174-141">If this parameter is not supplied or is **NULL**, then Everyone has read access to the share.</span></span> <span data-ttu-id="5f174-142">Pour plus d’informations, [**consultez \_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) et [modification de la sécurité d’accès sur des objets sécurisables](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="5f174-142">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) and [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f174-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5f174-143">Return value</span></span>

<span data-ttu-id="5f174-144">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="5f174-144">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="5f174-145">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="5f174-145">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5f174-146">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="5f174-146">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5f174-147">**Opération réussie** (0)</span><span class="sxs-lookup"><span data-stu-id="5f174-147">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-148">**Accès refusé** (2)</span><span class="sxs-lookup"><span data-stu-id="5f174-148">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-149">**Échec inconnu** (8)</span><span class="sxs-lookup"><span data-stu-id="5f174-149">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-150">**Nom non valide** (9)</span><span class="sxs-lookup"><span data-stu-id="5f174-150">**Invalid name** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-151">**Niveau non valide** (10)</span><span class="sxs-lookup"><span data-stu-id="5f174-151">**Invalid level** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-152">**Paramètre non valide** (21)</span><span class="sxs-lookup"><span data-stu-id="5f174-152">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-153">**Partage en double** (22)</span><span class="sxs-lookup"><span data-stu-id="5f174-153">**Duplicate share** (22)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-154">**Chemin d’accès Redirigé** (23)</span><span class="sxs-lookup"><span data-stu-id="5f174-154">**Redirected path** (23)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-155">**Périphérique ou répertoire inconnu** (24)</span><span class="sxs-lookup"><span data-stu-id="5f174-155">**Unknown device or directory** (24)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-156">**Nom de réseau introuvable** (25)</span><span class="sxs-lookup"><span data-stu-id="5f174-156">**Net name not found** (25)</span></span>
</dt> <dt>

<span data-ttu-id="5f174-157">**Autre** (26 4294967295)</span><span class="sxs-lookup"><span data-stu-id="5f174-157">**Other** (26 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="5f174-158">Notes</span><span class="sxs-lookup"><span data-stu-id="5f174-158">Remarks</span></span>

<span data-ttu-id="5f174-159">**Create** est une méthode statique.</span><span class="sxs-lookup"><span data-stu-id="5f174-159">**Create** is a static method.</span></span>

<span data-ttu-id="5f174-160">Seuls les membres du groupe local Administrateurs ou opérateurs de compte ou ceux ayant une appartenance de groupe communication, impression ou opérateur de serveur peuvent exécuter la **création**.</span><span class="sxs-lookup"><span data-stu-id="5f174-160">Only members of the Administrators or Account Operators local group or those with Communication, Print, or Server operator group membership can successfully execute **Create**.</span></span> <span data-ttu-id="5f174-161">L’opérateur Print peut uniquement ajouter des files d’attente d’impression.</span><span class="sxs-lookup"><span data-stu-id="5f174-161">The Print operator can only add printer queues.</span></span> <span data-ttu-id="5f174-162">L’opérateur de communication peut uniquement ajouter des files d’attente d’appareils de communication.</span><span class="sxs-lookup"><span data-stu-id="5f174-162">The Communication operator can only add communication device queues.</span></span>

## <a name="examples"></a><span data-ttu-id="5f174-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="5f174-163">Examples</span></span>

<span data-ttu-id="5f174-164">L’exemple d' [exportation et d’importation partages](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell exporte et importe des partages de fichiers et définit des autorisations de partage.</span><span class="sxs-lookup"><span data-stu-id="5f174-164">The [Export and Import Fileshares](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell sample exports and imports file shares and sets share permissions.</span></span> <span data-ttu-id="5f174-165">De même, l’exemple [créer un partage et définir des autorisations](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) crée également un nouveau partage et définit les autorisations de partage.</span><span class="sxs-lookup"><span data-stu-id="5f174-165">Similarly, the [Create a Share and Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) sample also creates a new share and sets the share permissions.</span></span>

<span data-ttu-id="5f174-166">Le code PowerShell suivant crée un partage.</span><span class="sxs-lookup"><span data-stu-id="5f174-166">The following PowerShell code creates a share.</span></span>


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



<span data-ttu-id="5f174-167">L’exemple de code précédent retourne ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5f174-167">The previous code sample returns the following:</span></span>

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

<span data-ttu-id="5f174-168">L' \# exemple de code C suivant décrit comment appeler la méthode Create.</span><span class="sxs-lookup"><span data-stu-id="5f174-168">The following C\# code sample describe how to call the create method.</span></span>


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
```



## <a name="requirements"></a><span data-ttu-id="5f174-169">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f174-169">Requirements</span></span>



| <span data-ttu-id="5f174-170">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f174-170">Requirement</span></span> | <span data-ttu-id="5f174-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f174-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f174-172">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f174-172">Minimum supported client</span></span><br/> | <span data-ttu-id="5f174-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f174-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5f174-174">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f174-174">Minimum supported server</span></span><br/> | <span data-ttu-id="5f174-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f174-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5f174-176">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5f174-176">Namespace</span></span><br/>                | <span data-ttu-id="5f174-177">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5f174-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5f174-178">MOF</span><span class="sxs-lookup"><span data-stu-id="5f174-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f174-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f174-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f174-180">DLL</span><span class="sxs-lookup"><span data-stu-id="5f174-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f174-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f174-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f174-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f174-182">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f174-183">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f174-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5f174-184">**\_Partage Win32**</span><span class="sxs-lookup"><span data-stu-id="5f174-184">**Win32\_Share**</span></span>](win32-share.md)
</dt> </dl>

 

