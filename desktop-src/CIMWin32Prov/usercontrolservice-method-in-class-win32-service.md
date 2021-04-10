---
description: Tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.
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
ms.openlocfilehash: 8c523617826bd5d608b8c6b1ee242863f7591a61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950798"
---
# <a name="usercontrolservice-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="7bb26-103">Méthode UserControlService de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7bb26-103">UserControlService method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7bb26-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UserControlService** tente d’envoyer un code de contrôle défini par l’utilisateur au service référencé.</span><span class="sxs-lookup"><span data-stu-id="7bb26-104">The **UserControlService** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to the referenced service.</span></span>

<span data-ttu-id="7bb26-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7bb26-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7bb26-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7bb26-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb26-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bb26-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="7bb26-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bb26-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb26-109">*ControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bb26-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-110">Spécifie des valeurs définies (de 128 à 255) qui fournissent des commandes de contrôle spécifiques à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7bb26-110">Specifies defined values (from 128 to 255) that provide control commands specific to a user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb26-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bb26-111">Return value</span></span>

<span data-ttu-id="7bb26-112">Retourne l’une des valeurs répertoriées dans la liste suivante, ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7bb26-112">Returns one of the values listed in the following list, or any other value to indicate an error.</span></span> <span data-ttu-id="7bb26-113">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7bb26-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7bb26-114">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7bb26-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7bb26-115">**0**</span><span class="sxs-lookup"><span data-stu-id="7bb26-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-116">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="7bb26-116">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-117">**1**</span><span class="sxs-lookup"><span data-stu-id="7bb26-117">**1**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-118">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7bb26-118">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-119">**2**</span><span class="sxs-lookup"><span data-stu-id="7bb26-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-120">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7bb26-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-121">**3**</span><span class="sxs-lookup"><span data-stu-id="7bb26-121">**3**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-122">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="7bb26-122">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-123">**4**</span><span class="sxs-lookup"><span data-stu-id="7bb26-123">**4**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-124">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="7bb26-124">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-125">**5**</span><span class="sxs-lookup"><span data-stu-id="7bb26-125">**5**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-126">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="7bb26-126">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-127">**6**</span><span class="sxs-lookup"><span data-stu-id="7bb26-127">**6**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-128">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="7bb26-128">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-129">**7**</span><span class="sxs-lookup"><span data-stu-id="7bb26-129">**7**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-130">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="7bb26-130">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-131">**8**</span><span class="sxs-lookup"><span data-stu-id="7bb26-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-132">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="7bb26-132">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-133">**9**</span><span class="sxs-lookup"><span data-stu-id="7bb26-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-134">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7bb26-134">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-135">**10**</span><span class="sxs-lookup"><span data-stu-id="7bb26-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-136">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7bb26-136">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-137">**11**</span><span class="sxs-lookup"><span data-stu-id="7bb26-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-138">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="7bb26-138">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-139">**12**</span><span class="sxs-lookup"><span data-stu-id="7bb26-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-140">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-140">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-141">**13**</span><span class="sxs-lookup"><span data-stu-id="7bb26-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-142">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="7bb26-142">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-143">**14**</span><span class="sxs-lookup"><span data-stu-id="7bb26-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-144">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-144">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-145">**15**</span><span class="sxs-lookup"><span data-stu-id="7bb26-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-146">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-146">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-147">**16**</span><span class="sxs-lookup"><span data-stu-id="7bb26-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-148">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-148">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-149">**17**</span><span class="sxs-lookup"><span data-stu-id="7bb26-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-150">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7bb26-150">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-151">**19**</span><span class="sxs-lookup"><span data-stu-id="7bb26-151">**18**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-152">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="7bb26-152">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-153">**19**</span><span class="sxs-lookup"><span data-stu-id="7bb26-153">**19**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-154">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="7bb26-154">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-155">**20**</span><span class="sxs-lookup"><span data-stu-id="7bb26-155">**20**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-156">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7bb26-156">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-157">**21**</span><span class="sxs-lookup"><span data-stu-id="7bb26-157">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-158">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="7bb26-158">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-159">**22**</span><span class="sxs-lookup"><span data-stu-id="7bb26-159">**22**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-160">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="7bb26-160">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-161">**23**</span><span class="sxs-lookup"><span data-stu-id="7bb26-161">**23**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-162">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-162">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7bb26-163">**24**</span><span class="sxs-lookup"><span data-stu-id="7bb26-163">**24**</span></span>
</dt> <dd>

<span data-ttu-id="7bb26-164">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="7bb26-164">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bb26-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bb26-165">Requirements</span></span>



| <span data-ttu-id="7bb26-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bb26-166">Requirement</span></span> | <span data-ttu-id="7bb26-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bb26-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb26-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bb26-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb26-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7bb26-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7bb26-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bb26-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb26-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7bb26-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7bb26-172">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7bb26-172">Namespace</span></span><br/>                | <span data-ttu-id="7bb26-173">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7bb26-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7bb26-174">MOF</span><span class="sxs-lookup"><span data-stu-id="7bb26-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bb26-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bb26-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bb26-176">DLL</span><span class="sxs-lookup"><span data-stu-id="7bb26-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bb26-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bb26-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb26-178">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bb26-178">See also</span></span>

<dl> <dt>

<span data-ttu-id="7bb26-179">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bb26-179">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7bb26-180">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="7bb26-180">**Win32\_Service**</span></span>](win32-service.md)
</dt> </dl>

 

