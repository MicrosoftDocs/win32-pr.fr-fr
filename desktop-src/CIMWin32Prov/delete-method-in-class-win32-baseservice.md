---
description: La méthode Delete WMI Class supprime un service existant.
ms.assetid: 040005a0-9584-4458-bd1e-a2d50f53a637
ms.tgt_platform: multiple
title: Méthode Delete de la classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4683887aa8844e682a572126d3ad134315273c6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111523"
---
# <a name="delete-method-of-the-win32_baseservice-class"></a><span data-ttu-id="1d63b-103">Méthode Delete de la \_ classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="1d63b-103">Delete method of the Win32\_BaseService class</span></span>

<span data-ttu-id="1d63b-104">La méthode **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="1d63b-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method deletes an existing service.</span></span>

<span data-ttu-id="1d63b-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="1d63b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1d63b-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1d63b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d63b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d63b-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="1d63b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d63b-108">Parameters</span></span>

<span data-ttu-id="1d63b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d63b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d63b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d63b-110">Return value</span></span>

<span data-ttu-id="1d63b-111">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="1d63b-111">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1d63b-112">**Success**</span><span class="sxs-lookup"><span data-stu-id="1d63b-112">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-113">0</span><span class="sxs-lookup"><span data-stu-id="1d63b-113">0</span></span>

<span data-ttu-id="1d63b-114">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="1d63b-114">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-115">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="1d63b-115">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-116">1</span><span class="sxs-lookup"><span data-stu-id="1d63b-116">1</span></span>

<span data-ttu-id="1d63b-117">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="1d63b-117">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-118">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="1d63b-118">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-119">2</span><span class="sxs-lookup"><span data-stu-id="1d63b-119">2</span></span>

<span data-ttu-id="1d63b-120">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="1d63b-120">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-121">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="1d63b-121">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-122">3</span><span class="sxs-lookup"><span data-stu-id="1d63b-122">3</span></span>

<span data-ttu-id="1d63b-123">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="1d63b-123">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-124">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="1d63b-124">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-125">4</span><span class="sxs-lookup"><span data-stu-id="1d63b-125">4</span></span>

<span data-ttu-id="1d63b-126">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="1d63b-126">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-127">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="1d63b-127">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-128">5</span><span class="sxs-lookup"><span data-stu-id="1d63b-128">5</span></span>

<span data-ttu-id="1d63b-129">Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété de l'[**État**](win32-baseservice.md) de [**\_ BaseService Win32**](win32-baseservice.md)) est égal à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="1d63b-129">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-130">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="1d63b-130">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-131">6</span><span class="sxs-lookup"><span data-stu-id="1d63b-131">6</span></span>

<span data-ttu-id="1d63b-132">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="1d63b-132">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-133">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="1d63b-133">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-134">7</span><span class="sxs-lookup"><span data-stu-id="1d63b-134">7</span></span>

<span data-ttu-id="1d63b-135">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="1d63b-135">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-136">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="1d63b-136">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-137">8</span><span class="sxs-lookup"><span data-stu-id="1d63b-137">8</span></span>

<span data-ttu-id="1d63b-138">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="1d63b-138">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-139">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="1d63b-139">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-140">9</span><span class="sxs-lookup"><span data-stu-id="1d63b-140">9</span></span>

<span data-ttu-id="1d63b-141">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="1d63b-141">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-142">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="1d63b-142">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-143">10</span><span class="sxs-lookup"><span data-stu-id="1d63b-143">10</span></span>

<span data-ttu-id="1d63b-144">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="1d63b-144">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-145">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="1d63b-145">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-146">11</span><span class="sxs-lookup"><span data-stu-id="1d63b-146">11</span></span>

<span data-ttu-id="1d63b-147">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="1d63b-147">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-148">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="1d63b-148">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-149">12</span><span class="sxs-lookup"><span data-stu-id="1d63b-149">12</span></span>

<span data-ttu-id="1d63b-150">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-150">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-151">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="1d63b-151">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-152">13</span><span class="sxs-lookup"><span data-stu-id="1d63b-152">13</span></span>

<span data-ttu-id="1d63b-153">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="1d63b-153">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-154">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="1d63b-154">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-155">14</span><span class="sxs-lookup"><span data-stu-id="1d63b-155">14</span></span>

<span data-ttu-id="1d63b-156">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-156">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-157">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="1d63b-157">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-158">15</span><span class="sxs-lookup"><span data-stu-id="1d63b-158">15</span></span>

<span data-ttu-id="1d63b-159">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-159">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-160">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="1d63b-160">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-161">16</span><span class="sxs-lookup"><span data-stu-id="1d63b-161">16</span></span>

<span data-ttu-id="1d63b-162">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-162">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-163">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="1d63b-163">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-164">17</span><span class="sxs-lookup"><span data-stu-id="1d63b-164">17</span></span>

<span data-ttu-id="1d63b-165">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="1d63b-165">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-166">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="1d63b-166">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-167">18</span><span class="sxs-lookup"><span data-stu-id="1d63b-167">18</span></span>

<span data-ttu-id="1d63b-168">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="1d63b-168">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-169">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="1d63b-169">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-170">19</span><span class="sxs-lookup"><span data-stu-id="1d63b-170">19</span></span>

<span data-ttu-id="1d63b-171">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="1d63b-171">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-172">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="1d63b-172">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-173">20</span><span class="sxs-lookup"><span data-stu-id="1d63b-173">20</span></span>

<span data-ttu-id="1d63b-174">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="1d63b-174">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-175">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="1d63b-175">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-176">21</span><span class="sxs-lookup"><span data-stu-id="1d63b-176">21</span></span>

<span data-ttu-id="1d63b-177">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="1d63b-177">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-178">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="1d63b-178">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-179">22</span><span class="sxs-lookup"><span data-stu-id="1d63b-179">22</span></span>

<span data-ttu-id="1d63b-180">Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="1d63b-180">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-181">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="1d63b-181">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-182">23</span><span class="sxs-lookup"><span data-stu-id="1d63b-182">23</span></span>

<span data-ttu-id="1d63b-183">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-183">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-184">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="1d63b-184">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-185">24</span><span class="sxs-lookup"><span data-stu-id="1d63b-185">24</span></span>

<span data-ttu-id="1d63b-186">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="1d63b-186">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d63b-187">**Autres**</span><span class="sxs-lookup"><span data-stu-id="1d63b-187">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1d63b-188">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="1d63b-188">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d63b-189">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d63b-189">Requirements</span></span>



| <span data-ttu-id="1d63b-190">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d63b-190">Requirement</span></span> | <span data-ttu-id="1d63b-191">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d63b-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d63b-192">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d63b-192">Minimum supported client</span></span><br/> | <span data-ttu-id="1d63b-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d63b-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d63b-194">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d63b-194">Minimum supported server</span></span><br/> | <span data-ttu-id="1d63b-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d63b-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d63b-196">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1d63b-196">Namespace</span></span><br/>                | <span data-ttu-id="1d63b-197">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="1d63b-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d63b-198">MOF</span><span class="sxs-lookup"><span data-stu-id="1d63b-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d63b-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d63b-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d63b-200">DLL</span><span class="sxs-lookup"><span data-stu-id="1d63b-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d63b-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d63b-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d63b-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d63b-202">See also</span></span>

<dl> <dt>

<span data-ttu-id="1d63b-203">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d63b-203">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1d63b-204">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="1d63b-204">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

