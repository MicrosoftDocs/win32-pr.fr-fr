---
title: Méthode StopService de la classe Win32_Service (Sdoias. h) (service Terminal Server)
description: Place le service, représenté par l' \_ objet Win32 TerminalService, à l’état arrêté.
ms.assetid: 228711DC-369B-48B6-96EE-DF4026904E26
ms.tgt_platform: multiple
keywords:
- Méthode StopService Services Bureau à distance
- Méthode StopService Services Bureau à distance, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode StopService
topic_type:
- apiref
api_name:
- Win32_Service.StopService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e1b21db330bb9111b96fb244200845cb83b3153
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106535429"
---
# <a name="stopservice-method-of-the-win32_service-class-sdoiash-for-the-terminal-service"></a><span data-ttu-id="1899f-106">Méthode StopService de la classe Win32_Service (Sdoias. h) pour le service Terminal Server</span><span class="sxs-lookup"><span data-stu-id="1899f-106">StopService method of the Win32_Service class (Sdoias.h) for the Terminal service</span></span>

<span data-ttu-id="1899f-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** place le service, représenté par l’objet [**Win32 \_ TerminalService**](win32-terminalservice.md) , à l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="1899f-107">The **StopService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method places the service, represented by the [**Win32\_TerminalService**](win32-terminalservice.md) object, in the stopped state.</span></span>

<span data-ttu-id="1899f-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1899f-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1899f-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1899f-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1899f-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1899f-110">Syntax</span></span>


```mof
uint32 StopService();
```



## <a name="parameters"></a><span data-ttu-id="1899f-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1899f-111">Parameters</span></span>

<span data-ttu-id="1899f-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1899f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1899f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1899f-113">Return value</span></span>

<span data-ttu-id="1899f-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1899f-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="1899f-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1899f-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="1899f-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="1899f-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="1899f-117">**0**</span><span class="sxs-lookup"><span data-stu-id="1899f-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-118">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="1899f-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-119">**1**</span><span class="sxs-lookup"><span data-stu-id="1899f-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-120">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1899f-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-121">**2**</span><span class="sxs-lookup"><span data-stu-id="1899f-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1899f-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-123">**3**</span><span class="sxs-lookup"><span data-stu-id="1899f-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-124">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="1899f-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-125">**4**</span><span class="sxs-lookup"><span data-stu-id="1899f-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="1899f-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-127">**5**</span><span class="sxs-lookup"><span data-stu-id="1899f-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-128">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="1899f-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-129">**6**</span><span class="sxs-lookup"><span data-stu-id="1899f-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-130">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="1899f-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-131">**7**</span><span class="sxs-lookup"><span data-stu-id="1899f-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-132">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="1899f-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-133">**8**</span><span class="sxs-lookup"><span data-stu-id="1899f-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="1899f-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-135">**9**</span><span class="sxs-lookup"><span data-stu-id="1899f-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="1899f-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-137">**10**</span><span class="sxs-lookup"><span data-stu-id="1899f-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="1899f-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-139">**11**</span><span class="sxs-lookup"><span data-stu-id="1899f-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="1899f-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-141">**12**</span><span class="sxs-lookup"><span data-stu-id="1899f-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="1899f-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-143">**13**</span><span class="sxs-lookup"><span data-stu-id="1899f-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="1899f-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-145">**14**</span><span class="sxs-lookup"><span data-stu-id="1899f-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="1899f-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-147">**15**</span><span class="sxs-lookup"><span data-stu-id="1899f-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="1899f-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-149">**16**</span><span class="sxs-lookup"><span data-stu-id="1899f-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="1899f-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-151">**17**</span><span class="sxs-lookup"><span data-stu-id="1899f-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1899f-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-153">**19**</span><span class="sxs-lookup"><span data-stu-id="1899f-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="1899f-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-155">**19**</span><span class="sxs-lookup"><span data-stu-id="1899f-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="1899f-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-157">**20**</span><span class="sxs-lookup"><span data-stu-id="1899f-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="1899f-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-159">**21**</span><span class="sxs-lookup"><span data-stu-id="1899f-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-160">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="1899f-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-161">**22**</span><span class="sxs-lookup"><span data-stu-id="1899f-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-162">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="1899f-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-163">**23**</span><span class="sxs-lookup"><span data-stu-id="1899f-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-164">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="1899f-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1899f-165">**24**</span><span class="sxs-lookup"><span data-stu-id="1899f-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="1899f-166">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="1899f-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1899f-167">Notes</span><span class="sxs-lookup"><span data-stu-id="1899f-167">Remarks</span></span>

