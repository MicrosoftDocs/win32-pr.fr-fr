---
title: Méthode GetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)
description: Retourne le descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- Windows Management Instrumentation de script, sécurité
- Windows Management Instrumentation de sécurité, scripts
- Services Bureau à distance de la méthode GetSecurityDescriptor
- Services Bureau à distance de la méthode GetSecurityDescriptor, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode GetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf8dc271d5498163352af10bcb0b9c55e2e81fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941986"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="03821-108">Méthode GetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="03821-108">GetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="03821-109">La méthode **GetSecurityDescriptor** retourne le descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="03821-109">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="03821-110">Le descripteur est retourné sous la forme d’une instance de l’expression [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="03821-110">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="03821-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03821-111">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="03821-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03821-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03821-113">*Descripteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="03821-113">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03821-114">Descripteur de sécurité associé au service.</span><span class="sxs-lookup"><span data-stu-id="03821-114">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03821-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03821-115">Return value</span></span>

<span data-ttu-id="03821-116">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="03821-116">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="03821-117">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="03821-117">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="03821-118">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="03821-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="03821-119">**0**</span><span class="sxs-lookup"><span data-stu-id="03821-119">**0**</span></span>
</dt> <dd>

<span data-ttu-id="03821-120">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="03821-120">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="03821-121">**1**</span><span class="sxs-lookup"><span data-stu-id="03821-121">**1**</span></span>
</dt> <dd>

<span data-ttu-id="03821-122">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="03821-122">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="03821-123">**2**</span><span class="sxs-lookup"><span data-stu-id="03821-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="03821-124">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="03821-124">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="03821-125">**3**</span><span class="sxs-lookup"><span data-stu-id="03821-125">**3**</span></span>
</dt> <dd>

<span data-ttu-id="03821-126">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="03821-126">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="03821-127">**4**</span><span class="sxs-lookup"><span data-stu-id="03821-127">**4**</span></span>
</dt> <dd>

<span data-ttu-id="03821-128">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="03821-128">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="03821-129">**5**</span><span class="sxs-lookup"><span data-stu-id="03821-129">**5**</span></span>
</dt> <dd>

<span data-ttu-id="03821-130">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="03821-130">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="03821-131">**6**</span><span class="sxs-lookup"><span data-stu-id="03821-131">**6**</span></span>
</dt> <dd>

<span data-ttu-id="03821-132">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="03821-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="03821-133">**7**</span><span class="sxs-lookup"><span data-stu-id="03821-133">**7**</span></span>
</dt> <dd>

<span data-ttu-id="03821-134">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="03821-134">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="03821-135">**8**</span><span class="sxs-lookup"><span data-stu-id="03821-135">**8**</span></span>
</dt> <dd>

<span data-ttu-id="03821-136">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="03821-136">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="03821-137">**9**</span><span class="sxs-lookup"><span data-stu-id="03821-137">**9**</span></span>
</dt> <dd>

<span data-ttu-id="03821-138">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="03821-138">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="03821-139">**10**</span><span class="sxs-lookup"><span data-stu-id="03821-139">**10**</span></span>
</dt> <dd>

<span data-ttu-id="03821-140">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="03821-140">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="03821-141">**11**</span><span class="sxs-lookup"><span data-stu-id="03821-141">**11**</span></span>
</dt> <dd>

<span data-ttu-id="03821-142">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="03821-142">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="03821-143">**12**</span><span class="sxs-lookup"><span data-stu-id="03821-143">**12**</span></span>
</dt> <dd>

<span data-ttu-id="03821-144">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="03821-144">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03821-145">**13**</span><span class="sxs-lookup"><span data-stu-id="03821-145">**13**</span></span>
</dt> <dd>

<span data-ttu-id="03821-146">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="03821-146">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="03821-147">**14**</span><span class="sxs-lookup"><span data-stu-id="03821-147">**14**</span></span>
</dt> <dd>

