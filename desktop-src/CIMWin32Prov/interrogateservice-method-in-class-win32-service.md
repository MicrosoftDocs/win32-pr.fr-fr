---
description: 'Méthode InterrogateService de la classe Win32_Service (fournisseurs WMI CIMWin32) : demande que le service référencé met à jour son état dans Service Manager.'
ms.assetid: a4ea8753-1859-4d97-b9ca-47598c7e7654
ms.tgt_platform: multiple
title: Méthode InterrogateService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.InterrogateService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9702bc3fbd0a9969db20a8f1326c31b9ea7d925d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096977"
---
# <a name="interrogateservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="b7fc2-103">Méthode InterrogateService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b7fc2-103">InterrogateService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b7fc2-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **InterrogateService** demande que le service référencé met à jour son état dans Service Manager.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-104">The **InterrogateService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method requests that the referenced service update its state to the service manager.</span></span>

<span data-ttu-id="b7fc2-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b7fc2-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b7fc2-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b7fc2-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7fc2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7fc2-107">Syntax</span></span>


```mof
uint32 InterrogateService();
```



## <a name="parameters"></a><span data-ttu-id="b7fc2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7fc2-108">Parameters</span></span>

<span data-ttu-id="b7fc2-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7fc2-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b7fc2-110">Return value</span></span>

<span data-ttu-id="b7fc2-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="b7fc2-112">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="b7fc2-112">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="b7fc2-113">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="b7fc2-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="b7fc2-114">**0**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-114">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-115">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-115">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-116">**1**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-116">**1**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-118">**2**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-119">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-119">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-120">**3**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-120">**3**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-121">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-121">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-122">**4**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-122">**4**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-123">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-123">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-124">**5**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-124">**5**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-125">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-125">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-126">**6**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-126">**6**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-127">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-127">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-128">**7**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-128">**7**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-129">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-129">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-130">**8**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-130">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-131">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-131">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-132">**9**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-132">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-133">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-133">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-134">**10**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-134">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-135">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-135">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-136">**11**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-136">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-137">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-137">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-138">**12**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-138">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-139">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-139">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-140">**13**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-140">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-141">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-141">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-142">**14**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-142">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-143">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-143">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-144">**15**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-144">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-145">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-145">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-146">**16**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-146">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-147">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-147">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-148">**17**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-148">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-149">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-149">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-150">**19**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-150">**18**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-151">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-151">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-152">**19**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-152">**19**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-153">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-153">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-154">**20**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-154">**20**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-155">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-155">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-156">**21**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-156">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-157">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-157">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-158">**22**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-158">**22**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-159">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-159">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-160">**23**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-160">**23**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-161">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-161">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="b7fc2-162">**24**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-162">**24**</span></span>
</dt> <dd>

<span data-ttu-id="b7fc2-163">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="b7fc2-163">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7fc2-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7fc2-164">Requirements</span></span>



| <span data-ttu-id="b7fc2-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7fc2-165">Requirement</span></span> | <span data-ttu-id="b7fc2-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7fc2-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7fc2-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fc2-167">Minimum supported client</span></span><br/> | <span data-ttu-id="b7fc2-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7fc2-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7fc2-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7fc2-169">Minimum supported server</span></span><br/> | <span data-ttu-id="b7fc2-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7fc2-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7fc2-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7fc2-171">Namespace</span></span><br/>                | <span data-ttu-id="b7fc2-172">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="b7fc2-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7fc2-173">MOF</span><span class="sxs-lookup"><span data-stu-id="b7fc2-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7fc2-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7fc2-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7fc2-175">DLL</span><span class="sxs-lookup"><span data-stu-id="b7fc2-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7fc2-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7fc2-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7fc2-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7fc2-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7fc2-178">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-178">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

<span data-ttu-id="b7fc2-179">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7fc2-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b7fc2-180">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="b7fc2-180">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="b7fc2-181">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="b7fc2-181">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

