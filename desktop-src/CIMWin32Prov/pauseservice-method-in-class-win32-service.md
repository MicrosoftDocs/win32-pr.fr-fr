---
description: 'Méthode PauseService de la classe Win32_Service (fournisseurs WMI CIMWin32) : tente de placer le service dans l’état suspendu.'
ms.assetid: 5382457e-7f9c-48a5-9262-b815a1a4a605
ms.tgt_platform: multiple
title: Méthode PauseService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.PauseService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7654feea410564137e98861c4c0b5de2b5e7192e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096947"
---
# <a name="pauseservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="22075-103">Méthode PauseService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="22075-103">PauseService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="22075-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tente de placer le service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="22075-104">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="22075-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="22075-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="22075-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="22075-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="22075-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22075-107">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="22075-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22075-108">Parameters</span></span>

<span data-ttu-id="22075-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="22075-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="22075-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="22075-110">Return value</span></span>

<span data-ttu-id="22075-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="22075-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="22075-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="22075-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="22075-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="22075-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="22075-114">**0**</span><span class="sxs-lookup"><span data-stu-id="22075-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="22075-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="22075-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="22075-116">**1**</span><span class="sxs-lookup"><span data-stu-id="22075-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="22075-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="22075-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="22075-118">**2**</span><span class="sxs-lookup"><span data-stu-id="22075-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="22075-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="22075-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="22075-120">**3**</span><span class="sxs-lookup"><span data-stu-id="22075-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="22075-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="22075-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="22075-122">**4**</span><span class="sxs-lookup"><span data-stu-id="22075-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="22075-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="22075-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="22075-124">**5**</span><span class="sxs-lookup"><span data-stu-id="22075-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="22075-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="22075-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="22075-126">**6**</span><span class="sxs-lookup"><span data-stu-id="22075-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="22075-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="22075-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="22075-128">**7**</span><span class="sxs-lookup"><span data-stu-id="22075-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="22075-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="22075-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="22075-130">**8**</span><span class="sxs-lookup"><span data-stu-id="22075-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="22075-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="22075-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="22075-132">**9**</span><span class="sxs-lookup"><span data-stu-id="22075-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="22075-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="22075-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="22075-134">**10**</span><span class="sxs-lookup"><span data-stu-id="22075-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="22075-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="22075-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="22075-136">**11**</span><span class="sxs-lookup"><span data-stu-id="22075-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="22075-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="22075-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="22075-138">**12**</span><span class="sxs-lookup"><span data-stu-id="22075-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="22075-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="22075-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="22075-140">**13**</span><span class="sxs-lookup"><span data-stu-id="22075-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="22075-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="22075-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="22075-142">**14**</span><span class="sxs-lookup"><span data-stu-id="22075-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="22075-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="22075-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="22075-144">**15**</span><span class="sxs-lookup"><span data-stu-id="22075-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="22075-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="22075-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="22075-146">**16**</span><span class="sxs-lookup"><span data-stu-id="22075-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="22075-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="22075-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="22075-148">**17**</span><span class="sxs-lookup"><span data-stu-id="22075-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="22075-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22075-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="22075-150">**19**</span><span class="sxs-lookup"><span data-stu-id="22075-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="22075-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="22075-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="22075-152">**19**</span><span class="sxs-lookup"><span data-stu-id="22075-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="22075-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="22075-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="22075-154">**20**</span><span class="sxs-lookup"><span data-stu-id="22075-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="22075-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="22075-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="22075-156">**21**</span><span class="sxs-lookup"><span data-stu-id="22075-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="22075-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="22075-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="22075-158">**22**</span><span class="sxs-lookup"><span data-stu-id="22075-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="22075-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="22075-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="22075-160">**23**</span><span class="sxs-lookup"><span data-stu-id="22075-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="22075-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="22075-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="22075-162">**24**</span><span class="sxs-lookup"><span data-stu-id="22075-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="22075-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="22075-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22075-164">Notes </span><span class="sxs-lookup"><span data-stu-id="22075-164">Remarks</span></span>