<span data-ttu-id="1899f-168">Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes **StopService** et [**PauseService**](win32-terminalservice-pauseservice.md) pour arrêter et suspendre les services.</span><span class="sxs-lookup"><span data-stu-id="1899f-168">After you have determined which services can be stopped or paused, you can use the **StopService** and [**PauseService**](win32-terminalservice-pauseservice.md) methods to stop and pause services.</span></span> <span data-ttu-id="1899f-169">La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="1899f-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="1899f-170">Le service est-il susceptible d’être suspendu ?</span><span class="sxs-lookup"><span data-stu-id="1899f-170">Is the service capable of being paused?</span></span> <span data-ttu-id="1899f-171">Si ce n’est pas le cas, la seule option consiste à arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="1899f-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="1899f-172">Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ?</span><span class="sxs-lookup"><span data-stu-id="1899f-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="1899f-173">Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients.</span><span class="sxs-lookup"><span data-stu-id="1899f-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="1899f-174">En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.</span><span class="sxs-lookup"><span data-stu-id="1899f-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="1899f-175">Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="1899f-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="1899f-176">Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="1899f-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="1899f-177">Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.</span><span class="sxs-lookup"><span data-stu-id="1899f-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

<span data-ttu-id="1899f-178">Si vous tentez d’arrêter un service qui a des services dépendants en cours d’exécution, la méthode **StopService** échoue avec une valeur de retour de 3.</span><span class="sxs-lookup"><span data-stu-id="1899f-178">If you attempt to stop a service which has dependent services running, the **StopService** method fails with a return value of 3.</span></span> <span data-ttu-id="1899f-179">Les services dépendants doivent d’abord être arrêtés.</span><span class="sxs-lookup"><span data-stu-id="1899f-179">The dependent services must be stopped first.</span></span>

<span data-ttu-id="1899f-180">Si vous arrêtez un service, vérifiez immédiatement le [**\_ TerminalService Win32**](win32-terminalservice.md).**Propriété State** , car la valeur peut toujours afficher le service comme étant en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="1899f-180">If you stop a service, then immediately check the [**Win32\_TerminalService**](win32-terminalservice.md).**State** property, as the value may still show the service as running.</span></span>

## <a name="examples"></a><span data-ttu-id="1899f-181">Exemples</span><span class="sxs-lookup"><span data-stu-id="1899f-181">Examples</span></span>

<span data-ttu-id="1899f-182">[L’ensemble de RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) L’exemple PowerShell définit l’état du service pour les ordinateurs distants.</span><span class="sxs-lookup"><span data-stu-id="1899f-182">[The Set-RemoteService](https://Gallery.TechNet.Microsoft.Com/79595ce9-bfc3-463e-9e84-d9e0b78590c1) PowerShell sample Sets service state for remote machines.</span></span>

<span data-ttu-id="1899f-183">L’exemple [d’arrêt d’un service et de ses dépendants](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript arrête un service et tous les services dépendants.</span><span class="sxs-lookup"><span data-stu-id="1899f-183">The [Stop a Service and Its Dependents](https://Gallery.TechNet.Microsoft.Com/ae07e623-2cbd-4983-b991-aa4d1e6e2732) VBScript sample stops a service and all dependent services.</span></span>

## <a name="requirements"></a><span data-ttu-id="1899f-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1899f-184">Requirements</span></span>



| <span data-ttu-id="1899f-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1899f-185">Requirement</span></span> | <span data-ttu-id="1899f-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="1899f-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1899f-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1899f-187">Minimum supported client</span></span><br/> | <span data-ttu-id="1899f-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1899f-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1899f-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1899f-189">Minimum supported server</span></span><br/> | <span data-ttu-id="1899f-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1899f-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1899f-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1899f-191">Namespace</span></span><br/>                | <span data-ttu-id="1899f-192">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="1899f-192">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1899f-193">En-tête</span><span class="sxs-lookup"><span data-stu-id="1899f-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="1899f-194"><dt>Sdoias. h</dt></span><span class="sxs-lookup"><span data-stu-id="1899f-194"><dt>Sdoias.h</dt></span></span> </dl>     |
| <span data-ttu-id="1899f-195">MOF</span><span class="sxs-lookup"><span data-stu-id="1899f-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1899f-196"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1899f-196"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1899f-197">DLL</span><span class="sxs-lookup"><span data-stu-id="1899f-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1899f-198"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1899f-198"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1899f-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1899f-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1899f-200">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="1899f-200">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="1899f-201">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="1899f-201">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="1899f-202">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="1899f-202">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="1899f-203">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="1899f-203">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="1899f-204">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="1899f-204">**PauseService**</span></span>](/windows/desktop/CIMWin32Prov/pauseservice-method-in-class-win32-systemdriver)
</dt> </dl>

 

