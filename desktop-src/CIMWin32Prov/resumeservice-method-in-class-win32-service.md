---
description: 'Méthode ResumeService de la classe Win32_Service (fournisseurs WMI CIMWin32) : tente de placer le service référencé dans l’État repris.'
ms.assetid: 3b4228bf-9ff5-44ab-bfe2-f7dd8fb62007
ms.tgt_platform: multiple
title: Méthode ResumeService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73c21f282577207b63bcfa2d624c59ddfa3c9bcb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090977"
---
# <a name="resumeservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="41370-103">Méthode ResumeService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="41370-103">ResumeService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="41370-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tente de placer le service référencé dans l’État repris.</span><span class="sxs-lookup"><span data-stu-id="41370-104">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="41370-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="41370-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="41370-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="41370-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="41370-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41370-107">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="41370-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41370-108">Parameters</span></span>

<span data-ttu-id="41370-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="41370-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41370-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41370-110">Return value</span></span>

<span data-ttu-id="41370-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="41370-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="41370-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="41370-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="41370-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="41370-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="41370-114">**0**</span><span class="sxs-lookup"><span data-stu-id="41370-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="41370-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="41370-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="41370-116">**1**</span><span class="sxs-lookup"><span data-stu-id="41370-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="41370-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="41370-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="41370-118">**2**</span><span class="sxs-lookup"><span data-stu-id="41370-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="41370-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="41370-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="41370-120">**3**</span><span class="sxs-lookup"><span data-stu-id="41370-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="41370-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="41370-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="41370-122">**4**</span><span class="sxs-lookup"><span data-stu-id="41370-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="41370-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="41370-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41370-124">**5**</span><span class="sxs-lookup"><span data-stu-id="41370-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="41370-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="41370-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="41370-126">**6**</span><span class="sxs-lookup"><span data-stu-id="41370-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="41370-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="41370-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="41370-128">**7**</span><span class="sxs-lookup"><span data-stu-id="41370-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="41370-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="41370-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="41370-130">**8**</span><span class="sxs-lookup"><span data-stu-id="41370-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="41370-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="41370-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="41370-132">**9**</span><span class="sxs-lookup"><span data-stu-id="41370-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="41370-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="41370-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="41370-134">**10**</span><span class="sxs-lookup"><span data-stu-id="41370-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="41370-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="41370-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="41370-136">**11**</span><span class="sxs-lookup"><span data-stu-id="41370-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="41370-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="41370-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="41370-138">**12**</span><span class="sxs-lookup"><span data-stu-id="41370-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="41370-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="41370-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41370-140">**13**</span><span class="sxs-lookup"><span data-stu-id="41370-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="41370-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="41370-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="41370-142">**14**</span><span class="sxs-lookup"><span data-stu-id="41370-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="41370-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="41370-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41370-144">**15**</span><span class="sxs-lookup"><span data-stu-id="41370-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="41370-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="41370-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="41370-146">**16**</span><span class="sxs-lookup"><span data-stu-id="41370-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="41370-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="41370-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41370-148">**17**</span><span class="sxs-lookup"><span data-stu-id="41370-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="41370-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41370-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="41370-150">**19**</span><span class="sxs-lookup"><span data-stu-id="41370-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="41370-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="41370-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="41370-152">**19**</span><span class="sxs-lookup"><span data-stu-id="41370-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="41370-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="41370-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="41370-154">**20**</span><span class="sxs-lookup"><span data-stu-id="41370-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="41370-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="41370-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="41370-156">**21**</span><span class="sxs-lookup"><span data-stu-id="41370-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="41370-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="41370-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41370-158">**22**</span><span class="sxs-lookup"><span data-stu-id="41370-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="41370-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="41370-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="41370-160">**23**</span><span class="sxs-lookup"><span data-stu-id="41370-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="41370-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="41370-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41370-162">**24**</span><span class="sxs-lookup"><span data-stu-id="41370-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="41370-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="41370-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41370-164">Notes </span><span class="sxs-lookup"><span data-stu-id="41370-164">Remarks</span></span>