<span data-ttu-id="22075-165">Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes [**StopService**](stopservice-method-in-class-win32-service.md) et [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) pour arrêter et suspendre les services.</span><span class="sxs-lookup"><span data-stu-id="22075-165">After you have determined which services can be stopped or paused, you can use the [**StopService**](stopservice-method-in-class-win32-service.md) and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="22075-166">La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="22075-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="22075-167">Le service est-il susceptible d’être suspendu ?</span><span class="sxs-lookup"><span data-stu-id="22075-167">Is the service capable of being paused?</span></span> <span data-ttu-id="22075-168">Si ce n’est pas le cas, la seule option consiste à arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="22075-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="22075-169">Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ?</span><span class="sxs-lookup"><span data-stu-id="22075-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="22075-170">Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients.</span><span class="sxs-lookup"><span data-stu-id="22075-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="22075-171">En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.</span><span class="sxs-lookup"><span data-stu-id="22075-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="22075-172">Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="22075-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="22075-173">Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="22075-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="22075-174">Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.</span><span class="sxs-lookup"><span data-stu-id="22075-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="22075-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="22075-175">Examples</span></span>

<span data-ttu-id="22075-176">L’exemple de [suspension de services s’exécutant sous un compte spécifique](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) met en pause tous les services qui s’exécutent sous le compte de service hypothétique « netsvc ».</span><span class="sxs-lookup"><span data-stu-id="22075-176">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account "Netsvc".</span></span>

<span data-ttu-id="22075-177">L’exemple de code VBScript suivant montre comment suspendre un service spécifique à partir d’instances du [**\_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="22075-177">The following VBScript code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="22075-178">Le service doit prendre en charge la suspension et être déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22075-178">The service must support pausing and be running already.</span></span>

 


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='Schedule'")

for each Service in ServiceSet
 SupportsPause = Service.AcceptPause
 if SupportsPause = true then
  RetVal = Service.PauseService()
  if RetVal = 0 then 
   WScript.Echo "Service paused"   
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



<span data-ttu-id="22075-179">L’exemple de code perl suivant montre comment suspendre un service spécifique à partir d’instances du [**\_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="22075-179">The following Perl code sample demonstrates how to pause a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="22075-180">Le service doit prendre en charge la suspension et être déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22075-180">The service must support pausing and be running already.</span></span>

 


```
use strict;
use Win32::OLE;

my ($ServiceSet, $SupportsPause, $RetVal);  
eval {$ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='Schedule'"); };
unless($@)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  if ($ServiceInst->{AcceptPause})
  {
   $RetVal = $ServiceInst->PauseService();
   if ($RetVal == 0)
   {
    print "\nService paused\n";
   }
   else
   {
    if ($RetVal == 1)
    {
     print "\nPause not supported\n" ;
    }
    else 
    {
     print "\nAn error occurred:", $RetVal, "\n";
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
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="22075-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22075-181">Requirements</span></span>



| <span data-ttu-id="22075-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22075-182">Requirement</span></span> | <span data-ttu-id="22075-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="22075-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22075-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22075-184">Minimum supported client</span></span><br/> | <span data-ttu-id="22075-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22075-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22075-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22075-186">Minimum supported server</span></span><br/> | <span data-ttu-id="22075-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22075-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22075-188">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22075-188">Namespace</span></span><br/>                | <span data-ttu-id="22075-189">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="22075-189">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="22075-190">MOF</span><span class="sxs-lookup"><span data-stu-id="22075-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22075-191"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22075-191"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22075-192">DLL</span><span class="sxs-lookup"><span data-stu-id="22075-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22075-193"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22075-193"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22075-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22075-194">See also</span></span>

<dl> <dt>

<span data-ttu-id="22075-195">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="22075-195">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="22075-196">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="22075-196">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="22075-197">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="22075-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="22075-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="22075-198">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)
</dt> </dl>

 

