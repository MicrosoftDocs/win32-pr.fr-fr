---
description: Modifie le mode de démarrage d’un \_ service Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Méthode ChangeStartMode de la classe Win32_Service (fournisseurs WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033669"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a><span data-ttu-id="933db-103">Méthode ChangeStartMode de la classe Win32_Service (fournisseurs WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="933db-103">ChangeStartMode method of the Win32_Service class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="933db-104">La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeStartMode** modifie le mode de démarrage d' [**un \_ service Win32**](win32-service.md).</span><span class="sxs-lookup"><span data-stu-id="933db-104">The **ChangeStartMode** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method modifies the start mode of a [**Win32\_Service**](win32-service.md).</span></span>

<span data-ttu-id="933db-105">Cette rubrique utilise la syntaxe format MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="933db-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="933db-106">Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="933db-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="933db-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="933db-107">Syntax</span></span>


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a><span data-ttu-id="933db-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="933db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933db-109">*StartMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="933db-109">*StartMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="933db-110">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="933db-110">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span data-ttu-id="933db-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>Démarrage du **démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="933db-111"><span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Boot Start** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="933db-112">Pilote de périphérique Démarré par le chargeur du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="933db-112">Device driver started by the operating system loader.</span></span> <span data-ttu-id="933db-113">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="933db-113">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="933db-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="933db-114"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="933db-115">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="933db-115">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="933db-116">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="933db-116">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span data-ttu-id="933db-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Démarrage automatique** (« automatique »)</span><span class="sxs-lookup"><span data-stu-id="933db-117"><span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Auto Start** ("Automatic")</span></span>


</dt> <dd>

<span data-ttu-id="933db-118">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="933db-118">Service to be started automatically by the service control manager during system startup.</span></span>

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span data-ttu-id="933db-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Début de la demande** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="933db-119"><span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Demand Start** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="933db-120">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="933db-120">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="933db-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="933db-121"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="933db-122">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="933db-122">Service that can no longer be started.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933db-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="933db-123">Return value</span></span>

<span data-ttu-id="933db-124">Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="933db-124">Returns one of the values listed in the following list or any other value to indicate an error.</span></span> <span data-ttu-id="933db-125">Pour obtenir d’autres codes d’erreur, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="933db-125">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="933db-126">Pour obtenir les valeurs de **HRESULT** générales, consultez [codes d’erreur système](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="933db-126">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="933db-127">**Success**</span><span class="sxs-lookup"><span data-stu-id="933db-127">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="933db-128">0</span><span class="sxs-lookup"><span data-stu-id="933db-128">0</span></span>

<span data-ttu-id="933db-129">La demande a été acceptée.</span><span class="sxs-lookup"><span data-stu-id="933db-129">The request was accepted.</span></span>

</dd> <dt>

<span data-ttu-id="933db-130">**Non pris en charge**</span><span class="sxs-lookup"><span data-stu-id="933db-130">**Not Supported**</span></span>
</dt> <dd>

<span data-ttu-id="933db-131">1</span><span class="sxs-lookup"><span data-stu-id="933db-131">1</span></span>

<span data-ttu-id="933db-132">La demande n'est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="933db-132">The request is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="933db-133">**Accès refusé**</span><span class="sxs-lookup"><span data-stu-id="933db-133">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="933db-134">2</span><span class="sxs-lookup"><span data-stu-id="933db-134">2</span></span>

<span data-ttu-id="933db-135">L’utilisateur n’a pas l’accès nécessaire.</span><span class="sxs-lookup"><span data-stu-id="933db-135">The user did not have the necessary access.</span></span>

</dd> <dt>

<span data-ttu-id="933db-136">**Services dépendants en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="933db-136">**Dependent Services Running**</span></span>
</dt> <dd>

<span data-ttu-id="933db-137">3</span><span class="sxs-lookup"><span data-stu-id="933db-137">3</span></span>

<span data-ttu-id="933db-138">Le service ne peut pas être arrêté car d'autres services en cours d'exécution en dépendent.</span><span class="sxs-lookup"><span data-stu-id="933db-138">The service cannot be stopped because other services that are running are dependent on it.</span></span>

</dd> <dt>

<span data-ttu-id="933db-139">**Contrôle de service non valide**</span><span class="sxs-lookup"><span data-stu-id="933db-139">**Invalid Service Control**</span></span>
</dt> <dd>

<span data-ttu-id="933db-140">4</span><span class="sxs-lookup"><span data-stu-id="933db-140">4</span></span>

<span data-ttu-id="933db-141">Le code de contrôle demandé n'est pas valide ou est inacceptable pour le service.</span><span class="sxs-lookup"><span data-stu-id="933db-141">The requested control code is not valid, or it is unacceptable to the service.</span></span>

</dd> <dt>

<span data-ttu-id="933db-142">**Le service ne peut pas accepter le contrôle**</span><span class="sxs-lookup"><span data-stu-id="933db-142">**Service Cannot Accept Control**</span></span>
</dt> <dd>

<span data-ttu-id="933db-143">5</span><span class="sxs-lookup"><span data-stu-id="933db-143">5</span></span>

<span data-ttu-id="933db-144">Le code de contrôle demandé ne peut pas être envoyé au service car l’état du service ([**Win32 \_ BaseService**](win32-baseservice.md).\*\*\*\* La propriété State) est égale à 0, 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="933db-144">The requested control code cannot be sent to the service because the state of the service ([**Win32\_BaseService**](win32-baseservice.md).**State** property) is equal to 0, 1, or 2.</span></span>

</dd> <dt>

<span data-ttu-id="933db-145">**Service non actif**</span><span class="sxs-lookup"><span data-stu-id="933db-145">**Service Not Active**</span></span>
</dt> <dd>

<span data-ttu-id="933db-146">6</span><span class="sxs-lookup"><span data-stu-id="933db-146">6</span></span>

<span data-ttu-id="933db-147">Le service n'a pas été démarré.</span><span class="sxs-lookup"><span data-stu-id="933db-147">The service has not been started.</span></span>

</dd> <dt>

<span data-ttu-id="933db-148">**Délai d’expiration de la demande de service**</span><span class="sxs-lookup"><span data-stu-id="933db-148">**Service Request Timeout**</span></span>
</dt> <dd>

<span data-ttu-id="933db-149">7</span><span class="sxs-lookup"><span data-stu-id="933db-149">7</span></span>

<span data-ttu-id="933db-150">Le service n'a pas répondu à la demande de démarrage en temps voulu.</span><span class="sxs-lookup"><span data-stu-id="933db-150">The service did not respond to the start request in a timely fashion.</span></span>

</dd> <dt>

<span data-ttu-id="933db-151">**Échec inconnu**</span><span class="sxs-lookup"><span data-stu-id="933db-151">**Unknown Failure**</span></span>
</dt> <dd>

<span data-ttu-id="933db-152">8</span><span class="sxs-lookup"><span data-stu-id="933db-152">8</span></span>

<span data-ttu-id="933db-153">Échec inconnu lors du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="933db-153">Unknown failure when starting the service.</span></span>

</dd> <dt>

<span data-ttu-id="933db-154">**Chemin introuvable**</span><span class="sxs-lookup"><span data-stu-id="933db-154">**Path Not Found**</span></span>
</dt> <dd>

<span data-ttu-id="933db-155">9</span><span class="sxs-lookup"><span data-stu-id="933db-155">9</span></span>

<span data-ttu-id="933db-156">Le chemin d’accès au répertoire du fichier exécutable du service est introuvable.</span><span class="sxs-lookup"><span data-stu-id="933db-156">The directory path to the service executable file was not found.</span></span>

</dd> <dt>

<span data-ttu-id="933db-157">**Service déjà en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="933db-157">**Service Already Running**</span></span>
</dt> <dd>

<span data-ttu-id="933db-158">10</span><span class="sxs-lookup"><span data-stu-id="933db-158">10</span></span>

<span data-ttu-id="933db-159">Le service est déjà en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="933db-159">The service is already running.</span></span>

</dd> <dt>

<span data-ttu-id="933db-160">**Base de données du service verrouillée**</span><span class="sxs-lookup"><span data-stu-id="933db-160">**Service Database Locked**</span></span>
</dt> <dd>

<span data-ttu-id="933db-161">11</span><span class="sxs-lookup"><span data-stu-id="933db-161">11</span></span>

<span data-ttu-id="933db-162">La base de données pour ajouter un nouveau service est verrouillée.</span><span class="sxs-lookup"><span data-stu-id="933db-162">The database to add a new service is locked.</span></span>

</dd> <dt>

<span data-ttu-id="933db-163">**Dépendance de service supprimée**</span><span class="sxs-lookup"><span data-stu-id="933db-163">**Service Dependency Deleted**</span></span>
</dt> <dd>

<span data-ttu-id="933db-164">12</span><span class="sxs-lookup"><span data-stu-id="933db-164">12</span></span>

<span data-ttu-id="933db-165">Une dépendance sur laquelle repose ce service a été supprimée du système.</span><span class="sxs-lookup"><span data-stu-id="933db-165">A dependency this service relies on has been removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-166">**Échec de la dépendance du service**</span><span class="sxs-lookup"><span data-stu-id="933db-166">**Service Dependency Failure**</span></span>
</dt> <dd>

<span data-ttu-id="933db-167">13</span><span class="sxs-lookup"><span data-stu-id="933db-167">13</span></span>

<span data-ttu-id="933db-168">Le service n'a pas pu trouver le service nécessaire à partir d'un service dépendant.</span><span class="sxs-lookup"><span data-stu-id="933db-168">The service failed to find the service needed from a dependent service.</span></span>

</dd> <dt>

<span data-ttu-id="933db-169">**Service désactivé**</span><span class="sxs-lookup"><span data-stu-id="933db-169">**Service Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="933db-170">14</span><span class="sxs-lookup"><span data-stu-id="933db-170">14</span></span>

<span data-ttu-id="933db-171">Le service a été désactivé du système.</span><span class="sxs-lookup"><span data-stu-id="933db-171">The service has been disabled from the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-172">**Échec de l’ouverture de session du service**</span><span class="sxs-lookup"><span data-stu-id="933db-172">**Service Logon Failed**</span></span>
</dt> <dd>

<span data-ttu-id="933db-173">15</span><span class="sxs-lookup"><span data-stu-id="933db-173">15</span></span>

<span data-ttu-id="933db-174">Le service ne dispose pas de l'authentification correcte pour être exécuté sur le système.</span><span class="sxs-lookup"><span data-stu-id="933db-174">The service does not have the correct authentication to run on the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-175">**Service marqué pour suppression**</span><span class="sxs-lookup"><span data-stu-id="933db-175">**Service Marked For Deletion**</span></span>
</dt> <dd>

<span data-ttu-id="933db-176">16</span><span class="sxs-lookup"><span data-stu-id="933db-176">16</span></span>

<span data-ttu-id="933db-177">Ce service est en cours de suppression du système.</span><span class="sxs-lookup"><span data-stu-id="933db-177">This service is being removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-178">**Service sans thread**</span><span class="sxs-lookup"><span data-stu-id="933db-178">**Service No Thread**</span></span>
</dt> <dd>

<span data-ttu-id="933db-179">17</span><span class="sxs-lookup"><span data-stu-id="933db-179">17</span></span>

<span data-ttu-id="933db-180">Le service n’a pas de thread d’exécution.</span><span class="sxs-lookup"><span data-stu-id="933db-180">The service has no execution thread.</span></span>

</dd> <dt>

<span data-ttu-id="933db-181">**Dépendance circulaire d’État**</span><span class="sxs-lookup"><span data-stu-id="933db-181">**Status Circular Dependency**</span></span>
</dt> <dd>

<span data-ttu-id="933db-182">18</span><span class="sxs-lookup"><span data-stu-id="933db-182">18</span></span>

<span data-ttu-id="933db-183">Le service a des dépendances circulaires lorsqu’il démarre.</span><span class="sxs-lookup"><span data-stu-id="933db-183">The service has circular dependencies when it starts.</span></span>

</dd> <dt>

<span data-ttu-id="933db-184">**Nom de l’État en double**</span><span class="sxs-lookup"><span data-stu-id="933db-184">**Status Duplicate Name**</span></span>
</dt> <dd>

<span data-ttu-id="933db-185">19</span><span class="sxs-lookup"><span data-stu-id="933db-185">19</span></span>

<span data-ttu-id="933db-186">Un service est en cours d’exécution sous le même nom.</span><span class="sxs-lookup"><span data-stu-id="933db-186">A service is running under the same name.</span></span>

</dd> <dt>

<span data-ttu-id="933db-187">**Nom de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="933db-187">**Status Invalid Name**</span></span>
</dt> <dd>

<span data-ttu-id="933db-188">20</span><span class="sxs-lookup"><span data-stu-id="933db-188">20</span></span>

<span data-ttu-id="933db-189">Le nom du service contient des caractères non valides.</span><span class="sxs-lookup"><span data-stu-id="933db-189">The service name has invalid characters.</span></span>

</dd> <dt>

<span data-ttu-id="933db-190">**Paramètre d’État non valide**</span><span class="sxs-lookup"><span data-stu-id="933db-190">**Status Invalid Parameter**</span></span>
</dt> <dd>

<span data-ttu-id="933db-191">21</span><span class="sxs-lookup"><span data-stu-id="933db-191">21</span></span>

<span data-ttu-id="933db-192">Des paramètres non valides ont été transmis au service.</span><span class="sxs-lookup"><span data-stu-id="933db-192">Invalid parameters have been passed to the service.</span></span>

</dd> <dt>

<span data-ttu-id="933db-193">**Compte de service de l’état non valide**</span><span class="sxs-lookup"><span data-stu-id="933db-193">**Status Invalid Service Account**</span></span>
</dt> <dd>

<span data-ttu-id="933db-194">22</span><span class="sxs-lookup"><span data-stu-id="933db-194">22</span></span>

<span data-ttu-id="933db-195">Le compte sous lequel ce service s’exécute n’est pas valide ou ne dispose pas des autorisations nécessaires pour exécuter le service.</span><span class="sxs-lookup"><span data-stu-id="933db-195">The account under which this service runs is either invalid or lacks the permissions to run the service.</span></span>

</dd> <dt>

<span data-ttu-id="933db-196">**Le service d’État existe**</span><span class="sxs-lookup"><span data-stu-id="933db-196">**Status Service Exists**</span></span>
</dt> <dd>

<span data-ttu-id="933db-197">23</span><span class="sxs-lookup"><span data-stu-id="933db-197">23</span></span>

<span data-ttu-id="933db-198">Le service existe dans la base de données des services disponibles dans le système.</span><span class="sxs-lookup"><span data-stu-id="933db-198">The service exists in the database of services available from the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-199">**Service déjà suspendu**</span><span class="sxs-lookup"><span data-stu-id="933db-199">**Service Already Paused**</span></span>
</dt> <dd>

<span data-ttu-id="933db-200">24</span><span class="sxs-lookup"><span data-stu-id="933db-200">24</span></span>

<span data-ttu-id="933db-201">Le service est actuellement mis en pause dans le système.</span><span class="sxs-lookup"><span data-stu-id="933db-201">The service is currently paused in the system.</span></span>

</dd> <dt>

<span data-ttu-id="933db-202">**Autres**</span><span class="sxs-lookup"><span data-stu-id="933db-202">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="933db-203">25 4294967295</span><span class="sxs-lookup"><span data-stu-id="933db-203">25 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="933db-204">Exemples</span><span class="sxs-lookup"><span data-stu-id="933db-204">Examples</span></span>

<span data-ttu-id="933db-205">Le [startMode de modification suivant d’un](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) exemple PowerShell de service, extrait de la Galerie TechNet, modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="933db-205">The following [Change StartMode of a Service](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell sample, pulled from TechNet Gallery, changes the start mode of a service.</span></span>


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
```



## <a name="requirements"></a><span data-ttu-id="933db-206">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="933db-206">Requirements</span></span>



| <span data-ttu-id="933db-207">Condition requise</span><span class="sxs-lookup"><span data-stu-id="933db-207">Requirement</span></span> | <span data-ttu-id="933db-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="933db-208">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="933db-209">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="933db-209">Minimum supported client</span></span><br/> | <span data-ttu-id="933db-210">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="933db-210">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="933db-211">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="933db-211">Minimum supported server</span></span><br/> | <span data-ttu-id="933db-212">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="933db-212">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="933db-213">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="933db-213">Namespace</span></span><br/>                | <span data-ttu-id="933db-214">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="933db-214">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="933db-215">MOF</span><span class="sxs-lookup"><span data-stu-id="933db-215">MOF</span></span><br/>                      | <dl> <span data-ttu-id="933db-216"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="933db-216"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="933db-217">DLL</span><span class="sxs-lookup"><span data-stu-id="933db-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="933db-218"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="933db-218"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933db-219">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="933db-219">See also</span></span>

<dl> <dt>

<span data-ttu-id="933db-220">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="933db-220">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="933db-221">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="933db-221">**Win32\_Service**</span></span>](win32-service.md)
</dt> <dt>

[<span data-ttu-id="933db-222">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="933db-222">WMI Tasks: Services</span></span>](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

