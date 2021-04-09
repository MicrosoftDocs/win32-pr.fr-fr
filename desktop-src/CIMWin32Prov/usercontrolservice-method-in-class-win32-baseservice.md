---
description: Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Méthode UserControlService de la classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861598"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a><span data-ttu-id="066a9-103">Méthode UserControlService de la \_ classe Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="066a9-103">UserControlService method of the Win32\_BaseService class</span></span>

<span data-ttu-id="066a9-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) tente d’envoyer un code de contrôle défini par l’utilisateur à un service.</span><span class="sxs-lookup"><span data-stu-id="066a9-104">The [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method attempts to send a user-defined control code to a service.</span></span>

<span data-ttu-id="066a9-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="066a9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="066a9-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="066a9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="066a9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="066a9-107">Syntax</span></span>


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a><span data-ttu-id="066a9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="066a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="066a9-109">*ControlCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="066a9-109">*ControlCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="066a9-110">Valeur qui spécifie une commande de contrôle pour un service.</span><span class="sxs-lookup"><span data-stu-id="066a9-110">Value that specifies a control command to a service.</span></span> <span data-ttu-id="066a9-111">Par exemple, une commande de contrôle est une commande « suspendre » ou « continuer ».</span><span class="sxs-lookup"><span data-stu-id="066a9-111">For example a control command is a "pause" or "continue" command.</span></span> <span data-ttu-id="066a9-112">La valeur peut être un code prédéfini, ou une valeur et une action que le service définit.</span><span class="sxs-lookup"><span data-stu-id="066a9-112">The value can be a predefined code, or a value and action that the service defines.</span></span> <span data-ttu-id="066a9-113">Les codes de contrôle prédéfinis sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="066a9-113">The following are the predefined control codes:</span></span>

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span data-ttu-id="066a9-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_le contrôle du service \_ continue**</span><span class="sxs-lookup"><span data-stu-id="066a9-114"><span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**SERVICE\_CONTROL\_CONTINUE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-115">Avertit un service suspendu de reprendre.</span><span class="sxs-lookup"><span data-stu-id="066a9-115">Notifies a paused service to resume.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span data-ttu-id="066a9-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**interrogation du contrôle des services \_ \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-116"><span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**SERVICE\_CONTROL\_INTERROGATE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-117">Avertit un service qu’il doit signaler les informations d’état actuelles au gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="066a9-117">Notifies a service to report the current status information to the service control manager.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span data-ttu-id="066a9-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_NETBINDADD de contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-118"><span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**SERVICE\_CONTROL\_NETBINDADD**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-119">Notifie un service réseau qu’il existe un nouveau composant pour la liaison.</span><span class="sxs-lookup"><span data-stu-id="066a9-119">Notifies a network service that there is a new component for binding.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span data-ttu-id="066a9-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_NETBINDDISABLE de contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-120"><span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**SERVICE\_CONTROL\_NETBINDDISABLE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-121">Notifie un service réseau qu’une de ses liaisons est désactivée.</span><span class="sxs-lookup"><span data-stu-id="066a9-121">Notifies a network service that one of its bindings is disabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span data-ttu-id="066a9-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_NETBINDENABLE de contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-122"><span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**SERVICE\_CONTROL\_NETBINDENABLE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-123">Notifie un service réseau qu’une liaison désactivée est activée.</span><span class="sxs-lookup"><span data-stu-id="066a9-123">Notifies a network service that a disabled binding is enabled.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span data-ttu-id="066a9-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_NETBINDREMOVE de contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-124"><span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**SERVICE\_CONTROL\_NETBINDREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-125">Notifie un service réseau qu’un composant pour la liaison a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="066a9-125">Notifies a network service that a component for binding has been removed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span data-ttu-id="066a9-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_PARAMCHANGE de contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-126"><span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**SERVICE\_CONTROL\_PARAMCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-127">Avertit un service que ses paramètres de démarrage sont modifiés.</span><span class="sxs-lookup"><span data-stu-id="066a9-127">Notifies a service that its startup parameters are changed.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span data-ttu-id="066a9-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_suspension du contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-128"><span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**SERVICE\_CONTROL\_PAUSE**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-129">Notifie un service de s’interrompre.</span><span class="sxs-lookup"><span data-stu-id="066a9-129">Notifies a service to pause.</span></span>

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span data-ttu-id="066a9-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_arrêt du contrôle de service \_**</span><span class="sxs-lookup"><span data-stu-id="066a9-130"><span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**SERVICE\_CONTROL\_STOP**</span></span>


