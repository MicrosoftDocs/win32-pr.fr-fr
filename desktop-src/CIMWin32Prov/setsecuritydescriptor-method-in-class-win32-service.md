---
description: Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)-écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: c1745b69-f355-4b4c-9e58-6a76c230f498
ms.tgt_platform: multiple
title: Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20619a459171841d0a3bd5b7acabe984dc835dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100003"
---
# <a name="setsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="a3aed-103">Méthode SetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a3aed-103">SetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a3aed-104">La méthode **SetSecurityDescriptor** écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3aed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3aed-105">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="a3aed-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3aed-107">*Descripteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a3aed-107">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-108">Descripteur de sécurité associé au service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-108">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3aed-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3aed-109">Return value</span></span>

<span data-ttu-id="a3aed-110">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="a3aed-110">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="a3aed-111">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="a3aed-111">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a3aed-112">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="a3aed-112">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a3aed-113">**Success**</span><span class="sxs-lookup"><span data-stu-id="a3aed-113">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-114">0</span><span class="sxs-lookup"><span data-stu-id="a3aed-114">0</span></span>

<span data-ttu-id="a3aed-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="a3aed-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-116">**1**</span><span class="sxs-lookup"><span data-stu-id="a3aed-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a3aed-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-118">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="a3aed-118">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-119">2</span><span class="sxs-lookup"><span data-stu-id="a3aed-119">2</span></span>

<span data-ttu-id="a3aed-120">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a3aed-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-121">**3**</span><span class="sxs-lookup"><span data-stu-id="a3aed-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-122">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="a3aed-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-123">**4**</span><span class="sxs-lookup"><span data-stu-id="a3aed-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-124">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-125">**5**</span><span class="sxs-lookup"><span data-stu-id="a3aed-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-126">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="a3aed-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-127">**6**</span><span class="sxs-lookup"><span data-stu-id="a3aed-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-128">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="a3aed-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-129">**7**</span><span class="sxs-lookup"><span data-stu-id="a3aed-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-130">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="a3aed-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-131">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="a3aed-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-132">8</span><span class="sxs-lookup"><span data-stu-id="a3aed-132">8</span></span>

<span data-ttu-id="a3aed-133">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-133">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-134">**Privilège manquant**</span><span class="sxs-lookup"><span data-stu-id="a3aed-134">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-135">9</span><span class="sxs-lookup"><span data-stu-id="a3aed-135">9</span></span>

<span data-ttu-id="a3aed-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="a3aed-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-137">**10**</span><span class="sxs-lookup"><span data-stu-id="a3aed-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="a3aed-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-139">**11**</span><span class="sxs-lookup"><span data-stu-id="a3aed-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="a3aed-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-141">**12**</span><span class="sxs-lookup"><span data-stu-id="a3aed-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-143">**13**</span><span class="sxs-lookup"><span data-stu-id="a3aed-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="a3aed-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-145">**14**</span><span class="sxs-lookup"><span data-stu-id="a3aed-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-147">**15**</span><span class="sxs-lookup"><span data-stu-id="a3aed-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-149">**16**</span><span class="sxs-lookup"><span data-stu-id="a3aed-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-151">**17**</span><span class="sxs-lookup"><span data-stu-id="a3aed-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a3aed-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-153">**19**</span><span class="sxs-lookup"><span data-stu-id="a3aed-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="a3aed-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-155">**19**</span><span class="sxs-lookup"><span data-stu-id="a3aed-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="a3aed-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-157">**20**</span><span class="sxs-lookup"><span data-stu-id="a3aed-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="a3aed-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-159">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="a3aed-159">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-160">21</span><span class="sxs-lookup"><span data-stu-id="a3aed-160">21</span></span>

