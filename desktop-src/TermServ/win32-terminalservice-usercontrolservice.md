---
title: Méthode UserControlService de la classe Win32_Service (Services Bureau à distance)
description: 'Méthode UserControlService de la classe Win32_Service (Services Bureau à distance) : tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.'
ms.assetid: 7B9020C1-2183-4FC4-ABCF-CE34111FF5D3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode UserControlService
- Services Bureau à distance de la méthode UserControlService, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode UserControlService
topic_type:
- apiref
api_name:
- Win32_Service.UserControlService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71a33056f596afaf577968a5c725b3f64f79b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090607"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="b6fe3-106">Méthode UserControlService de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="b6fe3-106">UserControlService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="b6fe3-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-107">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="b6fe3-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b6fe3-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b6fe3-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b6fe3-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6fe3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6fe3-110">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="b6fe3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6fe3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6fe3-112">*ControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b6fe3-112">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-113">Spécifie des valeurs définies (de 128 à 255) qui fournissent des commandes de contrôle spécifiques à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-113">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6fe3-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6fe3-114">Return value</span></span>

<span data-ttu-id="b6fe3-115">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-115">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="b6fe3-116">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b6fe3-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b6fe3-117">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b6fe3-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b6fe3-118">**0**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-118">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-119">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-119">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-120">**1**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-120">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-121">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-121">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-122">**2**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-122">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-123">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-123">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-124">**3**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-124">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-125">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-125">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-126">**4**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-126">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-127">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-127">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-128">**5**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-128">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-129">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-130">**6**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-130">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-131">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-131">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-132">**7**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-132">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-133">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-133">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-134">**8**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-134">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-135">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-135">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-136">**9**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-136">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-137">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-137">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-138">**10**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-138">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-139">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-139">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-140">**11**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-140">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-141">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-141">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-142">**12**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-142">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-143">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-143">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-144">**13**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-144">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-145">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-145">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-146">**14**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-146">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-147">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-147">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-148">**15**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-148">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-149">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-149">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-150">**16**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-150">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-151">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-151">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-152">**17**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-152">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-153">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-153">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-154">**19**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-154">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-155">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-155">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-156">**19**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-156">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-157">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-157">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-158">**20**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-158">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-159">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-159">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-160">**21**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-160">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-161">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-161">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-162">**22**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-162">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-163">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-163">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-164">**23**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-164">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-165">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-165">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b6fe3-166">**24**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-166">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b6fe3-167">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="b6fe3-167">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6fe3-168">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6fe3-168">Requirements</span></span>



| <span data-ttu-id="b6fe3-169">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6fe3-169">Requirement</span></span> | <span data-ttu-id="b6fe3-170">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6fe3-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6fe3-171">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6fe3-171">Minimum supported client</span></span><br/> | <span data-ttu-id="b6fe3-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6fe3-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6fe3-173">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6fe3-173">Minimum supported server</span></span><br/> | <span data-ttu-id="b6fe3-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6fe3-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6fe3-175">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b6fe3-175">Namespace</span></span><br/>                | <span data-ttu-id="b6fe3-176">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="b6fe3-176">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b6fe3-177">MOF</span><span class="sxs-lookup"><span data-stu-id="b6fe3-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6fe3-178"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6fe3-178"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6fe3-179">DLL</span><span class="sxs-lookup"><span data-stu-id="b6fe3-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6fe3-180"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6fe3-180"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6fe3-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6fe3-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6fe3-182">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-182">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="b6fe3-183">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="b6fe3-183">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="b6fe3-184">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="b6fe3-184">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> </dl>

 

