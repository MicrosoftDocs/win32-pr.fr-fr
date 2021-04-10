---
description: La suppression&\# 8194 ; La méthode de classe WMI supprime un service existant.
ms.assetid: aa4e7630-3b19-47dd-acd1-4d1735acb819
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d06301c3620e144d72c2d4c4f3d8bc90e642374a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201016"
---
# <a name="delete-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="b183c-103">Méthode Delete de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b183c-103">Delete method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b183c-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="b183c-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="b183c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b183c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b183c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b183c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b183c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b183c-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="b183c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b183c-108">Parameters</span></span>

<span data-ttu-id="b183c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b183c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b183c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b183c-110">Return value</span></span>

<span data-ttu-id="b183c-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b183c-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b183c-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b183c-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b183c-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b183c-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b183c-114">**0**</span><span class="sxs-lookup"><span data-stu-id="b183c-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="b183c-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-116">**1**</span><span class="sxs-lookup"><span data-stu-id="b183c-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b183c-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-118">**2**</span><span class="sxs-lookup"><span data-stu-id="b183c-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b183c-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-120">**3**</span><span class="sxs-lookup"><span data-stu-id="b183c-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="b183c-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-122">**4**</span><span class="sxs-lookup"><span data-stu-id="b183c-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="b183c-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-124">**5**</span><span class="sxs-lookup"><span data-stu-id="b183c-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b183c-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-126">**6**</span><span class="sxs-lookup"><span data-stu-id="b183c-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="b183c-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-128">**7**</span><span class="sxs-lookup"><span data-stu-id="b183c-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="b183c-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-130">**8**</span><span class="sxs-lookup"><span data-stu-id="b183c-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="b183c-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-132">**9**</span><span class="sxs-lookup"><span data-stu-id="b183c-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b183c-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-134">**10**</span><span class="sxs-lookup"><span data-stu-id="b183c-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="b183c-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-136">**11**</span><span class="sxs-lookup"><span data-stu-id="b183c-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="b183c-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-138">**12**</span><span class="sxs-lookup"><span data-stu-id="b183c-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="b183c-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-140">**13**</span><span class="sxs-lookup"><span data-stu-id="b183c-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="b183c-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-142">**14**</span><span class="sxs-lookup"><span data-stu-id="b183c-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="b183c-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-144">**15**</span><span class="sxs-lookup"><span data-stu-id="b183c-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="b183c-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-146">**16**</span><span class="sxs-lookup"><span data-stu-id="b183c-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="b183c-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-148">**17**</span><span class="sxs-lookup"><span data-stu-id="b183c-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b183c-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-150">**19**</span><span class="sxs-lookup"><span data-stu-id="b183c-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="b183c-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-152">**19**</span><span class="sxs-lookup"><span data-stu-id="b183c-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="b183c-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-154">**20**</span><span class="sxs-lookup"><span data-stu-id="b183c-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="b183c-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-156">**21**</span><span class="sxs-lookup"><span data-stu-id="b183c-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="b183c-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-158">**22**</span><span class="sxs-lookup"><span data-stu-id="b183c-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="b183c-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-160">**23**</span><span class="sxs-lookup"><span data-stu-id="b183c-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="b183c-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b183c-162">**24**</span><span class="sxs-lookup"><span data-stu-id="b183c-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b183c-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="b183c-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b183c-164">Notes</span><span class="sxs-lookup"><span data-stu-id="b183c-164">Remarks</span></span>

<span data-ttu-id="b183c-165">À mesure que votre organisation change, vous pouvez décider de supprimer certains services de certains ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="b183c-165">As your organization changes, you might decide to remove certain services from certain computers.</span></span> <span data-ttu-id="b183c-166">Les services internes et tiers peuvent être supprimés à l’aide de WMI, tandis que les services du système d’exploitation peuvent être supprimés à l’aide de Sysocmgr.exe.</span><span class="sxs-lookup"><span data-stu-id="b183c-166">In-house and third-party services can be removed by using WMI, while operating system services can be removed by using Sysocmgr.exe.</span></span>

<span data-ttu-id="b183c-167">Lorsque vous vous préparez à supprimer des services, gardez à l’esprit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b183c-167">When preparing to remove services, keep the following information in mind:</span></span>

-   <span data-ttu-id="b183c-168">Les services doivent être arrêtés avant de les supprimer.</span><span class="sxs-lookup"><span data-stu-id="b183c-168">Services must be stopped before you remove them.</span></span> <span data-ttu-id="b183c-169">Si le service est en cours d’exécution lorsque vous exécutez la commande Delete, le service est marqué pour suppression, mais il continue à s’exécuter jusqu’à ce qu’il s’arrête et que tous les descripteurs ouverts soient fermés.</span><span class="sxs-lookup"><span data-stu-id="b183c-169">If the service is running when you issue the delete command, the service is marked for deletion, but it continues to run until it stops and all open handles are closed.</span></span>

    <span data-ttu-id="b183c-170">Si le service n’est jamais arrêté, ce service ne sera jamais supprimé.</span><span class="sxs-lookup"><span data-stu-id="b183c-170">If the service is never stopped, that service will never be deleted.</span></span>