</dt> <dd>

<span data-ttu-id="066a9-131">Notifie l’arrêt d’un service.</span><span class="sxs-lookup"><span data-stu-id="066a9-131">Notifies a service to stop.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="066a9-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="066a9-132">Return value</span></span>

<span data-ttu-id="066a9-133">Retourne l’une des valeurs répertoriées dans la liste suivante, ou une valeur différente pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="066a9-133">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="066a9-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="066a9-134">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-135">0</span><span class="sxs-lookup"><span data-stu-id="066a9-135">0</span></span>

<span data-ttu-id="066a9-136">La demande est acceptée.</span><span class="sxs-lookup"><span data-stu-id="066a9-136">The request is accepted.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-137">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="066a9-137">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-138">1</span><span class="sxs-lookup"><span data-stu-id="066a9-138">1</span></span>

<span data-ttu-id="066a9-139">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="066a9-139">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-140">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="066a9-140">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-141">2</span><span class="sxs-lookup"><span data-stu-id="066a9-141">2</span></span>

<span data-ttu-id="066a9-142">L’utilisateur ne dispose pas des droits d’accès nécessaires.</span><span class="sxs-lookup"><span data-stu-id="066a9-142">The user does not have the necessary access rights.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-143">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="066a9-143">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-144">3</span><span class="sxs-lookup"><span data-stu-id="066a9-144">3</span></span>

<span data-ttu-id="066a9-145">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="066a9-145">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-146">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="066a9-146">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-147">4</span><span class="sxs-lookup"><span data-stu-id="066a9-147">4</span></span>

<span data-ttu-id="066a9-148">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="066a9-148">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-149">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="066a9-149">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-150">5</span><span class="sxs-lookup"><span data-stu-id="066a9-150">5</span></span>

<span data-ttu-id="066a9-151">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="066a9-151">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-152">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="066a9-152">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-153">6</span><span class="sxs-lookup"><span data-stu-id="066a9-153">6</span></span>

<span data-ttu-id="066a9-154">Ce service n'a pas démarré.</span><span class="sxs-lookup"><span data-stu-id="066a9-154">The service has not started.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-155">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="066a9-155">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-156">7</span><span class="sxs-lookup"><span data-stu-id="066a9-156">7</span></span>

<span data-ttu-id="066a9-157">Le service ne répond pas rapidement à la demande de démarrage.</span><span class="sxs-lookup"><span data-stu-id="066a9-157">The service does not respond to the start request quickly.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-158">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="066a9-158">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-159">8</span><span class="sxs-lookup"><span data-stu-id="066a9-159">8</span></span>

<span data-ttu-id="066a9-160">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="066a9-160">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-161">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="066a9-161">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-162">9</span><span class="sxs-lookup"><span data-stu-id="066a9-162">9</span></span>

<span data-ttu-id="066a9-163">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="066a9-163">The directory path to the service executable file is not found.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-164">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="066a9-164">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-165">10</span><span class="sxs-lookup"><span data-stu-id="066a9-165">10</span></span>

<span data-ttu-id="066a9-166">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="066a9-166">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-167">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="066a9-167">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-168">11</span><span class="sxs-lookup"><span data-stu-id="066a9-168">11</span></span>

<span data-ttu-id="066a9-169">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="066a9-169">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-170">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="066a9-170">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-171">12</span><span class="sxs-lookup"><span data-stu-id="066a9-171">12</span></span>

