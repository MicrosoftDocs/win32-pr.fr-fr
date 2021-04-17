---
title: Méthode ResumeService de la classe Win32_Service (Services Bureau à distance)
description: Tente de placer le service référencé dans l’État repris.
ms.assetid: AA020A0A-E69C-44AB-B259-A73460728770
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ResumeService
- Services Bureau à distance de la méthode ResumeService, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode ResumeService
topic_type:
- apiref
api_name:
- Win32_Service.ResumeService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7b446dea84e4320e9aa8972a88dc4fdd5a6eea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509270"
---
# <a name="resumeservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="09ff3-106">Méthode ResumeService de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="09ff3-106">ResumeService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="09ff3-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ResumeService** tente de placer le service référencé dans l’État repris.</span><span class="sxs-lookup"><span data-stu-id="09ff3-107">The **ResumeService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to place the referenced service in the resumed state.</span></span>

<span data-ttu-id="09ff3-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="09ff3-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="09ff3-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="09ff3-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="09ff3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09ff3-110">Syntax</span></span>


```mof
uint32 ResumeService();
```



## <a name="parameters"></a><span data-ttu-id="09ff3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09ff3-111">Parameters</span></span>

<span data-ttu-id="09ff3-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="09ff3-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="09ff3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09ff3-113">Return value</span></span>

<span data-ttu-id="09ff3-114">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="09ff3-114">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="09ff3-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="09ff3-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="09ff3-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="09ff3-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="09ff3-117">**0**</span><span class="sxs-lookup"><span data-stu-id="09ff3-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-118">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="09ff3-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-119">**1**</span><span class="sxs-lookup"><span data-stu-id="09ff3-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-120">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="09ff3-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-121">**2**</span><span class="sxs-lookup"><span data-stu-id="09ff3-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="09ff3-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-123">**3**</span><span class="sxs-lookup"><span data-stu-id="09ff3-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-124">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="09ff3-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-125">**4**</span><span class="sxs-lookup"><span data-stu-id="09ff3-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="09ff3-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-127">**5**</span><span class="sxs-lookup"><span data-stu-id="09ff3-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-128">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="09ff3-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-129">**6**</span><span class="sxs-lookup"><span data-stu-id="09ff3-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-130">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="09ff3-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-131">**7**</span><span class="sxs-lookup"><span data-stu-id="09ff3-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-132">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="09ff3-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-133">**8**</span><span class="sxs-lookup"><span data-stu-id="09ff3-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="09ff3-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-135">**9**</span><span class="sxs-lookup"><span data-stu-id="09ff3-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="09ff3-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-137">**10**</span><span class="sxs-lookup"><span data-stu-id="09ff3-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="09ff3-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-139">**11**</span><span class="sxs-lookup"><span data-stu-id="09ff3-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="09ff3-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-141">**12**</span><span class="sxs-lookup"><span data-stu-id="09ff3-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-143">**13**</span><span class="sxs-lookup"><span data-stu-id="09ff3-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="09ff3-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-145">**14**</span><span class="sxs-lookup"><span data-stu-id="09ff3-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-147">**15**</span><span class="sxs-lookup"><span data-stu-id="09ff3-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-149">**16**</span><span class="sxs-lookup"><span data-stu-id="09ff3-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-151">**17**</span><span class="sxs-lookup"><span data-stu-id="09ff3-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="09ff3-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-153">**19**</span><span class="sxs-lookup"><span data-stu-id="09ff3-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="09ff3-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-155">**19**</span><span class="sxs-lookup"><span data-stu-id="09ff3-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="09ff3-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-157">**20**</span><span class="sxs-lookup"><span data-stu-id="09ff3-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="09ff3-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-159">**21**</span><span class="sxs-lookup"><span data-stu-id="09ff3-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-160">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="09ff3-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-161">**22**</span><span class="sxs-lookup"><span data-stu-id="09ff3-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-162">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="09ff3-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-163">**23**</span><span class="sxs-lookup"><span data-stu-id="09ff3-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-164">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="09ff3-165">**24**</span><span class="sxs-lookup"><span data-stu-id="09ff3-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="09ff3-166">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="09ff3-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09ff3-167">Notes</span><span class="sxs-lookup"><span data-stu-id="09ff3-167">Remarks</span></span>

