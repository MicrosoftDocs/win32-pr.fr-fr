---
description: La table MsiServiceConfig configure un service qui est installé ou en cours d’installation par le package actuel.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Table MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522149"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="f31a7-103">Table MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f31a7-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="f31a7-104">La table MsiServiceConfig configure un service qui est installé ou en cours d’installation par le package actuel.</span><span class="sxs-lookup"><span data-stu-id="f31a7-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="f31a7-105">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f31a7-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="f31a7-106">Cette table est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="f31a7-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="f31a7-107">La table MsiServiceConfig contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f31a7-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="f31a7-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="f31a7-108">Column</span></span>           | <span data-ttu-id="f31a7-109">Type</span><span class="sxs-lookup"><span data-stu-id="f31a7-109">Type</span></span>                         | <span data-ttu-id="f31a7-110">Clé</span><span class="sxs-lookup"><span data-stu-id="f31a7-110">Key</span></span> | <span data-ttu-id="f31a7-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="f31a7-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="f31a7-112">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f31a7-112">MsiServiceConfig</span></span> | [<span data-ttu-id="f31a7-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f31a7-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="f31a7-114">O</span><span class="sxs-lookup"><span data-stu-id="f31a7-114">Y</span></span>   | <span data-ttu-id="f31a7-115">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-115">N</span></span>        |
| <span data-ttu-id="f31a7-116">Nom</span><span class="sxs-lookup"><span data-stu-id="f31a7-116">Name</span></span>             | [<span data-ttu-id="f31a7-117">Correct</span><span class="sxs-lookup"><span data-stu-id="f31a7-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f31a7-118">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-118">N</span></span>   | <span data-ttu-id="f31a7-119">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-119">N</span></span>        |
| <span data-ttu-id="f31a7-120">Événement</span><span class="sxs-lookup"><span data-stu-id="f31a7-120">Event</span></span>            | [<span data-ttu-id="f31a7-121">Integer</span><span class="sxs-lookup"><span data-stu-id="f31a7-121">Integer</span></span>](integer.md)       | <span data-ttu-id="f31a7-122">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-122">N</span></span>   | <span data-ttu-id="f31a7-123">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-123">N</span></span>        |
| <span data-ttu-id="f31a7-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="f31a7-124">ConfigType</span></span>       | [<span data-ttu-id="f31a7-125">Integer</span><span class="sxs-lookup"><span data-stu-id="f31a7-125">Integer</span></span>](integer.md)       | <span data-ttu-id="f31a7-126">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-126">N</span></span>   | <span data-ttu-id="f31a7-127">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-127">N</span></span>        |
| <span data-ttu-id="f31a7-128">Argument</span><span class="sxs-lookup"><span data-stu-id="f31a7-128">Argument</span></span>         | [<span data-ttu-id="f31a7-129">Correct</span><span class="sxs-lookup"><span data-stu-id="f31a7-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f31a7-130">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-130">N</span></span>   | <span data-ttu-id="f31a7-131">O</span><span class="sxs-lookup"><span data-stu-id="f31a7-131">Y</span></span>        |
| <span data-ttu-id="f31a7-132">-\_</span><span class="sxs-lookup"><span data-stu-id="f31a7-132">Component\_</span></span>      | [<span data-ttu-id="f31a7-133">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f31a7-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="f31a7-134">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-134">N</span></span>   | <span data-ttu-id="f31a7-135">N</span><span class="sxs-lookup"><span data-stu-id="f31a7-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f31a7-136">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f31a7-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f31a7-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="f31a7-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-138">Il s’agit de la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="f31a7-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="f31a7-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="f31a7-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-140">Cette colonne contient le nom d’un service qui fait partie de ce package ou qui est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="f31a7-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="f31a7-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement</span><span class="sxs-lookup"><span data-stu-id="f31a7-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-142">Cette colonne spécifie quand modifier la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="f31a7-143">Les valeurs suivantes peuvent être combinées pour représenter plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="f31a7-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="f31a7-144">Toutes les valeurs incluses en dehors de celles-ci sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="f31a7-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="f31a7-145">Constante</span><span class="sxs-lookup"><span data-stu-id="f31a7-145">Constant</span></span>                                         | <span data-ttu-id="f31a7-146">Description</span><span class="sxs-lookup"><span data-stu-id="f31a7-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="f31a7-147">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="f31a7-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="f31a7-148">Exécute l’action lors de l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="f31a7-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="f31a7-149">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="f31a7-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="f31a7-150">Exécute l’action pendant la désinstallation du composant.</span><span class="sxs-lookup"><span data-stu-id="f31a7-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="f31a7-151">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="f31a7-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="f31a7-152">Effectue l’action lors de la réinstallation du composant.</span><span class="sxs-lookup"><span data-stu-id="f31a7-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f31a7-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="f31a7-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-154">La valeur de ce champ, associée à la valeur dans le champ arguments, spécifie la modification à apporter à la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="f31a7-155">La modification spécifiée prend effet lors du prochain démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="f31a7-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="f31a7-156">Config</span><span class="sxs-lookup"><span data-stu-id="f31a7-156">Config</span></span>                                                      | <span data-ttu-id="f31a7-157">Description</span><span class="sxs-lookup"><span data-stu-id="f31a7-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f31a7-158">**Service \_ \_ \_ \_ Démarrage automatique différé** de la configuration 3</span><span class="sxs-lookup"><span data-stu-id="f31a7-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="f31a7-159">Configurez le délai d’un [service à démarrage automatique](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="f31a7-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="f31a7-160">Entrez 1 dans le champ argument pour démarrer le service après d’autres services à démarrage automatique plus un délai.</span><span class="sxs-lookup"><span data-stu-id="f31a7-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="f31a7-161">Entrez 0 dans le champ argument pour désactiver le délai de service de démarrage automatique.</span><span class="sxs-lookup"><span data-stu-id="f31a7-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="f31a7-162">S’applique uniquement aux services ou services à démarrage automatique installés par ce package avec **le \_ \_ démarrage automatique du service** dans le champ StartType de la [table ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="f31a7-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="f31a7-163">**Service \_ \_ \_ \_ Informations sur les privilèges requis** pour la configuration 6</span><span class="sxs-lookup"><span data-stu-id="f31a7-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="f31a7-164">Modifiez la liste des privilèges requis par le service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="f31a7-165">Entrez la liste des privilèges demandés dans le champ argument.</span><span class="sxs-lookup"><span data-stu-id="f31a7-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="f31a7-166">La valeur de chaîne [mise en forme](formatted.md) dans le champ argument répertorie les [**constantes de privilège**](../secauthz/privilege-constants.md) pour les privilèges demandés.</span><span class="sxs-lookup"><span data-stu-id="f31a7-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="f31a7-167">Vous pouvez utiliser la \[ ~ \] syntaxe de la chaîne [mise en forme](formatted.md) pour insérer un caractère null.</span><span class="sxs-lookup"><span data-stu-id="f31a7-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="f31a7-168">Séparez les constantes de privilège de la liste par \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="f31a7-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="f31a7-169">**Service \_ \_ \_ \_ Informations sid** 5 du service de configuration</span><span class="sxs-lookup"><span data-stu-id="f31a7-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="f31a7-170">Ajoutez un type de SID de service au jeton de processus contenant ce service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="f31a7-171">Entrez dans le champ argument un type de SID de service valide pour la structure d' [**\_ \_ informations SID du service**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : **type de SID de service \_ \_ \_ None** (0x00), type de SID de service (0x03) ou type de **\_ SID de \_ \_ service** **\_ \_ \_ illimité** (0x01).</span><span class="sxs-lookup"><span data-stu-id="f31a7-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="f31a7-172">**Service \_ \_ \_ Informations de préfermeture de configuration** 7</span><span class="sxs-lookup"><span data-stu-id="f31a7-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="f31a7-173">Configurez la durée d’attente du [Gestionnaire de contrôle des services](../services/service-control-manager.md) (SCM) avant de procéder à d’autres opérations d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f31a7-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="f31a7-174">Le SCM attend pendant ce laps de temps après l’envoi de la notification de préversion de **\_ \_ contrôle de service** au service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="f31a7-175">Entrez la durée, en millisecondes, dans le champ argument.</span><span class="sxs-lookup"><span data-stu-id="f31a7-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="f31a7-176">Laissez le champ argument vide pour réinitialiser le délai à la valeur par défaut de 3 minutes.</span><span class="sxs-lookup"><span data-stu-id="f31a7-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="f31a7-177">**Service \_ \_Indicateur des \_ actions \_ d’échec** de la configuration 4</span><span class="sxs-lookup"><span data-stu-id="f31a7-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="f31a7-178">Configurez à quel moment exécuter les actions d’échec pour ce service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="f31a7-179">Ce paramètre est ignoré si le service n’a pas d’action d’échec configurée.</span><span class="sxs-lookup"><span data-stu-id="f31a7-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="f31a7-180">Entrez 0 pour exécuter les actions uniquement si le service se termine sans que Reporting **service soit \_ arrêté**.</span><span class="sxs-lookup"><span data-stu-id="f31a7-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="f31a7-181">Entrez 1 pour exécuter les actions si le service arrête le service de création de rapports et que le membre **dwWin32ExitCode** de la structure d' [**\_ État du service**](/windows/win32/api/winsvc/ns-winsvc-service_status) n’est pas une erreur de **\_ réussite**. **\_**</span><span class="sxs-lookup"><span data-stu-id="f31a7-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="f31a7-182">Les actions configurées en cas d’échec sont également exécutées si le service se termine sans que Reporting **services soit \_ arrêté**.</span><span class="sxs-lookup"><span data-stu-id="f31a7-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f31a7-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="f31a7-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-184">La valeur de ce champ, associée à la valeur dans le champ ConfigType, spécifiez la modification à apporter à la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="f31a7-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="f31a7-185">La modification spécifiée prend effet lors du prochain démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="f31a7-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="f31a7-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="f31a7-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f31a7-187">Clé externe de la colonne de composant de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f31a7-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="f31a7-188">Validation</span><span class="sxs-lookup"><span data-stu-id="f31a7-188">Validation</span></span>

<dl>

[<span data-ttu-id="f31a7-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="f31a7-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="f31a7-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="f31a7-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f31a7-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="f31a7-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f31a7-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="f31a7-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f31a7-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="f31a7-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="f31a7-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="f31a7-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="f31a7-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="f31a7-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
