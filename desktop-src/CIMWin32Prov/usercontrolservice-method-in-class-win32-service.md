---
description: 'Méthode UserControlService de la classe Win32_Service (fournisseurs WMI CIMWin32) : tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.'
ms.assetid: a7132c9b-6faf-4182-a5b8-3f2334c1a74b
ms.tgt_platform: multiple
title: Méthode UserControlService de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 455128b35c2645c6aa6ea10f64d12dff392fecca
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099999"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="38770-103">Méthode UserControlService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="38770-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="38770-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.</span><span class="sxs-lookup"><span data-stu-id="38770-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="38770-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="38770-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="38770-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="38770-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="38770-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38770-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="38770-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38770-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38770-109">*ControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="38770-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38770-110">Spécifie des valeurs définies (de 128 à 255) qui fournissent des commandes de contrôle spécifiques à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="38770-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38770-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38770-111">Return value</span></span>

<span data-ttu-id="38770-112">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="38770-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="38770-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="38770-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="38770-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="38770-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="38770-115">**0**</span><span class="sxs-lookup"><span data-stu-id="38770-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="38770-116">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="38770-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="38770-117">**1**</span><span class="sxs-lookup"><span data-stu-id="38770-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="38770-118">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="38770-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="38770-119">**2**</span><span class="sxs-lookup"><span data-stu-id="38770-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="38770-120">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="38770-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="38770-121">**3**</span><span class="sxs-lookup"><span data-stu-id="38770-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="38770-122">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="38770-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="38770-123">**4**</span><span class="sxs-lookup"><span data-stu-id="38770-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="38770-124">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="38770-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="38770-125">**5**</span><span class="sxs-lookup"><span data-stu-id="38770-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="38770-126">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="38770-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="38770-127">**6**</span><span class="sxs-lookup"><span data-stu-id="38770-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="38770-128">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="38770-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="38770-129">**7**</span><span class="sxs-lookup"><span data-stu-id="38770-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="38770-130">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="38770-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="38770-131">**8**</span><span class="sxs-lookup"><span data-stu-id="38770-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="38770-132">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="38770-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="38770-133">**9**</span><span class="sxs-lookup"><span data-stu-id="38770-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="38770-134">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="38770-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="38770-135">**10**</span><span class="sxs-lookup"><span data-stu-id="38770-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="38770-136">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="38770-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="38770-137">**11**</span><span class="sxs-lookup"><span data-stu-id="38770-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="38770-138">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="38770-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="38770-139">**12**</span><span class="sxs-lookup"><span data-stu-id="38770-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="38770-140">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="38770-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="38770-141">**13**</span><span class="sxs-lookup"><span data-stu-id="38770-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="38770-142">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="38770-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="38770-143">**14**</span><span class="sxs-lookup"><span data-stu-id="38770-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="38770-144">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="38770-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="38770-145">**15**</span><span class="sxs-lookup"><span data-stu-id="38770-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="38770-146">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="38770-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="38770-147">**16**</span><span class="sxs-lookup"><span data-stu-id="38770-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="38770-148">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="38770-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="38770-149">**17**</span><span class="sxs-lookup"><span data-stu-id="38770-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="38770-150">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="38770-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="38770-151">**19**</span><span class="sxs-lookup"><span data-stu-id="38770-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="38770-152">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="38770-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="38770-153">**19**</span><span class="sxs-lookup"><span data-stu-id="38770-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="38770-154">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="38770-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="38770-155">**20**</span><span class="sxs-lookup"><span data-stu-id="38770-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="38770-156">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="38770-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="38770-157">**21**</span><span class="sxs-lookup"><span data-stu-id="38770-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="38770-158">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="38770-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="38770-159">**22**</span><span class="sxs-lookup"><span data-stu-id="38770-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="38770-160">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="38770-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="38770-161">**23**</span><span class="sxs-lookup"><span data-stu-id="38770-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="38770-162">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="38770-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="38770-163">**24**</span><span class="sxs-lookup"><span data-stu-id="38770-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="38770-164">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="38770-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38770-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38770-165">Requirements</span></span>



| <span data-ttu-id="38770-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38770-166">Requirement</span></span> | <span data-ttu-id="38770-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="38770-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38770-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38770-168">Minimum supported client</span></span><br/> | <span data-ttu-id="38770-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38770-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38770-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="38770-170">Minimum supported server</span></span><br/> | <span data-ttu-id="38770-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38770-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38770-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="38770-172">Namespace</span></span><br/>                | <span data-ttu-id="38770-173">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="38770-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38770-174">MOF</span><span class="sxs-lookup"><span data-stu-id="38770-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38770-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38770-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38770-176">DLL</span><span class="sxs-lookup"><span data-stu-id="38770-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38770-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38770-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38770-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38770-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="38770-179">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38770-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="38770-180">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="38770-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

