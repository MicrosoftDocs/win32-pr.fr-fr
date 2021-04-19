---
description: Place le service, représenté par l' \_ objet de service Win32, à l’état arrêté.
ms.assetid: cc2c71f7-12e6-4ba4-bfb4-f23845d798b5
ms.tgt_platform: multiple
title: Méthode StopService de la classe Win32_Service (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90d979754a3d6f034c353229dbaa1b1dbaedea79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514113"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash"></a><span data-ttu-id="ad6b2-103">Méthode StopService de la classe Win32_Service (Sdoias. h)</span><span class="sxs-lookup"><span data-stu-id="ad6b2-103">StopService method of the Win32_Service class (Sdoias.h)</span></span>

<span data-ttu-id="ad6b2-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** place le service, représenté par l’objet de [**\_ service Win32**](win32-service.md) , à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-104">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_Service**](win32-service.md) object, in the stopped state.</span></span>

<span data-ttu-id="ad6b2-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="ad6b2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ad6b2-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ad6b2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6b2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad6b2-107">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="ad6b2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad6b2-108">Parameters</span></span>

<span data-ttu-id="ad6b2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad6b2-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad6b2-110">Return value</span></span>

<span data-ttu-id="ad6b2-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="ad6b2-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="ad6b2-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ad6b2-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="ad6b2-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ad6b2-114">**0**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-116">**1**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-118">**2**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-120">**3**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-122">**4**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-124">**5**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-126">**6**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-128">**7**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-130">**8**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-132">**9**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-134">**10**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-136">**11**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-138">**12**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-140">**13**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-142">**14**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-144">**15**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-146">**16**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-148">**17**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-150">**19**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-152">**19**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-154">**20**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-156">**21**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-158">**22**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-160">**23**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="ad6b2-162">**24**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="ad6b2-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad6b2-164">Notes</span><span class="sxs-lookup"><span data-stu-id="ad6b2-164">Remarks</span></span>

<span data-ttu-id="ad6b2-165">Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes **StopService** et [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) pour arrêter et suspendre les services.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-165">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md) methods to stop and pause services.</span></span> <span data-ttu-id="ad6b2-166">La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="ad6b2-166">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="ad6b2-167">Le service est-il susceptible d’être suspendu ?</span><span class="sxs-lookup"><span data-stu-id="ad6b2-167">Is the service capable of being paused?</span></span> <span data-ttu-id="ad6b2-168">Si ce n’est pas le cas, la seule option consiste à arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-168">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="ad6b2-169">Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ?</span><span class="sxs-lookup"><span data-stu-id="ad6b2-169">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="ad6b2-170">Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-170">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="ad6b2-171">En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-171">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="ad6b2-172">Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="ad6b2-172">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="ad6b2-173">Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-173">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="ad6b2-174">Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-174">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="ad6b2-175">Si vous tentez d’arrêter un service qui a des services dépendants en cours d’exécution, la méthode **StopService** échoue avec une valeur de retour de 3.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-175">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="ad6b2-176">Les services dépendants doivent d’abord être arrêtés.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-176">The dependent services must be stopped first.</span></span>

<span data-ttu-id="ad6b2-177">Si vous arrêtez un service, vérifiez immédiatement le [**\_ service Win32**](win32-service.md).**Propriété State** , car la valeur peut toujours afficher le service comme étant en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-177">If you stop a service, then immediately check the [**Win32\_Service**](win32-service.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="ad6b2-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="ad6b2-178">Examples</span></span>

<span data-ttu-id="ad6b2-179">[L’ensemble de RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) L’exemple PowerShell définit l’état du service pour les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-179">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="ad6b2-180">L’exemple [d’arrêt d’un service et de ses dépendants](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript arrête un service et tous les services dépendants.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-180">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

<span data-ttu-id="ad6b2-181">L’exemple de code VBScript suivant montre comment arrêter un service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-181">The following VBScript code sample demonstrates how to shut down a service.</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StopService()
 if RetVal = 0 then 
  WScript.Echo "Service stopped" 
 elseif RetVal = 5 then 
  WScript.Echo "Service already stopped" 
 end if
next
```



<span data-ttu-id="ad6b2-182">L’exemple de code perl suivant montre comment arrêter un service.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-182">The following Perl code sample demonstrates how to shut down a service.</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if (!$@ && defined $ServiceSet)
{
 foreach my $ServiceInst (in $ServiceSet)
 {
  my $Result = $ServiceInst->StopService();
  if ($Result == 0)
  {
   print "\nService stopped\n";
  }
  elsif ($Result == 5) 
  {
   print "\nService already stopped\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="ad6b2-183">L’exemple de code VBScript suivant montre que vous ne pouvez pas arrêter le service NetDDE tant que les services dépendants n’ont pas été arrêtés.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-183">The following VBScript code example shows that you cannot stop the NetDDE service until the dependent services have been stopped.</span></span> <span data-ttu-id="ad6b2-184">Pour exécuter le script, assurez-vous que le service NetDDE et ses services dépendants sont en cours d’exécution en utilisant le composant logiciel enfichable MMC Services. msc ou la commande **net start** .</span><span class="sxs-lookup"><span data-stu-id="ad6b2-184">To run the script, ensure that the NetDDE service and its dependent services are running by using the Services.msc MMC snap-in or the **Net Start** command.</span></span>

<span data-ttu-id="ad6b2-185">La [**classe \_ DependentService Win32**](win32-dependentservice.md) vous permet de localiser des dépendances de service via un [associateur de](/windows/desktop/WmiSdk/associators-of-statement) requête.</span><span class="sxs-lookup"><span data-stu-id="ad6b2-185">The [**Win32\_DependentService**](win32-dependentservice.md) class allows you to locate service dependencies through an [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & _
    strComputer & "\root\cimv2")

Set objNetDDEservice = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")

WScript.Echo "NetDDE service state: " & objNetDDEService.State
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return  & _
    "  Service cannot be stopped because " & _
    "dependent services are running"

Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " _
        & "AssocClass=Win32_DependentService " & _
    "Role=Antecedent" )

For Each objService in colServiceList
   WScript.Echo "Dependent service: " & objService.Name & _
   "   State: " & objService.State
   WScript.Echo "Stopping dependent service " & objService.Name
   objService.StopService()    
Next

Wscript.Sleep 20000
WScript.Echo "Stopping NetDDE service"
Return = objNetDDEService.StopService()
WScript.Echo "Return value: " & Return
```



## <a name="requirements"></a><span data-ttu-id="ad6b2-186">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad6b2-186">Requirements</span></span>



| <span data-ttu-id="ad6b2-187">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad6b2-187">Requirement</span></span> | <span data-ttu-id="ad6b2-188">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad6b2-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6b2-189">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad6b2-189">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6b2-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad6b2-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad6b2-191">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad6b2-191">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6b2-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad6b2-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad6b2-193">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad6b2-193">Namespace</span></span><br/>                | <span data-ttu-id="ad6b2-194">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="ad6b2-194">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad6b2-195">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad6b2-195">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad6b2-196"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad6b2-196"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="ad6b2-197">MOF</span><span class="sxs-lookup"><span data-stu-id="ad6b2-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad6b2-198"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad6b2-198"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad6b2-199">DLL</span><span class="sxs-lookup"><span data-stu-id="ad6b2-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad6b2-200"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad6b2-200"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6b2-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad6b2-201">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad6b2-202">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ad6b2-202">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ad6b2-203">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-203">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="ad6b2-204">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="ad6b2-204">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="ad6b2-205">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="ad6b2-205">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)
</dt> </dl>

 

