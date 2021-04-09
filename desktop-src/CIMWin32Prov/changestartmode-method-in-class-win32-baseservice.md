---
description: Modifie le mode de démarrage d’un objet de service dérivé de Win32 \_ BaseService.
ms.assetid: 33040632-6c04-4084-af09-8e1b8bc29090
ms.tgt_platform: multiple
title: Méthode ChangeStartMode de la classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9877300a2135b7082677193696cd2d11811ab3dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110626"
---
# <a name="changestartmode-method-of-the-win32_baseservice-class"></a><span data-ttu-id="7cf42-103">Méthode ChangeStartMode de la \_ classe Win32 BaseService</span><span class="sxs-lookup"><span data-stu-id="7cf42-103">ChangeStartMode method of the Win32\_BaseService class</span></span>

<span data-ttu-id="7cf42-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifie le mode de démarrage d’un objet de service dérivé de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="7cf42-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a service object derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="7cf42-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7cf42-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7cf42-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7cf42-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf42-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7cf42-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="7cf42-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7cf42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf42-109">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7cf42-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-110">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf42-110">Start mode of the Windows base service.</span></span> <span data-ttu-id="7cf42-111">La valeur par défaut est « Automatic ».</span><span class="sxs-lookup"><span data-stu-id="7cf42-111">The default is "Automatic".</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="7cf42-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="7cf42-112"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="7cf42-113">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7cf42-113">Device driver started by the operating system loader.</span></span> <span data-ttu-id="7cf42-114">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="7cf42-114">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span data-ttu-id="7cf42-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**Démarrage système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="7cf42-115"><span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**System Start** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="7cf42-116">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7cf42-116">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="7cf42-117">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="7cf42-117">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="7cf42-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="7cf42-118"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="7cf42-119">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-119">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="7cf42-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="7cf42-120"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="7cf42-121">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7cf42-121">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="7cf42-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="7cf42-122"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="7cf42-123">Le service est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7cf42-123">Service is disabled.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf42-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7cf42-124">Return value</span></span>

<span data-ttu-id="7cf42-125">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="7cf42-125">Returns one of the values listed in the following list or any other value to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="7cf42-126">**Success**</span><span class="sxs-lookup"><span data-stu-id="7cf42-126">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-127">0</span><span class="sxs-lookup"><span data-stu-id="7cf42-127">0</span></span>

<span data-ttu-id="7cf42-128">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="7cf42-128">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-129">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="7cf42-129">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-130">1</span><span class="sxs-lookup"><span data-stu-id="7cf42-130">1</span></span>

<span data-ttu-id="7cf42-131">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7cf42-131">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-132">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="7cf42-132">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-133">2</span><span class="sxs-lookup"><span data-stu-id="7cf42-133">2</span></span>

<span data-ttu-id="7cf42-134">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7cf42-134">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-135">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7cf42-135">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-136">3</span><span class="sxs-lookup"><span data-stu-id="7cf42-136">3</span></span>

<span data-ttu-id="7cf42-137">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="7cf42-137">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-138">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="7cf42-138">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-139">4</span><span class="sxs-lookup"><span data-stu-id="7cf42-139">4</span></span>

<span data-ttu-id="7cf42-140">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="7cf42-140">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-141">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="7cf42-141">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-142">5</span><span class="sxs-lookup"><span data-stu-id="7cf42-142">5</span></span>