<span data-ttu-id="03821-148">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="03821-148">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03821-149">**15**</span><span class="sxs-lookup"><span data-stu-id="03821-149">**15**</span></span>
</dt> <dd>

<span data-ttu-id="03821-150">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="03821-150">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="03821-151">**16**</span><span class="sxs-lookup"><span data-stu-id="03821-151">**16**</span></span>
</dt> <dd>

<span data-ttu-id="03821-152">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="03821-152">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03821-153">**17**</span><span class="sxs-lookup"><span data-stu-id="03821-153">**17**</span></span>
</dt> <dd>

<span data-ttu-id="03821-154">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="03821-154">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="03821-155">**19**</span><span class="sxs-lookup"><span data-stu-id="03821-155">**18**</span></span>
</dt> <dd>

<span data-ttu-id="03821-156">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="03821-156">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="03821-157">**19**</span><span class="sxs-lookup"><span data-stu-id="03821-157">**19**</span></span>
</dt> <dd>

<span data-ttu-id="03821-158">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="03821-158">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="03821-159">**20**</span><span class="sxs-lookup"><span data-stu-id="03821-159">**20**</span></span>
</dt> <dd>

<span data-ttu-id="03821-160">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="03821-160">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="03821-161">**21**</span><span class="sxs-lookup"><span data-stu-id="03821-161">**21**</span></span>
</dt> <dd>

<span data-ttu-id="03821-162">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="03821-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="03821-163">**22**</span><span class="sxs-lookup"><span data-stu-id="03821-163">**22**</span></span>
</dt> <dd>

<span data-ttu-id="03821-164">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="03821-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="03821-165">**23**</span><span class="sxs-lookup"><span data-stu-id="03821-165">**23**</span></span>
</dt> <dd>

<span data-ttu-id="03821-166">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="03821-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="03821-167">**24**</span><span class="sxs-lookup"><span data-stu-id="03821-167">**24**</span></span>
</dt> <dd>

<span data-ttu-id="03821-168">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="03821-168">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03821-169">Notes</span><span class="sxs-lookup"><span data-stu-id="03821-169">Remarks</span></span>

<span data-ttu-id="03821-170">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="03821-170">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="03821-171">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="03821-171">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="03821-172">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="03821-172">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="03821-173">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="03821-173">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="03821-174">Exemples</span><span class="sxs-lookup"><span data-stu-id="03821-174">Examples</span></span>

<span data-ttu-id="03821-175">Lorsque vous récupérez un descripteur de sécurité dans VBScript, veillez à « sécurité » et à exécuter en tant qu’administrateur, comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="03821-175">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="03821-176">Dans le cas contraire, votre code risque de générer une erreur d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="03821-176">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="03821-177">De même, dans VB.NET, veillez à définir « EnablePrivileges = true » et à exécuter l’application en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="03821-177">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="03821-178">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03821-178">Requirements</span></span>



| <span data-ttu-id="03821-179">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03821-179">Requirement</span></span> | <span data-ttu-id="03821-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="03821-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03821-181">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03821-181">Minimum supported client</span></span><br/> | <span data-ttu-id="03821-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03821-182">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="03821-183">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03821-183">Minimum supported server</span></span><br/> | <span data-ttu-id="03821-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03821-184">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="03821-185">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="03821-185">Namespace</span></span><br/>                | <span data-ttu-id="03821-186">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="03821-186">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="03821-187">MOF</span><span class="sxs-lookup"><span data-stu-id="03821-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03821-188"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03821-188"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="03821-189">DLL</span><span class="sxs-lookup"><span data-stu-id="03821-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03821-190"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03821-190"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03821-191">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03821-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03821-192">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="03821-192">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="03821-193">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="03821-193">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="03821-194">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="03821-194">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="03821-195">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="03821-195">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="03821-196">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="03821-196">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="03821-197">Contrôle de compte d’utilisateur et WMI</span><span class="sxs-lookup"><span data-stu-id="03821-197">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

