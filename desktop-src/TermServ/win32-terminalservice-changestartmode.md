---
title: Méthode ChangeStartMode de la classe Win32_Service (Services Bureau à distance)
description: Modifie le mode de démarrage d’un \_ TerminalService Win32.
ms.assetid: 4F4B8CFC-B38C-47C6-A2BA-D498EC2B7F55
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ChangeStartMode
- Services Bureau à distance de la méthode ChangeStartMode, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode ChangeStartMode
topic_type:
- apiref
api_name:
- Win32_Service.ChangeStartMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a46c6b72fbb070dac32b2b6990a217068c77da9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510534"
---
# <a name="changestartmode-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="9b10a-106">Méthode ChangeStartMode de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="9b10a-106">ChangeStartMode method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="9b10a-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifie le mode de démarrage d' [**un \_ TerminalService Win32**](win32-terminalservice.md).</span><span class="sxs-lookup"><span data-stu-id="9b10a-107">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_TerminalService**](win32-terminalservice.md).</span></span>

<span data-ttu-id="9b10a-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="9b10a-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9b10a-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9b10a-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9b10a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b10a-110">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode
);
```



## <a name="parameters"></a><span data-ttu-id="9b10a-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b10a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b10a-112">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b10a-112">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-113">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="9b10a-113">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="9b10a-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Partition**</span><span class="sxs-lookup"><span data-stu-id="9b10a-114"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot**</span></span>


</dt> <dd>

<span data-ttu-id="9b10a-115">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9b10a-115">Device driver started by the operating system loader.</span></span> <span data-ttu-id="9b10a-116">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="9b10a-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="9b10a-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Requise**</span><span class="sxs-lookup"><span data-stu-id="9b10a-117"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System**</span></span>


</dt> <dd>

<span data-ttu-id="9b10a-118">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9b10a-118">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="9b10a-119">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="9b10a-119">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="9b10a-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatique**</span><span class="sxs-lookup"><span data-stu-id="9b10a-120"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic**</span></span>


</dt> <dd>

<span data-ttu-id="9b10a-121">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-121">Service to be started automatically by the Service Control Manager during system startup.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="9b10a-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuelle**</span><span class="sxs-lookup"><span data-stu-id="9b10a-122"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual**</span></span>


</dt> <dd>

<span data-ttu-id="9b10a-123">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](win32-terminalservice-startservice.md) .</span><span class="sxs-lookup"><span data-stu-id="9b10a-123">Service to be started by the Service Control Manager when a process calls the [**StartService**](win32-terminalservice-startservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9b10a-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Activée**</span><span class="sxs-lookup"><span data-stu-id="9b10a-124"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>


</dt> <dd>

<span data-ttu-id="9b10a-125">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="9b10a-125">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b10a-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b10a-126">Return value</span></span>

<span data-ttu-id="9b10a-127">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="9b10a-127">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="9b10a-128">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="9b10a-128">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="9b10a-129">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="9b10a-129">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="9b10a-130">**0**</span><span class="sxs-lookup"><span data-stu-id="9b10a-130">**0**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-131">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="9b10a-131">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-132">**1**</span><span class="sxs-lookup"><span data-stu-id="9b10a-132">**1**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-133">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9b10a-133">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-134">**2**</span><span class="sxs-lookup"><span data-stu-id="9b10a-134">**2**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-135">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9b10a-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-136">**3**</span><span class="sxs-lookup"><span data-stu-id="9b10a-136">**3**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-137">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="9b10a-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-138">**4**</span><span class="sxs-lookup"><span data-stu-id="9b10a-138">**4**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-139">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="9b10a-139">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-140">**5**</span><span class="sxs-lookup"><span data-stu-id="9b10a-140">**5**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-141">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="9b10a-141">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-142">**6**</span><span class="sxs-lookup"><span data-stu-id="9b10a-142">**6**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-143">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="9b10a-143">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-144">**7**</span><span class="sxs-lookup"><span data-stu-id="9b10a-144">**7**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-145">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="9b10a-145">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-146">**8**</span><span class="sxs-lookup"><span data-stu-id="9b10a-146">**8**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-147">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="9b10a-147">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-148">**9**</span><span class="sxs-lookup"><span data-stu-id="9b10a-148">**9**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-149">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="9b10a-149">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-150">**10**</span><span class="sxs-lookup"><span data-stu-id="9b10a-150">**10**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-151">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="9b10a-151">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-152">**11**</span><span class="sxs-lookup"><span data-stu-id="9b10a-152">**11**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-153">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="9b10a-153">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-154">**12**</span><span class="sxs-lookup"><span data-stu-id="9b10a-154">**12**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-155">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-155">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-156">**13**</span><span class="sxs-lookup"><span data-stu-id="9b10a-156">**13**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-157">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="9b10a-157">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-158">**14**</span><span class="sxs-lookup"><span data-stu-id="9b10a-158">**14**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-159">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-159">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-160">**15**</span><span class="sxs-lookup"><span data-stu-id="9b10a-160">**15**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-161">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-161">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-162">**16**</span><span class="sxs-lookup"><span data-stu-id="9b10a-162">**16**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-163">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-163">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-164">**17**</span><span class="sxs-lookup"><span data-stu-id="9b10a-164">**17**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-165">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9b10a-165">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-166">**19**</span><span class="sxs-lookup"><span data-stu-id="9b10a-166">**18**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-167">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="9b10a-167">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-168">**19**</span><span class="sxs-lookup"><span data-stu-id="9b10a-168">**19**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-169">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="9b10a-169">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-170">**20**</span><span class="sxs-lookup"><span data-stu-id="9b10a-170">**20**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-171">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="9b10a-171">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-172">**21**</span><span class="sxs-lookup"><span data-stu-id="9b10a-172">**21**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-173">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="9b10a-173">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-174">**22**</span><span class="sxs-lookup"><span data-stu-id="9b10a-174">**22**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-175">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="9b10a-175">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-176">**23**</span><span class="sxs-lookup"><span data-stu-id="9b10a-176">**23**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-177">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-177">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="9b10a-178">**24**</span><span class="sxs-lookup"><span data-stu-id="9b10a-178">**24**</span></span>
</dt> <dd>

<span data-ttu-id="9b10a-179">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="9b10a-179">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9b10a-180">Exemples</span><span class="sxs-lookup"><span data-stu-id="9b10a-180">Examples</span></span>

<span data-ttu-id="9b10a-181">Le [startMode de modification suivant d’un](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) exemple PowerShell de service, extrait de la Galerie TechNet, modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="9b10a-181">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="9b10a-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b10a-182">Requirements</span></span>



| <span data-ttu-id="9b10a-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b10a-183">Requirement</span></span> | <span data-ttu-id="9b10a-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b10a-184">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b10a-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b10a-185">Minimum supported client</span></span><br/> | <span data-ttu-id="9b10a-186">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b10a-186">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b10a-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9b10a-187">Minimum supported server</span></span><br/> | <span data-ttu-id="9b10a-188">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b10a-188">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b10a-189">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9b10a-189">Namespace</span></span><br/>                | <span data-ttu-id="9b10a-190">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="9b10a-190">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9b10a-191">MOF</span><span class="sxs-lookup"><span data-stu-id="9b10a-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b10a-192"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b10a-192"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b10a-193">DLL</span><span class="sxs-lookup"><span data-stu-id="9b10a-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b10a-194"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b10a-194"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b10a-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b10a-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b10a-196">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="9b10a-196">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="9b10a-197">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="9b10a-197">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="9b10a-198">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="9b10a-198">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="9b10a-199">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="9b10a-199">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

