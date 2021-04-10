---
description: Tente de placer le service référencé dans son état de démarrage.
ms.assetid: b7a815a2-7bf6-436f-b3b4-de55eeb2de0e
ms.tgt_platform: multiple
title: Méthode StartService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb530766781de4e23cc86778c1597a5c5c2a1014
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950630"
---
# <a name="startservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="7103e-103">Méthode StartService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7103e-103">StartService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7103e-104">La méthode **StartService** tente de placer le service référencé dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="7103e-104">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="7103e-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7103e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7103e-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7103e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7103e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7103e-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="7103e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7103e-108">Parameters</span></span>

<span data-ttu-id="7103e-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="7103e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7103e-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7103e-110">Return value</span></span>

<span data-ttu-id="7103e-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7103e-111">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="7103e-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7103e-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7103e-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7103e-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7103e-114">**0**</span><span class="sxs-lookup"><span data-stu-id="7103e-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="7103e-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-116">**1**</span><span class="sxs-lookup"><span data-stu-id="7103e-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7103e-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-118">**2**</span><span class="sxs-lookup"><span data-stu-id="7103e-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7103e-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-120">**3**</span><span class="sxs-lookup"><span data-stu-id="7103e-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="7103e-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-122">**4**</span><span class="sxs-lookup"><span data-stu-id="7103e-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="7103e-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-124">**5**</span><span class="sxs-lookup"><span data-stu-id="7103e-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="7103e-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-126">**6**</span><span class="sxs-lookup"><span data-stu-id="7103e-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="7103e-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-128">**7**</span><span class="sxs-lookup"><span data-stu-id="7103e-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="7103e-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-130">**8**</span><span class="sxs-lookup"><span data-stu-id="7103e-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="7103e-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-132">**9**</span><span class="sxs-lookup"><span data-stu-id="7103e-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7103e-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-134">**10**</span><span class="sxs-lookup"><span data-stu-id="7103e-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7103e-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-136">**11**</span><span class="sxs-lookup"><span data-stu-id="7103e-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="7103e-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-138">**12**</span><span class="sxs-lookup"><span data-stu-id="7103e-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="7103e-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-140">**13**</span><span class="sxs-lookup"><span data-stu-id="7103e-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="7103e-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-142">**14**</span><span class="sxs-lookup"><span data-stu-id="7103e-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="7103e-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-144">**15**</span><span class="sxs-lookup"><span data-stu-id="7103e-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="7103e-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-146">**16**</span><span class="sxs-lookup"><span data-stu-id="7103e-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="7103e-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-148">**17**</span><span class="sxs-lookup"><span data-stu-id="7103e-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7103e-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-150">**19**</span><span class="sxs-lookup"><span data-stu-id="7103e-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="7103e-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-152">**19**</span><span class="sxs-lookup"><span data-stu-id="7103e-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="7103e-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-154">**20**</span><span class="sxs-lookup"><span data-stu-id="7103e-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7103e-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-156">**21**</span><span class="sxs-lookup"><span data-stu-id="7103e-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="7103e-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-158">**22**</span><span class="sxs-lookup"><span data-stu-id="7103e-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="7103e-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-160">**23**</span><span class="sxs-lookup"><span data-stu-id="7103e-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="7103e-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7103e-162">**24**</span><span class="sxs-lookup"><span data-stu-id="7103e-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="7103e-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="7103e-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7103e-164">Notes</span><span class="sxs-lookup"><span data-stu-id="7103e-164">Remarks</span></span>

