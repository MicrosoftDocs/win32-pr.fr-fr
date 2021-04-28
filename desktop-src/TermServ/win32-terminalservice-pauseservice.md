---
title: Méthode PauseService de la classe Win32_Service (Services Bureau à distance)
description: 'Méthode PauseService de la classe Win32_Service (Services Bureau à distance) : tente de placer le service dans l’état suspendu.'
ms.assetid: 101987F6-FBAB-4E79-B1FA-346B1EF58DE1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PauseService
- Services Bureau à distance de la méthode PauseService, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode PauseService
topic_type:
- apiref
api_name:
- Win32_Service.PauseService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c9847f363d9bc6d1743da6189d2c4290c00dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090597"
---
# <a name="pauseservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="a5c00-106">Méthode PauseService de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="a5c00-106">PauseService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="a5c00-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **PauseService** tente de placer le service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="a5c00-107">The **PauseService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the service in the paused state.</span></span>

<span data-ttu-id="a5c00-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="a5c00-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a5c00-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="a5c00-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5c00-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5c00-110">Syntax</span></span>


```mof
uint32 PauseService();
```



## <a name="parameters"></a><span data-ttu-id="a5c00-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5c00-111">Parameters</span></span>

<span data-ttu-id="a5c00-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5c00-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5c00-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a5c00-113">Return value</span></span>

<span data-ttu-id="a5c00-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a5c00-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="a5c00-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a5c00-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a5c00-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a5c00-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a5c00-117">**0**</span><span class="sxs-lookup"><span data-stu-id="a5c00-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-118">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="a5c00-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-119">**1**</span><span class="sxs-lookup"><span data-stu-id="a5c00-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-120">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a5c00-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-121">**2**</span><span class="sxs-lookup"><span data-stu-id="a5c00-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a5c00-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-123">**3**</span><span class="sxs-lookup"><span data-stu-id="a5c00-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-124">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="a5c00-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-125">**4**</span><span class="sxs-lookup"><span data-stu-id="a5c00-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-127">**5**</span><span class="sxs-lookup"><span data-stu-id="a5c00-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-128">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a5c00-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-129">**6**</span><span class="sxs-lookup"><span data-stu-id="a5c00-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-130">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="a5c00-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-131">**7**</span><span class="sxs-lookup"><span data-stu-id="a5c00-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-132">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="a5c00-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-133">**8**</span><span class="sxs-lookup"><span data-stu-id="a5c00-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-135">**9**</span><span class="sxs-lookup"><span data-stu-id="a5c00-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a5c00-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-137">**10**</span><span class="sxs-lookup"><span data-stu-id="a5c00-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="a5c00-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-139">**11**</span><span class="sxs-lookup"><span data-stu-id="a5c00-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="a5c00-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-141">**12**</span><span class="sxs-lookup"><span data-stu-id="a5c00-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-143">**13**</span><span class="sxs-lookup"><span data-stu-id="a5c00-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="a5c00-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-145">**14**</span><span class="sxs-lookup"><span data-stu-id="a5c00-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-147">**15**</span><span class="sxs-lookup"><span data-stu-id="a5c00-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-149">**16**</span><span class="sxs-lookup"><span data-stu-id="a5c00-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-151">**17**</span><span class="sxs-lookup"><span data-stu-id="a5c00-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a5c00-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-153">**19**</span><span class="sxs-lookup"><span data-stu-id="a5c00-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="a5c00-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-155">**19**</span><span class="sxs-lookup"><span data-stu-id="a5c00-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="a5c00-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-157">**20**</span><span class="sxs-lookup"><span data-stu-id="a5c00-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="a5c00-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-159">**21**</span><span class="sxs-lookup"><span data-stu-id="a5c00-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-160">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-161">**22**</span><span class="sxs-lookup"><span data-stu-id="a5c00-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-162">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-163">**23**</span><span class="sxs-lookup"><span data-stu-id="a5c00-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-164">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a5c00-165">**24**</span><span class="sxs-lookup"><span data-stu-id="a5c00-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a5c00-166">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="a5c00-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5c00-167">Notes </span><span class="sxs-lookup"><span data-stu-id="a5c00-167">Remarks</span></span>