-   <span data-ttu-id="b183c-171">La suppression d’un service ne supprime pas le fichier exécutable du service.</span><span class="sxs-lookup"><span data-stu-id="b183c-171">Removing a service does not remove the service's executable file.</span></span>

    <span data-ttu-id="b183c-172">La suppression d’un service à l’aide de WMI supprime les entrées de Registre associées sous HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services.</span><span class="sxs-lookup"><span data-stu-id="b183c-172">Removing a service by using WMI deletes the related registry entries under HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services.</span></span> <span data-ttu-id="b183c-173">Par conséquent, le service n’est plus installé et n’est pas disponible via le composant logiciel enfichable Services.</span><span class="sxs-lookup"><span data-stu-id="b183c-173">As a result, the service is no longer installed and is not available through the Services snap-in.</span></span> <span data-ttu-id="b183c-174">Toutefois, WMI ne supprime pas le fichier exécutable, ce qui signifie que vous pouvez facilement réinstaller le service.</span><span class="sxs-lookup"><span data-stu-id="b183c-174">However, WMI does not delete the executable file, meaning you could easily reinstall the service.</span></span> <span data-ttu-id="b183c-175">Pour supprimer le fichier exécutable, vous devez récupérer le nom du chemin d’accès, puis supprimer le fichier.</span><span class="sxs-lookup"><span data-stu-id="b183c-175">To delete the executable file, you must retrieve the path name and then delete the file.</span></span>

-   <span data-ttu-id="b183c-176">La suppression d’un service Windows 2000 de base (par exemple, DHCP) à l’aide de WMI supprime les entrées de Registre pour ce service, mais ne supprime pas le raccourci du menu Outils d’administration ou supprime le service de l’Assistant composants de Windows.</span><span class="sxs-lookup"><span data-stu-id="b183c-176">Removing a base Windows 2000 service (for example, DHCP) by using WMI deletes the registry entries for that service but does not remove the shortcut from the Administrative Tools menu or remove the service from the Windows Components Wizard.</span></span> <span data-ttu-id="b183c-177">Cela peut dérouter quiconque tente de déterminer la façon dont l’ordinateur a été configuré.</span><span class="sxs-lookup"><span data-stu-id="b183c-177">This can confuse anyone trying to determine how the computer has been configured.</span></span>

    <span data-ttu-id="b183c-178">Par exemple, si vous supprimez le service DHCP à l’aide d’un script WMI, le service DHCP n’est plus listé dans le composant logiciel enfichable Services.</span><span class="sxs-lookup"><span data-stu-id="b183c-178">For example, if you remove the DHCP service by using a WMI script, the DHCP service is no longer listed in the Services snap-in.</span></span> <span data-ttu-id="b183c-179">Toutefois, un raccourci de non-fonctionnement vers la console DHCP reste dans le menu Outils d’administration. Si vous démarrez l’Assistant composants de Windows, il indique que le service DHCP est installé.</span><span class="sxs-lookup"><span data-stu-id="b183c-179">However, a nonfunctioning shortcut to the DHCP console remains in the Administrative Tools menu, and if you start the Windows Component Wizard, it indicates that the DHCP service is installed.</span></span>

    <span data-ttu-id="b183c-180">Pour cette raison, vous devez toujours utiliser Sysocmgr.exe pour supprimer par programme les services Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b183c-180">Because of this, you should always use Sysocmgr.exe to programmatically remove Windows 2000 services.</span></span>

## <a name="examples"></a><span data-ttu-id="b183c-181">Exemples</span><span class="sxs-lookup"><span data-stu-id="b183c-181">Examples</span></span>

<span data-ttu-id="b183c-182">L’exemple de code VBScript suivant décrit comment supprimer un service.</span><span class="sxs-lookup"><span data-stu-id="b183c-182">The following VBScript code sample describes how to delete a service.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colListOfServices = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Service WHERE Name = 'DbService'")
For Each objService in colListOfServices
 objService.StopService()
 objService.Delete()
Next
```



<span data-ttu-id="b183c-183">L’exemple de code perl suivant décrit comment supprimer un service.</span><span class="sxs-lookup"><span data-stu-id="b183c-183">The following Perl code sample describes how to delete a service.</span></span>


```
use strict;
use Win32::OLE;

my ($Service, $ServiceSet) ;
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='MyService'");};
unless($@)
{
 foreach $Service (in $ServiceSet)
 {
  my $RetVal = $Service->Delete();
  if ($RetVal == 0)  
  {
   print "Service deleted \n"; 
  }
  else  
  {
   print "Delete failed: %d", $RetVal;
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="b183c-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b183c-184">Requirements</span></span>



| <span data-ttu-id="b183c-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b183c-185">Requirement</span></span> | <span data-ttu-id="b183c-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="b183c-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b183c-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b183c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="b183c-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b183c-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b183c-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b183c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="b183c-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b183c-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b183c-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b183c-191">Namespace</span></span><br/>                | <span data-ttu-id="b183c-192">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b183c-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b183c-193">MOF</span><span class="sxs-lookup"><span data-stu-id="b183c-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b183c-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b183c-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b183c-195">DLL</span><span class="sxs-lookup"><span data-stu-id="b183c-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b183c-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b183c-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b183c-197">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b183c-197">See also</span></span>

<dl> <dt>

<span data-ttu-id="b183c-198">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b183c-198">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b183c-199">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="b183c-199">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="b183c-200">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="b183c-200">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

