---
description: Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)-retourne le descripteur de sécurité qui contrôle l’accès au service.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096987"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="c1c40-103">Méthode GetSecurityDescriptor de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="c1c40-103">GetSecurityDescriptor method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="c1c40-104">La méthode **GetSecurityDescriptor** retourne le descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the service.</span></span> <span data-ttu-id="c1c40-105">Le descripteur est retourné sous la forme d’une instance de l’expression [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="c1c40-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c40-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1c40-106">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="c1c40-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1c40-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1c40-108">*Descripteur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c1c40-108">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-109">Descripteur de sécurité associé au service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-109">The security descriptor associated with the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1c40-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c1c40-110">Return value</span></span>

<span data-ttu-id="c1c40-111">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c1c40-111">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="c1c40-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="c1c40-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c1c40-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="c1c40-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c1c40-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="c1c40-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-115">0</span><span class="sxs-lookup"><span data-stu-id="c1c40-115">0</span></span>

<span data-ttu-id="c1c40-116">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="c1c40-116">The request was accepted.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-117">1</span><span class="sxs-lookup"><span data-stu-id="c1c40-117">1</span></span>

<span data-ttu-id="c1c40-118">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="c1c40-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c1c40-119">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="c1c40-119">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-120">2</span><span class="sxs-lookup"><span data-stu-id="c1c40-120">2</span></span>

<span data-ttu-id="c1c40-121">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c1c40-121">The user did not have the necessary access.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-122">3</span><span class="sxs-lookup"><span data-stu-id="c1c40-122">3</span></span>

<span data-ttu-id="c1c40-123">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="c1c40-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-124">4</span><span class="sxs-lookup"><span data-stu-id="c1c40-124">4</span></span>

<span data-ttu-id="c1c40-125">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-125">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-126">5</span><span class="sxs-lookup"><span data-stu-id="c1c40-126">5</span></span>

<span data-ttu-id="c1c40-127">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c1c40-127">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-128">6</span><span class="sxs-lookup"><span data-stu-id="c1c40-128">6</span></span>

<span data-ttu-id="c1c40-129">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="c1c40-129">The service has not been started.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-130">7</span><span class="sxs-lookup"><span data-stu-id="c1c40-130">7</span></span>

<span data-ttu-id="c1c40-131">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="c1c40-131">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="c1c40-132">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="c1c40-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-133">8</span><span class="sxs-lookup"><span data-stu-id="c1c40-133">8</span></span>

<span data-ttu-id="c1c40-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="c1c40-135">**Privilège manquant**</span><span class="sxs-lookup"><span data-stu-id="c1c40-135">**Privilege missing**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-136">9</span><span class="sxs-lookup"><span data-stu-id="c1c40-136">9</span></span>

<span data-ttu-id="c1c40-137">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="c1c40-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-138">10</span><span class="sxs-lookup"><span data-stu-id="c1c40-138">10</span></span>

<span data-ttu-id="c1c40-139">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="c1c40-139">The service is already running.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-140">11</span><span class="sxs-lookup"><span data-stu-id="c1c40-140">11</span></span>

<span data-ttu-id="c1c40-141">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c1c40-141">The database to add a new service is locked.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-142">12</span><span class="sxs-lookup"><span data-stu-id="c1c40-142">12</span></span>

<span data-ttu-id="c1c40-143">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-144">13</span><span class="sxs-lookup"><span data-stu-id="c1c40-144">13</span></span>

<span data-ttu-id="c1c40-145">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="c1c40-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-146">14</span><span class="sxs-lookup"><span data-stu-id="c1c40-146">14</span></span>

<span data-ttu-id="c1c40-147">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-147">The service has been disabled from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-148">15</span><span class="sxs-lookup"><span data-stu-id="c1c40-148">15</span></span>

<span data-ttu-id="c1c40-149">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-150">16</span><span class="sxs-lookup"><span data-stu-id="c1c40-150">16</span></span>

<span data-ttu-id="c1c40-151">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-151">This service is being removed from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-152">17</span><span class="sxs-lookup"><span data-stu-id="c1c40-152">17</span></span>

<span data-ttu-id="c1c40-153">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c1c40-153">The service has no execution thread.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-154">18</span><span class="sxs-lookup"><span data-stu-id="c1c40-154">18</span></span>

<span data-ttu-id="c1c40-155">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="c1c40-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-156">19</span><span class="sxs-lookup"><span data-stu-id="c1c40-156">19</span></span>