<span data-ttu-id="a5c00-168">Une fois que vous avez déterminé quels services peuvent être arrêtés ou suspendus, vous pouvez utiliser les méthodes [**StopService**](win32-terminalservice-stopservice.md) et **PauseService** pour arrêter et suspendre les services.</span><span class="sxs-lookup"><span data-stu-id="a5c00-168">After you have determined which services can be stopped or paused, you can use the [**StopService**](win32-terminalservice-stopservice.md) and **PauseService** methods to stop and pause services.</span></span> <span data-ttu-id="a5c00-169">La décision d’arrêter un service plutôt que de le suspendre, ou vice versa, dépend de plusieurs facteurs, notamment les suivants :</span><span class="sxs-lookup"><span data-stu-id="a5c00-169">The decision to stop a service rather than pause it, or vice versa, depends on several factors, including the following:</span></span>

-   <span data-ttu-id="a5c00-170">Le service est-il susceptible d’être suspendu ?</span><span class="sxs-lookup"><span data-stu-id="a5c00-170">Is the service capable of being paused?</span></span> <span data-ttu-id="a5c00-171">Si ce n’est pas le cas, la seule option consiste à arrêter le service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-171">If not, your only option is the stop the service.</span></span>
-   <span data-ttu-id="a5c00-172">Avez-vous besoin de continuer à gérer les demandes des clients pour quiconque déjà connecté au service ?</span><span class="sxs-lookup"><span data-stu-id="a5c00-172">Do you need to continue handling client requests for anyone already connected to the service?</span></span> <span data-ttu-id="a5c00-173">Dans ce cas, la suspension d’un service lui permet généralement de gérer les clients existants tout en refusant l’accès aux nouveaux clients.</span><span class="sxs-lookup"><span data-stu-id="a5c00-173">If so, pausing a service typically allows it to handle existing clients while denying access to new clients.</span></span> <span data-ttu-id="a5c00-174">En revanche, lorsque vous arrêtez un service, tous les clients sont immédiatement déconnectés.</span><span class="sxs-lookup"><span data-stu-id="a5c00-174">By contrast, when you stop a service, all clients are immediately disconnected.</span></span>
-   <span data-ttu-id="a5c00-175">Avez-vous besoin de reconfigurer un service et de faire en sorte que les modifications prennent effet immédiatement ?</span><span class="sxs-lookup"><span data-stu-id="a5c00-175">Do you need to reconfigure a service and have the changes take effect immediately?</span></span> <span data-ttu-id="a5c00-176">Bien que les propriétés de service puissent être modifiées pendant l’interruption d’un service, la plupart d’entre elles ne prennent pas effet tant que le service n’est pas arrêté et redémarré.</span><span class="sxs-lookup"><span data-stu-id="a5c00-176">Although service properties can be changed while a service is paused, most of them do not take effect until the service is actually stopped and restarted.</span></span>

<span data-ttu-id="a5c00-177">Le code de script requis pour arrêter un service est presque identique au code requis pour suspendre le service.</span><span class="sxs-lookup"><span data-stu-id="a5c00-177">The scripting code required to stop a service is almost identical to the code required to pause the service.</span></span>

## <a name="examples"></a><span data-ttu-id="a5c00-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="a5c00-178">Examples</span></span>

<span data-ttu-id="a5c00-179">L’exemple de [suspension de services s’exécutant sous un compte spécifique](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) met en pause tous les services qui s’exécutent sous le compte de service hypothétique netsvc.</span><span class="sxs-lookup"><span data-stu-id="a5c00-179">The [Pause Services Running Under a Specific Account](https://Gallery.TechNet.Microsoft.Com/12a256dd-39da-4690-b3f0-f0adccaf25f1) VBScript sample Pauses all services running under the hypothetical service account Netsvc.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5c00-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5c00-180">Requirements</span></span>



| <span data-ttu-id="a5c00-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5c00-181">Requirement</span></span> | <span data-ttu-id="a5c00-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5c00-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a5c00-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5c00-183">Minimum supported client</span></span><br/> | <span data-ttu-id="a5c00-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5c00-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a5c00-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5c00-185">Minimum supported server</span></span><br/> | <span data-ttu-id="a5c00-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5c00-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a5c00-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5c00-187">Namespace</span></span><br/>                | <span data-ttu-id="a5c00-188">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a5c00-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a5c00-189">MOF</span><span class="sxs-lookup"><span data-stu-id="a5c00-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5c00-190"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5c00-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5c00-191">DLL</span><span class="sxs-lookup"><span data-stu-id="a5c00-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5c00-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5c00-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5c00-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5c00-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5c00-194">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="a5c00-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="a5c00-195">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="a5c00-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="a5c00-196">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="a5c00-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="a5c00-197">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="a5c00-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> <dt>

[<span data-ttu-id="a5c00-198">**StopService**</span><span class="sxs-lookup"><span data-stu-id="a5c00-198">**StopService**</span></span>](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)
</dt> </dl>

 