<span data-ttu-id="09ff3-168">Bien qu’il puisse sembler qu’il n’y ait aucune différence pratique entre un service arrêté et un service suspendu, les deux États apparaissent différemment pour le SCM.</span><span class="sxs-lookup"><span data-stu-id="09ff3-168">Although there might appear to be no practical difference between a service that is stopped and a service that is paused, the two states appear differently to the SCM.</span></span> <span data-ttu-id="09ff3-169">Un service arrêté est un service qui n’est pas en cours d’exécution et doit suivre l’intégralité de la procédure de démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="09ff3-169">A stopped service is a service that is not running and must go through the entire service start procedure.</span></span> <span data-ttu-id="09ff3-170">Toutefois, un service suspendu est toujours en cours d’exécution, mais son fonctionnement est suspendu.</span><span class="sxs-lookup"><span data-stu-id="09ff3-170">A paused service, however, is still running but has had its functioning is suspended.</span></span> <span data-ttu-id="09ff3-171">Pour cette raison, un service suspendu n’a pas besoin de traverser l’intégralité de la procédure de démarrage du service, mais il a besoin d’une procédure différente pour reprendre son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="09ff3-171">Because of this, a paused service does not need to go through the entire service start procedure but needs a different procedure to resume functioning.</span></span>

<span data-ttu-id="09ff3-172">Vous devez utiliser la méthode appropriée pour démarrer un service qui a été arrêté ou pour reprendre un service qui a été suspendu.</span><span class="sxs-lookup"><span data-stu-id="09ff3-172">You must use the proper method to start a service that has been stopped or to resume a service that has been paused.</span></span> <span data-ttu-id="09ff3-173">Les méthodes de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) [**StartService**](win32-terminalservice-startservice.md) et **ResumeService** doivent être utilisées dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="09ff3-173">The [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) methods [**StartService**](win32-terminalservice-startservice.md) and **ResumeService** should be used in the following situations:</span></span>

-   <span data-ttu-id="09ff3-174">Si un service est actuellement arrêté, vous devez utiliser la méthode [**StartService**](win32-terminalservice-startservice.md) pour le redémarrer ; **ResumeService** ne peut pas démarrer un service qui est actuellement arrêté.</span><span class="sxs-lookup"><span data-stu-id="09ff3-174">If a service is currently stopped, you must use the [**StartService**](win32-terminalservice-startservice.md) method to restart it; **ResumeService** cannot start a service that is currently stopped.</span></span>
-   <span data-ttu-id="09ff3-175">Si un service est suspendu, vous devez utiliser **ResumeService**.</span><span class="sxs-lookup"><span data-stu-id="09ff3-175">If a service is paused, you must use **ResumeService**.</span></span> <span data-ttu-id="09ff3-176">Si vous utilisez la méthode [**StartService**](win32-terminalservice-startservice.md) sur un service suspendu, vous recevez le message « le service est déjà en cours d’exécution ».</span><span class="sxs-lookup"><span data-stu-id="09ff3-176">If you use the [**StartService**](win32-terminalservice-startservice.md) method on a paused service, you receive the message, "The service is already running."</span></span> <span data-ttu-id="09ff3-177">Toutefois, le service reste en pause jusqu’à ce que le code de contrôle de reprise du service lui soit envoyé.</span><span class="sxs-lookup"><span data-stu-id="09ff3-177">However, the service remains paused until the resume service control code is sent to it.</span></span>

## <a name="examples"></a><span data-ttu-id="09ff3-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="09ff3-178">Examples</span></span>

<span data-ttu-id="09ff3-179">L’exemple de [reprise des services AutoStart qui sont en pause](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript redémarre tous les services à démarrage automatique qui ont été suspendus.</span><span class="sxs-lookup"><span data-stu-id="09ff3-179">The [Resume AutoStart Services that are Paused](https://Gallery.TechNet.Microsoft.Com/413f2896-e7f3-4b3e-96cb-5abdc9bb6c36) VBScript sample restarts any auto-start services that have been paused.</span></span>

## <a name="requirements"></a><span data-ttu-id="09ff3-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09ff3-180">Requirements</span></span>



| <span data-ttu-id="09ff3-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09ff3-181">Requirement</span></span> | <span data-ttu-id="09ff3-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="09ff3-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09ff3-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ff3-183">Minimum supported client</span></span><br/> | <span data-ttu-id="09ff3-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09ff3-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09ff3-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="09ff3-185">Minimum supported server</span></span><br/> | <span data-ttu-id="09ff3-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09ff3-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09ff3-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="09ff3-187">Namespace</span></span><br/>                | <span data-ttu-id="09ff3-188">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="09ff3-188">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="09ff3-189">MOF</span><span class="sxs-lookup"><span data-stu-id="09ff3-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09ff3-190"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09ff3-190"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="09ff3-191">DLL</span><span class="sxs-lookup"><span data-stu-id="09ff3-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09ff3-192"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09ff3-192"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09ff3-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09ff3-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09ff3-194">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="09ff3-194">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="09ff3-195">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="09ff3-195">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="09ff3-196">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="09ff3-196">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="09ff3-197">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="09ff3-197">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

