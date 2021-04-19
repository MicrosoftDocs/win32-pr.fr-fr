---
title: Méthode InterrogateService de la classe Win32_Service (Services Bureau à distance)
description: Demande que le service référencé met à jour son état dans Service Manager.
ms.assetid: 7B572049-416E-4429-BD53-119FF570B2D8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode InterrogateService
- Services Bureau à distance de la méthode InterrogateService, classe Win32_Service
- Win32_Service de la classe Services Bureau à distance, méthode InterrogateService
topic_type:
- apiref
api_name:
- Win32_Service.InterrogateService
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f53b3d5e1cced6b6820f9b7334551de47f333be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511562"
---
# <a name="interrogateservice-method-of-the-win32_service-class-remote-desktop-services"></a><span data-ttu-id="f4a66-106">Méthode InterrogateService de la classe Win32_Service (Services Bureau à distance)</span><span class="sxs-lookup"><span data-stu-id="f4a66-106">InterrogateService method of the Win32_Service class (Remote Desktop Services)</span></span>

<span data-ttu-id="f4a66-107">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** demande que le service référencé met à jour son état dans Service Manager.</span><span class="sxs-lookup"><span data-stu-id="f4a66-107">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="f4a66-108">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="f4a66-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f4a66-109">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="f4a66-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a66-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4a66-110">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="f4a66-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f4a66-111">Parameters</span></span>

<span data-ttu-id="f4a66-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="f4a66-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4a66-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f4a66-113">Return value</span></span>

<span data-ttu-id="f4a66-114">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="f4a66-114">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="f4a66-115">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f4a66-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f4a66-116">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="f4a66-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f4a66-117">**0**</span><span class="sxs-lookup"><span data-stu-id="f4a66-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-118">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="f4a66-118">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-119">**1**</span><span class="sxs-lookup"><span data-stu-id="f4a66-119">**1**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-120">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="f4a66-120">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-121">**2**</span><span class="sxs-lookup"><span data-stu-id="f4a66-121">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-122">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="f4a66-122">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-123">**3**</span><span class="sxs-lookup"><span data-stu-id="f4a66-123">**3**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-124">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="f4a66-124">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-125">**4**</span><span class="sxs-lookup"><span data-stu-id="f4a66-125">**4**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="f4a66-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-127">**5**</span><span class="sxs-lookup"><span data-stu-id="f4a66-127">**5**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-128">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="f4a66-128">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-129">**6**</span><span class="sxs-lookup"><span data-stu-id="f4a66-129">**6**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-130">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="f4a66-130">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-131">**7**</span><span class="sxs-lookup"><span data-stu-id="f4a66-131">**7**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-132">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="f4a66-132">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-133">**8**</span><span class="sxs-lookup"><span data-stu-id="f4a66-133">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-134">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="f4a66-134">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-135">**9**</span><span class="sxs-lookup"><span data-stu-id="f4a66-135">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-136">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="f4a66-136">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-137">**10**</span><span class="sxs-lookup"><span data-stu-id="f4a66-137">**10**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-138">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="f4a66-138">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-139">**11**</span><span class="sxs-lookup"><span data-stu-id="f4a66-139">**11**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-140">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="f4a66-140">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-141">**12**</span><span class="sxs-lookup"><span data-stu-id="f4a66-141">**12**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-142">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-142">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-143">**13**</span><span class="sxs-lookup"><span data-stu-id="f4a66-143">**13**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-144">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="f4a66-144">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-145">**14**</span><span class="sxs-lookup"><span data-stu-id="f4a66-145">**14**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-146">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-146">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-147">**15**</span><span class="sxs-lookup"><span data-stu-id="f4a66-147">**15**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-148">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-148">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-149">**16**</span><span class="sxs-lookup"><span data-stu-id="f4a66-149">**16**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-150">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-150">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-151">**17**</span><span class="sxs-lookup"><span data-stu-id="f4a66-151">**17**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-152">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f4a66-152">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-153">**19**</span><span class="sxs-lookup"><span data-stu-id="f4a66-153">**18**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-154">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="f4a66-154">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-155">**19**</span><span class="sxs-lookup"><span data-stu-id="f4a66-155">**19**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-156">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="f4a66-156">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-157">**20**</span><span class="sxs-lookup"><span data-stu-id="f4a66-157">**20**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-158">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="f4a66-158">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-159">**21**</span><span class="sxs-lookup"><span data-stu-id="f4a66-159">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-160">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="f4a66-160">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-161">**22**</span><span class="sxs-lookup"><span data-stu-id="f4a66-161">**22**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-162">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="f4a66-162">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-163">**23**</span><span class="sxs-lookup"><span data-stu-id="f4a66-163">**23**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-164">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-164">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="f4a66-165">**24**</span><span class="sxs-lookup"><span data-stu-id="f4a66-165">**24**</span></span>
</dt> <dd>

<span data-ttu-id="f4a66-166">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="f4a66-166">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4a66-167">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4a66-167">Requirements</span></span>



| <span data-ttu-id="f4a66-168">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4a66-168">Requirement</span></span> | <span data-ttu-id="f4a66-169">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4a66-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a66-170">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4a66-170">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a66-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4a66-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4a66-172">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4a66-172">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a66-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4a66-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4a66-174">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4a66-174">Namespace</span></span><br/>                | <span data-ttu-id="f4a66-175">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f4a66-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f4a66-176">MOF</span><span class="sxs-lookup"><span data-stu-id="f4a66-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4a66-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4a66-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4a66-178">DLL</span><span class="sxs-lookup"><span data-stu-id="f4a66-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4a66-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4a66-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4a66-180">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4a66-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a66-181">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="f4a66-181">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="f4a66-182">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="f4a66-182">Operating System Classes</span></span>](/windows/desktop/CIMWin32Prov/operating-system-classes)
</dt> <dt>

[<span data-ttu-id="f4a66-183">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="f4a66-183">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="f4a66-184">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="f4a66-184">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