<span data-ttu-id="066a9-172">Une dépendance sur laquelle repose ce service est supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="066a9-172">A dependency that this service relies on is removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-173">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="066a9-173">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-174">13</span><span class="sxs-lookup"><span data-stu-id="066a9-174">13</span></span>

<span data-ttu-id="066a9-175">Le service ne trouve pas le service nécessaire à partir d’un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="066a9-175">The service does not find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-176">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="066a9-176">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-177">14</span><span class="sxs-lookup"><span data-stu-id="066a9-177">14</span></span>

<span data-ttu-id="066a9-178">Le service est désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="066a9-178">The service is disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-179">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="066a9-179">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-180">15</span><span class="sxs-lookup"><span data-stu-id="066a9-180">15</span></span>

<span data-ttu-id="066a9-181">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="066a9-181">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-182">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="066a9-182">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-183">16</span><span class="sxs-lookup"><span data-stu-id="066a9-183">16</span></span>

<span data-ttu-id="066a9-184">Le service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="066a9-184">The service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-185">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="066a9-185">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-186">17</span><span class="sxs-lookup"><span data-stu-id="066a9-186">17</span></span>

<span data-ttu-id="066a9-187">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="066a9-187">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-188">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="066a9-188">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-189">18</span><span class="sxs-lookup"><span data-stu-id="066a9-189">18</span></span>

<span data-ttu-id="066a9-190">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="066a9-190">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-191">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="066a9-191">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-192">19</span><span class="sxs-lookup"><span data-stu-id="066a9-192">19</span></span>

<span data-ttu-id="066a9-193">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="066a9-193">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-194">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="066a9-194">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-195">20</span><span class="sxs-lookup"><span data-stu-id="066a9-195">20</span></span>

<span data-ttu-id="066a9-196">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="066a9-196">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-197">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="066a9-197">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-198">21</span><span class="sxs-lookup"><span data-stu-id="066a9-198">21</span></span>

<span data-ttu-id="066a9-199">Des paramètres non valides ont été passés au service.</span><span class="sxs-lookup"><span data-stu-id="066a9-199">Invalid parameters have passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-200">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="066a9-200">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-201">22</span><span class="sxs-lookup"><span data-stu-id="066a9-201">22</span></span>

<span data-ttu-id="066a9-202">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="066a9-202">The account that this service runs under is not valid or does not have the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-203">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="066a9-203">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-204">23</span><span class="sxs-lookup"><span data-stu-id="066a9-204">23</span></span>

<span data-ttu-id="066a9-205">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="066a9-205">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-206">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="066a9-206">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-207">24</span><span class="sxs-lookup"><span data-stu-id="066a9-207">24</span></span>

<span data-ttu-id="066a9-208">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="066a9-208">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="066a9-209">**Autres**</span><span class="sxs-lookup"><span data-stu-id="066a9-209">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="066a9-210">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="066a9-210">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="066a9-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="066a9-211">Requirements</span></span>



| <span data-ttu-id="066a9-212">Condition requise</span><span class="sxs-lookup"><span data-stu-id="066a9-212">Requirement</span></span> | <span data-ttu-id="066a9-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="066a9-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="066a9-214">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066a9-214">Minimum supported client</span></span><br/> | <span data-ttu-id="066a9-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="066a9-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="066a9-216">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="066a9-216">Minimum supported server</span></span><br/> | <span data-ttu-id="066a9-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="066a9-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="066a9-218">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="066a9-218">Namespace</span></span><br/>                | <span data-ttu-id="066a9-219">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="066a9-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="066a9-220">MOF</span><span class="sxs-lookup"><span data-stu-id="066a9-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="066a9-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="066a9-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="066a9-222">DLL</span><span class="sxs-lookup"><span data-stu-id="066a9-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="066a9-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066a9-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066a9-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="066a9-224">See also</span></span>

<dl> <dt>

<span data-ttu-id="066a9-225">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="066a9-225">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="066a9-226">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="066a9-226">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