<span data-ttu-id="41370-165">Bien qu’il puisse sembler qu’il n’y ait aucune différence pratique entre un service arrêté et un service suspendu, les deux États apparaissent différemment pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="41370-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="41370-166">Un service arrêté est un service qui n’est pas en cours d’exécution et doit suivre l’intégralité de la procédure de démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="41370-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="41370-167">Toutefois, un service suspendu est toujours en cours d’exécution, mais son fonctionnement est suspendu.</span><span class="sxs-lookup"><span data-stu-id="41370-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="41370-168">Pour cette raison, un service suspendu n’a pas besoin de traverser l’intégralité de la procédure de démarrage du service, mais il a besoin d’une procédure différente pour reprendre son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="41370-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="41370-169">Vous devez utiliser la méthode appropriée pour démarrer un service qui a été arrêté ou pour reprendre un service qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="41370-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="41370-170">Les méthodes de [**\_ service Win32**](win32-service.md) [**StartService**](startservice-method-in-class-win32-service.md) et **ResumeService** doivent être utilisées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="41370-170">The [**Win32\_Service**](win32-service.md) methods [**StartService**](startservice-method-in-class-win32-service.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="41370-171">Si un service est actuellement arrêté, vous devez utiliser la méthode [**StartService**](startservice-method-in-class-win32-service.md) pour le redémarrer ; **ResumeService** ne peut pas démarrer un service qui est actuellement arrêté.</span><span class="sxs-lookup"><span data-stu-id="41370-171">If a service is currently stopped, you must use the [**StartService**](startservice-method-in-class-win32-service.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="41370-172">Si un service est suspendu, vous devez utiliser **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="41370-172">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="41370-173">Si vous utilisez la méthode [**StartService**](startservice-method-in-class-win32-service.md) sur un service suspendu, vous recevez le message « le service est déjà en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="41370-173">If you use the [**StartService**](startservice-method-in-class-win32-service.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="41370-174">Toutefois, le service reste en pause jusqu’à ce que le code de contrôle de reprise du service lui soit envoyé.</span><span class="sxs-lookup"><span data-stu-id="41370-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="41370-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="41370-175">Examples</span></span>

<span data-ttu-id="41370-176">L’exemple de [reprise des services AutoStart qui sont en pause](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript redémarre tous les services à démarrage automatique qui ont été suspendus.</span><span class="sxs-lookup"><span data-stu-id="41370-176">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

<span data-ttu-id="41370-177">L’exemple de code VBScript suivant décrit comment reprendre un service suspendu à partir d’instances [**du \_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="41370-177">The following VBScript code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="41370-178">Le service doit prendre en charge la suspension et être déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41370-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.ResumeService()
  if RetVal = 0 then 
   WScript.Echo "Service resumed"   
  else
   if RetVal = 1 then 
    WScript.Echo "Pause not supported" 
   else WScript.Echo "An error occurred:" & RetVal
   End If
  End If
 else
  WScript.Echo "Service does not support pause"
 end if
next
```



<span data-ttu-id="41370-179">L’exemple de code perl suivant décrit comment reprendre un service suspendu à partir d’instances [**du \_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="41370-179">The following Perl code sample describes how to resume a paused service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="41370-180">Le service doit prendre en charge la suspension et être déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41370-180">The service must support pausing and be running already.</span></span>

 


```Perl
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $Service (in $ServiceSet)
 {
  my $SupportsPause = $Service->{AcceptPause};
  if ($SupportsPause)
  {
   my $RetVal = $Service->ResumeService();
   if ($RetVal == 0)
   {
    print "\nService resumed\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print STDERR "\nPause not supported\n";
    }
    else
    {
     print STDERR "\nAn error occurred: ", $RetVal, "\n";
    }
   }
  }
  else
  {
   print "\nService does not support pause\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="41370-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41370-181">Requirements</span></span>



| <span data-ttu-id="41370-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41370-182">Requirement</span></span> | <span data-ttu-id="41370-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="41370-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41370-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41370-184">Minimum supported client</span></span><br/> | <span data-ttu-id="41370-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41370-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41370-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41370-186">Minimum supported server</span></span><br/> | <span data-ttu-id="41370-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41370-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41370-188">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41370-188">Namespace</span></span><br/>                | <span data-ttu-id="41370-189">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="41370-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="41370-190">MOF</span><span class="sxs-lookup"><span data-stu-id="41370-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41370-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41370-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41370-192">DLL</span><span class="sxs-lookup"><span data-stu-id="41370-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41370-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41370-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41370-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41370-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="41370-195">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41370-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="41370-196">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="41370-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="41370-197">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="41370-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