<span data-ttu-id="a3aed-161">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-162">**22**</span><span class="sxs-lookup"><span data-stu-id="a3aed-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-163">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="a3aed-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-164">**23**</span><span class="sxs-lookup"><span data-stu-id="a3aed-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-165">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-166">**24**</span><span class="sxs-lookup"><span data-stu-id="a3aed-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-167">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="a3aed-167">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="a3aed-168">**Autre**</span><span class="sxs-lookup"><span data-stu-id="a3aed-168">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a3aed-169">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="a3aed-169">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3aed-170">Notes </span><span class="sxs-lookup"><span data-stu-id="a3aed-170">Remarks</span></span>

<span data-ttu-id="a3aed-171">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="a3aed-171">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="a3aed-172">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="a3aed-172">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="a3aed-173">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="a3aed-173">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="a3aed-174">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="a3aed-174">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="a3aed-175">Vous pouvez mettre à jour la liste DACL et la liste SACL dans l’instance [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) lors de l’appel de cette méthode, mais vous pouvez également mettre à jour uniquement la liste DACL ou uniquement la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="a3aed-175">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="a3aed-176">Les valeurs suivantes dans [**le \_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) déterminent si la liste DACL, la liste SACL ou les deux sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a3aed-176">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="a3aed-177">**SE \_ DACL en \_ présence**</span><span class="sxs-lookup"><span data-stu-id="a3aed-177">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="a3aed-178">Indique que la liste DACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a3aed-178">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="a3aed-179">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste DACL.</span><span class="sxs-lookup"><span data-stu-id="a3aed-179">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="a3aed-180">**\_liste SACL se \_ présente**</span><span class="sxs-lookup"><span data-stu-id="a3aed-180">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="a3aed-181">Indique que la liste SACL doit être mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a3aed-181">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="a3aed-182">Si cette valeur n’est pas définie, WMI conserve la valeur d’origine de la liste SACL.</span><span class="sxs-lookup"><span data-stu-id="a3aed-182">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="a3aed-183">Pour mettre à jour la liste SACL, le privilège **SeSecurityPrivilege** doit être activé sur le compte.</span><span class="sxs-lookup"><span data-stu-id="a3aed-183">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="a3aed-184">Pour les scripts, le nom du privilège est **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="a3aed-184">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="a3aed-185">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="a3aed-185">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="a3aed-186">Si les propriétés tiers de confiance du groupe et tiers de confiance du propriétaire ne sont pas **null**, elles sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="a3aed-186">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="a3aed-187">Dans le cas contraire, WMI conserve les valeurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3aed-187">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="a3aed-188">Pour plus d’informations, consultez [objets descripteurs de sécurité WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="a3aed-188">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="a3aed-189">Quand une nouvelle SACL a la **valeur null** dans un appel de cette méthode, le descripteur de sécurité SACL de l’objet sécurisable cible reste inchangé.</span><span class="sxs-lookup"><span data-stu-id="a3aed-189">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3aed-190">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3aed-190">Requirements</span></span>



| <span data-ttu-id="a3aed-191">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3aed-191">Requirement</span></span> | <span data-ttu-id="a3aed-192">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3aed-192">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aed-193">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3aed-193">Minimum supported client</span></span><br/> | <span data-ttu-id="a3aed-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3aed-194">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3aed-195">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3aed-195">Minimum supported server</span></span><br/> | <span data-ttu-id="a3aed-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3aed-196">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3aed-197">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a3aed-197">Namespace</span></span><br/>                | <span data-ttu-id="a3aed-198">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="a3aed-198">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3aed-199">MOF</span><span class="sxs-lookup"><span data-stu-id="a3aed-199">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3aed-200"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3aed-200"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3aed-201">DLL</span><span class="sxs-lookup"><span data-stu-id="a3aed-201">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3aed-202"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3aed-202"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3aed-203">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3aed-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3aed-204">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="a3aed-204">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="a3aed-205">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="a3aed-205">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="a3aed-206">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="a3aed-206">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="a3aed-207">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="a3aed-207">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="a3aed-208">Contrôle de compte d’utilisateur et WMI</span><span class="sxs-lookup"><span data-stu-id="a3aed-208">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