<span data-ttu-id="c1c40-157">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="c1c40-157">A service is running under the same name.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-158">20</span><span class="sxs-lookup"><span data-stu-id="c1c40-158">20</span></span>

<span data-ttu-id="c1c40-159">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="c1c40-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="c1c40-160">**Paramètre non valide**</span><span class="sxs-lookup"><span data-stu-id="c1c40-160">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-161">21</span><span class="sxs-lookup"><span data-stu-id="c1c40-161">21</span></span>

<span data-ttu-id="c1c40-162">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-162">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-163">22</span><span class="sxs-lookup"><span data-stu-id="c1c40-163">22</span></span>

<span data-ttu-id="c1c40-164">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="c1c40-164">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-165">23</span><span class="sxs-lookup"><span data-stu-id="c1c40-165">23</span></span>

<span data-ttu-id="c1c40-166">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-166">The service exists in the database of services available from the system.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="c1c40-167">24</span><span class="sxs-lookup"><span data-stu-id="c1c40-167">24</span></span>

<span data-ttu-id="c1c40-168">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="c1c40-168">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="c1c40-169">**Autre**</span><span class="sxs-lookup"><span data-stu-id="c1c40-169">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c1c40-170">22 4294967295</span><span class="sxs-lookup"><span data-stu-id="c1c40-170">22 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1c40-171">Notes </span><span class="sxs-lookup"><span data-stu-id="c1c40-171">Remarks</span></span>

<span data-ttu-id="c1c40-172">L' [**instance \_ Win32 SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) représente un type de données de [**\_ \_ contrôle de descripteur de sécurité**](/windows/desktop/SecAuthZ/security-descriptor-control) et contient une liste de contrôle d' [*accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) et une [*liste de contrôle d’accès système*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="c1c40-172">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="c1c40-173">Pour plus d’informations, consultez [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="c1c40-173">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="c1c40-174">Si le **droit SeSecurityPrivilege** n’est pas accordé ou activé lors de l’obtention d’un descripteur de sécurité, seule la liste DACL est retournée dans le descripteur de sécurité retourné.</span><span class="sxs-lookup"><span data-stu-id="c1c40-174">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="c1c40-175">Pour plus d’informations, consultez [**constantes de privilège**](/windows/desktop/WmiSdk/privilege-constants) et [exécution d’opérations privilégiées](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="c1c40-175">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="c1c40-176">Exemples</span><span class="sxs-lookup"><span data-stu-id="c1c40-176">Examples</span></span>

<span data-ttu-id="c1c40-177">Lorsque vous récupérez un descripteur de sécurité dans VBScript, veillez à « sécurité » et à exécuter en tant qu’administrateur, comme illustré dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="c1c40-177">When retrieving a security descriptor in VBScript, be sure to "Security" and run as as Admin, as shown in the following code snippet.</span></span> <span data-ttu-id="c1c40-178">Dans le cas contraire, votre code risque de générer une erreur d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="c1c40-178">Otherwise, your code may throw a permissions error.</span></span>


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



<span data-ttu-id="c1c40-179">De même, dans VB.NET, veillez à définir « EnablePrivileges = true » et à exécuter l’application en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="c1c40-179">Similarly, in VB.NET, be sure to set "EnablePrivileges = True" and run the Application as Admin.</span></span>


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a><span data-ttu-id="c1c40-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1c40-180">Requirements</span></span>



| <span data-ttu-id="c1c40-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1c40-181">Requirement</span></span> | <span data-ttu-id="c1c40-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1c40-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c40-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1c40-183">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c40-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1c40-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c1c40-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1c40-185">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c40-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1c40-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c1c40-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1c40-187">Namespace</span></span><br/>                | <span data-ttu-id="c1c40-188">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="c1c40-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c1c40-189">MOF</span><span class="sxs-lookup"><span data-stu-id="c1c40-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1c40-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c1c40-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1c40-191">DLL</span><span class="sxs-lookup"><span data-stu-id="c1c40-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1c40-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1c40-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c40-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1c40-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c40-194">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="c1c40-194">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="c1c40-195">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="c1c40-195">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="c1c40-196">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="c1c40-196">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="c1c40-197">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="c1c40-197">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[<span data-ttu-id="c1c40-198">Contrôle de compte d’utilisateur et WMI</span><span class="sxs-lookup"><span data-stu-id="c1c40-198">User Account Control and WMI</span></span>](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

