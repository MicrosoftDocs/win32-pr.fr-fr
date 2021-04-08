---
title: Méthode SetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)
description: Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: 4F03B798-0912-4A0D-B31E-419662D5849B
ms.tgt_platform: multiple
keywords:
- Windows Management Instrumentation de script, sécurité
- Windows Management Instrumentation de sécurité, scripts
- Services Bureau à distance de la méthode SetSecurityDescriptor
- Services Bureau à distance de la méthode SetSecurityDescriptor, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode SetSecurityDescriptor
topic_type:
- apiref
api_name:
- Win32_Service.SetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19a21f9730b4c1c0ab7b3ccf662ddb2d95da2ee2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743485"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="41d22-108">Méthode SetSecurityDescriptor de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="41d22-108">SetSecurityDescriptor method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="41d22-109">La méthode **SetSecurityDescriptor** écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="41d22-109">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d22-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41d22-110">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="41d22-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41d22-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d22-112">*Descripteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="41d22-112">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41d22-113">Descripteur de sécurité associé au service.</span><span class="sxs-lookup"><span data-stu-id="41d22-113">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d22-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41d22-114">Return value</span></span>

<span data-ttu-id="41d22-115">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="41d22-115">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="41d22-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="41d22-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="41d22-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="41d22-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="41d22-118">**0**</span><span class="sxs-lookup"><span data-stu-id="41d22-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-119">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="41d22-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-120">**1**</span><span class="sxs-lookup"><span data-stu-id="41d22-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-121">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="41d22-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-122">**2**</span><span class="sxs-lookup"><span data-stu-id="41d22-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-123">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="41d22-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-124">**3**</span><span class="sxs-lookup"><span data-stu-id="41d22-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-125">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="41d22-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-126">**4**</span><span class="sxs-lookup"><span data-stu-id="41d22-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-127">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="41d22-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-128">**5**</span><span class="sxs-lookup"><span data-stu-id="41d22-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-129">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="41d22-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-130">**6**</span><span class="sxs-lookup"><span data-stu-id="41d22-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-131">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="41d22-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-132">**7**</span><span class="sxs-lookup"><span data-stu-id="41d22-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-133">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="41d22-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-134">**8**</span><span class="sxs-lookup"><span data-stu-id="41d22-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-135">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="41d22-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-136">**9**</span><span class="sxs-lookup"><span data-stu-id="41d22-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-137">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="41d22-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-138">**10**</span><span class="sxs-lookup"><span data-stu-id="41d22-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-139">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="41d22-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-140">**11**</span><span class="sxs-lookup"><span data-stu-id="41d22-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-141">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="41d22-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-142">**12**</span><span class="sxs-lookup"><span data-stu-id="41d22-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-143">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="41d22-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-144">**13**</span><span class="sxs-lookup"><span data-stu-id="41d22-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-145">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="41d22-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-146">**14**</span><span class="sxs-lookup"><span data-stu-id="41d22-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-147">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="41d22-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-148">**15**</span><span class="sxs-lookup"><span data-stu-id="41d22-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-149">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="41d22-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-150">**16**</span><span class="sxs-lookup"><span data-stu-id="41d22-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-151">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="41d22-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-152">**17**</span><span class="sxs-lookup"><span data-stu-id="41d22-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-153">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="41d22-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-154">**19**</span><span class="sxs-lookup"><span data-stu-id="41d22-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-155">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="41d22-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-156">**19**</span><span class="sxs-lookup"><span data-stu-id="41d22-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-157">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="41d22-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-158">**20**</span><span class="sxs-lookup"><span data-stu-id="41d22-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-159">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="41d22-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-160">**21**</span><span class="sxs-lookup"><span data-stu-id="41d22-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-161">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="41d22-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-162">**22**</span><span class="sxs-lookup"><span data-stu-id="41d22-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-163">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="41d22-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-164">**23**</span><span class="sxs-lookup"><span data-stu-id="41d22-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-165">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="41d22-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="41d22-166">**24**</span><span class="sxs-lookup"><span data-stu-id="41d22-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="41d22-167">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="41d22-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41d22-168">Notes</span><span class="sxs-lookup"><span data-stu-id="41d22-168">Remarks</span></span>

<span data-ttu-id="41d22-169">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="41d22-169">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="41d22-170">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="41d22-170">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="41d22-171">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="41d22-171">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="41d22-172">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="41d22-172">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="41d22-173">Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="41d22-173">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="41d22-174">Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="41d22-174">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="41d22-175">**SE \_ DACL en \_ présence**</span><span class="sxs-lookup"><span data-stu-id="41d22-175">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="41d22-176">Indique que la liste DACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="41d22-176">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="41d22-177">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="41d22-177">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="41d22-178">**\_liste SACL se \_ présente**</span><span class="sxs-lookup"><span data-stu-id="41d22-178">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="41d22-179">Indique que la liste SACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="41d22-179">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="41d22-180">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="41d22-180">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="41d22-181">Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte.</span><span class="sxs-lookup"><span data-stu-id="41d22-181">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="41d22-182">Pour les scripts, le nom du privilège est **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="41d22-182">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="41d22-183">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="41d22-183">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="41d22-184">Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="41d22-184">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="41d22-185">Dans le cas contraire, WMI conserve les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="41d22-185">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="41d22-186">Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="41d22-186">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="41d22-187">Quand une nouvelle SACL a la **valeur null** dans un appel de cette méthode, le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="41d22-187">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="41d22-188">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41d22-188">Requirements</span></span>



| <span data-ttu-id="41d22-189">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d22-189">Requirement</span></span> | <span data-ttu-id="41d22-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="41d22-190">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d22-191">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d22-191">Minimum supported client</span></span><br/> | <span data-ttu-id="41d22-192">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41d22-192">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41d22-193">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d22-193">Minimum supported server</span></span><br/> | <span data-ttu-id="41d22-194">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41d22-194">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41d22-195">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="41d22-195">Namespace</span></span><br/>                | <span data-ttu-id="41d22-196">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="41d22-196">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="41d22-197">MOF</span><span class="sxs-lookup"><span data-stu-id="41d22-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41d22-198"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41d22-198"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="41d22-199">DLL</span><span class="sxs-lookup"><span data-stu-id="41d22-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41d22-200"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41d22-200"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d22-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41d22-201">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d22-202">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="41d22-202">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="41d22-203">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="41d22-203">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="41d22-204">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="41d22-204">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="41d22-205">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="41d22-205">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="41d22-206">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="41d22-206">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="41d22-207">Contrôle de compte d’utilisateur et WMI</span><span class="sxs-lookup"><span data-stu-id="41d22-207">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