<span data-ttu-id="7cf42-143">Le code de contrôle demandé ne peut pas être envoyé au service, car l’état du service (propriété de l'[**État**](win32-baseservice.md) de [**\_ BaseService Win32**](win32-baseservice.md)) est égal à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="7cf42-143">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md)[**State**](win32-baseservice.md) property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-144">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="7cf42-144">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-145">6</span><span class="sxs-lookup"><span data-stu-id="7cf42-145">6</span></span>

<span data-ttu-id="7cf42-146">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="7cf42-146">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-147">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="7cf42-147">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-148">7</span><span class="sxs-lookup"><span data-stu-id="7cf42-148">7</span></span>

<span data-ttu-id="7cf42-149">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="7cf42-149">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-150">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="7cf42-150">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-151">8</span><span class="sxs-lookup"><span data-stu-id="7cf42-151">8</span></span>

<span data-ttu-id="7cf42-152">Processus interactif.</span><span class="sxs-lookup"><span data-stu-id="7cf42-152">Interactive process.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-153">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="7cf42-153">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-154">9</span><span class="sxs-lookup"><span data-stu-id="7cf42-154">9</span></span>

<span data-ttu-id="7cf42-155">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7cf42-155">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-156">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="7cf42-156">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-157">10</span><span class="sxs-lookup"><span data-stu-id="7cf42-157">10</span></span>

<span data-ttu-id="7cf42-158">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="7cf42-158">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-159">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="7cf42-159">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-160">11</span><span class="sxs-lookup"><span data-stu-id="7cf42-160">11</span></span>

<span data-ttu-id="7cf42-161">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="7cf42-161">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-162">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="7cf42-162">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-163">12</span><span class="sxs-lookup"><span data-stu-id="7cf42-163">12</span></span>

<span data-ttu-id="7cf42-164">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-164">A dependency on which this service relies has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-165">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="7cf42-165">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-166">13</span><span class="sxs-lookup"><span data-stu-id="7cf42-166">13</span></span>

<span data-ttu-id="7cf42-167">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="7cf42-167">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-168">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="7cf42-168">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-169">14</span><span class="sxs-lookup"><span data-stu-id="7cf42-169">14</span></span>

<span data-ttu-id="7cf42-170">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-170">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-171">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="7cf42-171">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-172">15</span><span class="sxs-lookup"><span data-stu-id="7cf42-172">15</span></span>

<span data-ttu-id="7cf42-173">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-173">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-174">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="7cf42-174">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-175">16</span><span class="sxs-lookup"><span data-stu-id="7cf42-175">16</span></span>

<span data-ttu-id="7cf42-176">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-176">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-177">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="7cf42-177">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-178">17</span><span class="sxs-lookup"><span data-stu-id="7cf42-178">17</span></span>

<span data-ttu-id="7cf42-179">Il n'y a pas de thread d'exécution pour le service.</span><span class="sxs-lookup"><span data-stu-id="7cf42-179">There is no execution thread for the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-180">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="7cf42-180">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-181">18</span><span class="sxs-lookup"><span data-stu-id="7cf42-181">18</span></span>

<span data-ttu-id="7cf42-182">Le démarrage du service donne lieu à des dépendances circulaires.</span><span class="sxs-lookup"><span data-stu-id="7cf42-182">There are circular dependencies when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-183">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="7cf42-183">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-184">19</span><span class="sxs-lookup"><span data-stu-id="7cf42-184">19</span></span>

<span data-ttu-id="7cf42-185">Un service est en cours d'exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="7cf42-185">There is a service running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-186">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="7cf42-186">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-187">20</span><span class="sxs-lookup"><span data-stu-id="7cf42-187">20</span></span>

<span data-ttu-id="7cf42-188">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="7cf42-188">There are invalid characters in the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-189">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="7cf42-189">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-190">21</span><span class="sxs-lookup"><span data-stu-id="7cf42-190">21</span></span>

<span data-ttu-id="7cf42-191">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="7cf42-191">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-192">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="7cf42-192">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-193">22</span><span class="sxs-lookup"><span data-stu-id="7cf42-193">22</span></span>

<span data-ttu-id="7cf42-194">Le compte sous lequel ce service doit s’exécuter n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="7cf42-194">The account which this service is to run under is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-195">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="7cf42-195">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-196">23</span><span class="sxs-lookup"><span data-stu-id="7cf42-196">23</span></span>

<span data-ttu-id="7cf42-197">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-197">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-198">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="7cf42-198">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-199">24</span><span class="sxs-lookup"><span data-stu-id="7cf42-199">24</span></span>

<span data-ttu-id="7cf42-200">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="7cf42-200">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="7cf42-201">**Autres**</span><span class="sxs-lookup"><span data-stu-id="7cf42-201">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="7cf42-202">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="7cf42-202">25 4294967295</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7cf42-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7cf42-203">Requirements</span></span>



| <span data-ttu-id="7cf42-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7cf42-204">Requirement</span></span> | <span data-ttu-id="7cf42-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="7cf42-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf42-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cf42-206">Minimum supported client</span></span><br/> | <span data-ttu-id="7cf42-207">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7cf42-207">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7cf42-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7cf42-208">Minimum supported server</span></span><br/> | <span data-ttu-id="7cf42-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7cf42-209">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7cf42-210">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7cf42-210">Namespace</span></span><br/>                | <span data-ttu-id="7cf42-211">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="7cf42-211">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7cf42-212">MOF</span><span class="sxs-lookup"><span data-stu-id="7cf42-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7cf42-213"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7cf42-213"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7cf42-214">DLL</span><span class="sxs-lookup"><span data-stu-id="7cf42-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cf42-215"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cf42-215"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf42-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7cf42-216">See also</span></span>

<dl> <dt>

<span data-ttu-id="7cf42-217">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7cf42-217">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7cf42-218">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="7cf42-218">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> </dl>

 