<span data-ttu-id="7103e-165">Bien qu’il puisse sembler qu’il n’y ait aucune différence pratique entre un service arrêté et un service suspendu, les deux États apparaissent différemment pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="7103e-165">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="7103e-166">Un service arrêté est un service qui n’est pas en cours d’exécution et doit suivre l’intégralité de la procédure de démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="7103e-166">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="7103e-167">Toutefois, un service suspendu est toujours en cours d’exécution, mais son fonctionnement est suspendu.</span><span class="sxs-lookup"><span data-stu-id="7103e-167">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="7103e-168">Pour cette raison, un service suspendu n’a pas besoin de traverser l’intégralité de la procédure de démarrage du service, mais il a besoin d’une procédure différente pour reprendre son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="7103e-168">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="7103e-169">Vous devez utiliser la méthode appropriée pour démarrer un service qui a été arrêté ou pour reprendre un service qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="7103e-169">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="7103e-170">Les méthodes de [**\_ service Win32**](win32-service.md) **StartService** et [**ResumeService**](resumeservice-method-in-class-win32-service.md) doivent être utilisées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="7103e-170">The [**Win32\_Service**](win32-service.md) methods **StartService** and [**ResumeService**](resumeservice-method-in-class-win32-service.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="7103e-171">Si un service est actuellement arrêté, vous devez utiliser la méthode **StartService** pour le redémarrer ; [**ResumeService**](resumeservice-method-in-class-win32-service.md) ne peut pas démarrer un service qui est actuellement arrêté.</span><span class="sxs-lookup"><span data-stu-id="7103e-171">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](resumeservice-method-in-class-win32-service.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="7103e-172">Si un service est suspendu, vous devez utiliser [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7103e-172">If a service is paused, you must use [**ResumeService**](resumeservice-method-in-class-win32-service.md).</span></span> <span data-ttu-id="7103e-173">Si vous utilisez la méthode **StartService** sur un service suspendu, vous recevez le message « le service est déjà en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="7103e-173">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="7103e-174">Toutefois, le service reste en pause jusqu’à ce que le code de contrôle de reprise du service lui soit envoyé.</span><span class="sxs-lookup"><span data-stu-id="7103e-174">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="7103e-175">Si vous démarrez un service arrêté qui dépend d’un autre service, les deux services sont démarrés.</span><span class="sxs-lookup"><span data-stu-id="7103e-175">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="7103e-176">Lorsqu’un service est démarré avec cette méthode, tous les services dépendants ne sont pas démarrés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7103e-176">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="7103e-177">Vous devez utiliser la classe d’association [**Win32 \_ DependentService**](win32-dependentservice.md) et les [associateurs de](/windows/desktop/WmiSdk/associators-of-statement) la requête pour localiser les dépendants et les démarrer séparément.</span><span class="sxs-lookup"><span data-stu-id="7103e-177">You must use the association class [**Win32\_DependentService**](win32-dependentservice.md) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="examples"></a><span data-ttu-id="7103e-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="7103e-178">Examples</span></span>

<span data-ttu-id="7103e-179">L’exemple d' [activation à distance](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) de PowerShell RDP active à distance le service bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="7103e-179">The [Remotely Enable RDP](https://Gallery.TechNet.Microsoft.Com/Remotely-Enable-RDP-855c3842) PowerShell sample remotely enables the Remote Desktop service.</span></span>

<span data-ttu-id="7103e-180">L’exemple PowerShell [Stop, Start, Enable ou Disable service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) démarre, arrête, active ou désactive un service.</span><span class="sxs-lookup"><span data-stu-id="7103e-180">The [Stop, Start, Enable or Disable Service](https://Gallery.TechNet.Microsoft.Com/212e68f0-5279-4499-8e9e-6aa1807719c0) PowerShell sample starts, stops, enables, or disables a service.</span></span>

<span data-ttu-id="7103e-181">L’exemple de code VBSScript suivant montre comment démarrer un service spécifique à partir d’instances du [**\_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7103e-181">The following VBSScript code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```VB
Set ServiceSet = GetObject("winmgmts:").ExecQuery("select * from Win32_Service where Name='ClipSrv'")

for each Service in ServiceSet
 RetVal = Service.StartService()
 if RetVal = 0 then WScript.Echo "Service started"
 if RetVal = 10 then WScript.Echo "Service already running"
next
```



<span data-ttu-id="7103e-182">L’exemple de code perl suivant montre comment démarrer un service spécifique à partir d’instances du [**\_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="7103e-182">The following Perl code sample demonstrates how to start a specific service from instances of [**Win32\_Service**](win32-service.md).</span></span>


```
use strict;
use Win32::OLE;

my $ServiceSet;

eval { $ServiceSet = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE Name='ClipSrv'"); };

if(!$@ && defined $ServiceSet)
{
 foreach my $service (in $ServiceSet)
 {
  my $Result = $service->StartService();
  if ($Result == 0) 
  {
   print "\nService started\n";
  }
  elsif ($Result == 10)
  {
   print "\nService already running\n";
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="7103e-183">L’exemple de code VBScript suivant, NetDDE, dépend du service NetDDEDSDM.</span><span class="sxs-lookup"><span data-stu-id="7103e-183">The following VBScript code example, NetDDE, is dependent on the NetDDEDSDM service.</span></span> <span data-ttu-id="7103e-184">Le script localise la classe dont dépend NetDDE et le démarre, ce qui ne démarre pas automatiquement NetDDE.</span><span class="sxs-lookup"><span data-stu-id="7103e-184">The script locates the class on which NetDDE depends and starts it, which does not automatically start NetDDE.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Stop NetDDE if it is running
Set objNetDDEService = objWMIService.Get("Win32_Service.Name='NetDDE'")
Return = objNetDDEService.StopService()

' NetDDE is in the dependent role to another service
Set colServiceList = objWMIService.ExecQuery("Associators of " _
    & "{Win32_Service.Name='NetDDE'} Where " & "AssocClass=Win32_DependentService " & "Role=Dependent" )

' start the service on which NetDDE is dependent
For Each objService in colServiceList
    WScript.Echo "Starting " & objService.Name
    Return = objService.StartService()
    If Return = 0 Then
        WScript.Echo "Parent service " & objService.Name & " started successfully"
    Else
        WScript.Echo "Parent service " & objService.Name & " did not start. Return = " & Return
    End If
Next

' NetDDE is still stopped
Set objNetDDEService = _
    objWMIService.Get("Win32_Service.Name='NetDDE'")
WScript.Echo "Dependent NetDDE service is " & objNetDDEService.State
```



## <a name="requirements"></a><span data-ttu-id="7103e-185">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7103e-185">Requirements</span></span>



| <span data-ttu-id="7103e-186">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7103e-186">Requirement</span></span> | <span data-ttu-id="7103e-187">Valeur</span><span class="sxs-lookup"><span data-stu-id="7103e-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7103e-188">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7103e-188">Minimum supported client</span></span><br/> | <span data-ttu-id="7103e-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7103e-189">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7103e-190">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7103e-190">Minimum supported server</span></span><br/> | <span data-ttu-id="7103e-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7103e-191">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7103e-192">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7103e-192">Namespace</span></span><br/>                | <span data-ttu-id="7103e-193">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7103e-193">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7103e-194">MOF</span><span class="sxs-lookup"><span data-stu-id="7103e-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7103e-195"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7103e-195"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7103e-196">DLL</span><span class="sxs-lookup"><span data-stu-id="7103e-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7103e-197"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7103e-197"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7103e-198">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7103e-198">See also</span></span>

<dl> <dt>

<span data-ttu-id="7103e-199">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7103e-199">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7103e-200">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="7103e-200">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="7103e-201">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="7103e-201">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

