---
description: Tente de placer le service géré par le pilote système dans son état de démarrage.
ms.assetid: 3f9d29aa-b549-4a55-be9c-01fad4932fe6
ms.tgt_platform: multiple
title: Méthode StartService de la classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2c189d9b5f24a3ccc803a588abb94337ee65a1da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201002"
---
# <a name="startservice-method-of-the-win32_systemdriver-class"></a><span data-ttu-id="8488c-103">Méthode StartService de la \_ classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="8488c-103">StartService method of the Win32\_SystemDriver class</span></span>

<span data-ttu-id="8488c-104">La méthode **StartService** tente de placer le service géré par le pilote système dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="8488c-104">The **StartService** method attempts to place the service managed by the system driver into its startup state.</span></span>

<span data-ttu-id="8488c-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="8488c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8488c-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8488c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8488c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8488c-107">Syntax</span></span>


```mof
uint32 StartService();
```



## <a name="parameters"></a><span data-ttu-id="8488c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8488c-108">Parameters</span></span>

<span data-ttu-id="8488c-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="8488c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8488c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8488c-110">Return value</span></span>

<span data-ttu-id="8488c-111">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8488c-111">Returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8488c-112">**0**</span><span class="sxs-lookup"><span data-stu-id="8488c-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-113">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="8488c-113">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-114">**1**</span><span class="sxs-lookup"><span data-stu-id="8488c-114">**1**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-115">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8488c-115">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-116">**2**</span><span class="sxs-lookup"><span data-stu-id="8488c-116">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-117">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="8488c-117">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-118">**3**</span><span class="sxs-lookup"><span data-stu-id="8488c-118">**3**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-119">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="8488c-119">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-120">**4**</span><span class="sxs-lookup"><span data-stu-id="8488c-120">**4**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-121">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="8488c-121">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-122">**5**</span><span class="sxs-lookup"><span data-stu-id="8488c-122">**5**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-123">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="8488c-123">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-124">**6**</span><span class="sxs-lookup"><span data-stu-id="8488c-124">**6**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-125">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="8488c-125">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-126">**7**</span><span class="sxs-lookup"><span data-stu-id="8488c-126">**7**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-127">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="8488c-127">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-128">**8**</span><span class="sxs-lookup"><span data-stu-id="8488c-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-129">Un échec inconnu s'est produit lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="8488c-129">An unknown failure occurred when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-130">**9**</span><span class="sxs-lookup"><span data-stu-id="8488c-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-131">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="8488c-131">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-132">**10**</span><span class="sxs-lookup"><span data-stu-id="8488c-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-133">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="8488c-133">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-134">**11**</span><span class="sxs-lookup"><span data-stu-id="8488c-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-135">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="8488c-135">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-136">**12**</span><span class="sxs-lookup"><span data-stu-id="8488c-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-137">Une dépendance sur laquelle ce service repose a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="8488c-137">A dependency for which this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-138">**13**</span><span class="sxs-lookup"><span data-stu-id="8488c-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-139">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="8488c-139">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-140">**14**</span><span class="sxs-lookup"><span data-stu-id="8488c-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-141">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="8488c-141">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-142">**15**</span><span class="sxs-lookup"><span data-stu-id="8488c-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-143">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="8488c-143">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-144">**16**</span><span class="sxs-lookup"><span data-stu-id="8488c-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-145">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="8488c-145">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-146">**17**</span><span class="sxs-lookup"><span data-stu-id="8488c-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-147">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="8488c-147">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-148">**19**</span><span class="sxs-lookup"><span data-stu-id="8488c-148">**18**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-149">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="8488c-149">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-150">**19**</span><span class="sxs-lookup"><span data-stu-id="8488c-150">**19**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-151">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="8488c-151">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-152">**20**</span><span class="sxs-lookup"><span data-stu-id="8488c-152">**20**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-153">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="8488c-153">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-154">**21**</span><span class="sxs-lookup"><span data-stu-id="8488c-154">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-155">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="8488c-155">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-156">**22**</span><span class="sxs-lookup"><span data-stu-id="8488c-156">**22**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-157">Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="8488c-157">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-158">**23**</span><span class="sxs-lookup"><span data-stu-id="8488c-158">**23**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-159">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="8488c-159">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="8488c-160">**24**</span><span class="sxs-lookup"><span data-stu-id="8488c-160">**24**</span></span>
</dt> <dd>

<span data-ttu-id="8488c-161">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="8488c-161">The service is currently paused in the system.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="8488c-162">Exemples</span><span class="sxs-lookup"><span data-stu-id="8488c-162">Examples</span></span>

<span data-ttu-id="8488c-163">Le code PowerShell suivant démarre le service « classe d’imprimante Microsoft USB ».</span><span class="sxs-lookup"><span data-stu-id="8488c-163">The following PowerShell code starts the "Microsoft USB Printer class" service.</span></span>


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.StartService()
"Start Service Called. Return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



## <a name="requirements"></a><span data-ttu-id="8488c-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8488c-164">Requirements</span></span>



| <span data-ttu-id="8488c-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8488c-165">Requirement</span></span> | <span data-ttu-id="8488c-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="8488c-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8488c-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8488c-167">Minimum supported client</span></span><br/> | <span data-ttu-id="8488c-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8488c-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8488c-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8488c-169">Minimum supported server</span></span><br/> | <span data-ttu-id="8488c-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8488c-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8488c-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8488c-171">Namespace</span></span><br/>                | <span data-ttu-id="8488c-172">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="8488c-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8488c-173">MOF</span><span class="sxs-lookup"><span data-stu-id="8488c-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8488c-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8488c-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8488c-175">DLL</span><span class="sxs-lookup"><span data-stu-id="8488c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8488c-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8488c-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8488c-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8488c-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="8488c-178">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8488c-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8488c-179">**\_SystemDriver Win32**</span><span class="sxs-lookup"><span data-stu-id="8488c-179">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)
</dt> </dl>

 

