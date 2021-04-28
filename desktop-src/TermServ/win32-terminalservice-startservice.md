---
title: Méthode StartService de la classe Win32_Service (Services Bureau à distance)
description: 'Méthode StartService de la classe Win32_Service (Services Bureau à distance) : tente de placer le service référencé dans son état de démarrage.'
ms.assetid: 4DA05C48-03A0-4D4B-9E69-0404393C219C
ms.tgt_platform: multiple
keywords:
- StartService, méthode Services Bureau à distance
- StartService, méthode Services Bureau à distance, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode StartService
topic_type:
- apiref
api_name:
- Win32_Service.StartService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce4bd12150223d7cdc1340b7557ba309a1e07da4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084197"
---
# <a name="startservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="8fc5b-106">Méthode StartService de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="8fc5b-106">StartService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="8fc5b-107">La méthode **StartService** tente de placer le service référencé dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-107">The **StartService** method attempts to place the referenced service into its startup state.</span></span>

<span data-ttu-id="8fc5b-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8fc5b-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc5b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fc5b-110">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="8fc5b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fc5b-111">Parameters</span></span>

<span data-ttu-id="8fc5b-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fc5b-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8fc5b-113">Return value</span></span>

<span data-ttu-id="8fc5b-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="8fc5b-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8fc5b-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8fc5b-117">**0**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-118">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-119">**1**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-120">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-121">**2**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-123">**3**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-124">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-125">**4**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-127">**5**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-128">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-129">**6**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-130">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-131">**7**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-132">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-133">**8**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-135">**9**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-137">**10**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-139">**11**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-141">**12**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-143">**13**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-145">**14**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-147">**15**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-149">**16**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-151">**17**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-153">**19**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-155">**19**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-157">**20**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-159">**21**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-160">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-161">**22**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-162">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-163">**23**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-164">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8fc5b-165">**24**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8fc5b-166">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fc5b-167">Notes </span><span class="sxs-lookup"><span data-stu-id="8fc5b-167">Remarks</span></span>

<span data-ttu-id="8fc5b-168">Bien qu’il puisse sembler qu’il n’y ait aucune différence pratique entre un service arrêté et un service suspendu, les deux États apparaissent différemment pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="8fc5b-169">Un service arrêté est un service qui n’est pas en cours d’exécution et doit suivre l’intégralité de la procédure de démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="8fc5b-170">Toutefois, un service suspendu est toujours en cours d’exécution, mais son fonctionnement est suspendu.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="8fc5b-171">Pour cette raison, un service suspendu n’a pas besoin de traverser l’intégralité de la procédure de démarrage du service, mais il a besoin d’une procédure différente pour reprendre son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="8fc5b-172">Vous devez utiliser la méthode appropriée pour démarrer un service qui a été arrêté ou pour reprendre un service qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="8fc5b-173">Les méthodes de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) **StartService** et [**ResumeService**](win32-terminalservice-resumeservice.md) doivent être utilisées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="8fc5b-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods **StartService** and [**ResumeService**](win32-terminalservice-resumeservice.md) should be used in the following situations:</span></span>

-   <span data-ttu-id="8fc5b-174">Si un service est actuellement arrêté, vous devez utiliser la méthode **StartService** pour le redémarrer ; [**ResumeService**](win32-terminalservice-resumeservice.md) ne peut pas démarrer un service qui est actuellement arrêté.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-174">If a service is currently stopped, you must use the **StartService** method to restart it; [**ResumeService**](win32-terminalservice-resumeservice.md) cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="8fc5b-175">Si un service est suspendu, vous devez utiliser [**ResumeService**](win32-terminalservice-resumeservice.md).</span><span class="sxs-lookup"><span data-stu-id="8fc5b-175">If a service is paused, you must use [**ResumeService**](win32-terminalservice-resumeservice.md).</span></span> <span data-ttu-id="8fc5b-176">Si vous utilisez la méthode **StartService** sur un service suspendu, vous recevez le message « le service est déjà en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="8fc5b-176">If you use the **StartService** method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="8fc5b-177">Toutefois, le service reste en pause jusqu’à ce que le code de contrôle de reprise du service lui soit envoyé.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

<span data-ttu-id="8fc5b-178">Si vous démarrez un service arrêté qui dépend d’un autre service, les deux services sont démarrés.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-178">If you start a stopped service that depends on another service, then both services are started.</span></span> <span data-ttu-id="8fc5b-179">Lorsqu’un service est démarré avec cette méthode, tous les services dépendants ne sont pas démarrés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-179">When a service is started with this method, any dependent services are not automatically started.</span></span> <span data-ttu-id="8fc5b-180">Vous devez utiliser la classe d’association [**Win32 \_ DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) et les [associateurs de](/windows/desktop/WmiSdk/associators-of-statement) la requête pour localiser les dépendants et les démarrer séparément.</span><span class="sxs-lookup"><span data-stu-id="8fc5b-180">You must use the association class [**Win32\_DependentService**](/windows/desktop/CIMWin32Prov/win32-dependentservice) and the [Associators Of](/windows/desktop/WmiSdk/associators-of-statement) query to locate the dependents and start them separately.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc5b-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fc5b-181">Requirements</span></span>



| <span data-ttu-id="8fc5b-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fc5b-182">Requirement</span></span> | <span data-ttu-id="8fc5b-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fc5b-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc5b-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc5b-184">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc5b-185">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8fc5b-185">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8fc5b-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fc5b-186">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc5b-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8fc5b-187">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8fc5b-188">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8fc5b-188">Namespace</span></span><br/>                | <span data-ttu-id="8fc5b-189">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="8fc5b-189">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="8fc5b-190">MOF</span><span class="sxs-lookup"><span data-stu-id="8fc5b-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fc5b-191"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fc5b-191"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fc5b-192">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc5b-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc5b-193"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc5b-193"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc5b-194">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fc5b-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc5b-195">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-195">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="8fc5b-196">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="8fc5b-196">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="8fc5b-197">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc5b-197">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="8fc5b-198">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="8fc5b-198">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

