---
description: La table ServiceControl est utilisée pour contrôler les services installés ou désinstallés. Notez que les services qui s’appuient sur la présence d’un assembly dans le global assembly cache (GAC) ne peuvent pas être installés ou démarrés à l’aide des tables ServiceInstall et ServiceControl.
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Table ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757624"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="f0cc9-103">Table ServiceControl</span><span class="sxs-lookup"><span data-stu-id="f0cc9-103">ServiceControl Table</span></span>

<span data-ttu-id="f0cc9-104">La table ServiceControl est utilisée pour contrôler les services installés ou désinstallés.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="f0cc9-105">Les services qui s’appuient sur la présence d’un [assembly](assemblies.md) dans le global assembly cache (GAC) ne peuvent pas être installés ou démarrés à l’aide des tables [ServiceInstall](serviceinstall-table.md) et ServiceControl.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="f0cc9-106">Si vous avez besoin de démarrer un service qui dépend d’un assembly dans le GAC, vous devez utiliser une séquence d’action personnalisée après l' [action InstallFinalize](installfinalize-action.md) ou une [action personnalisée de validation](commit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="f0cc9-107">Pour plus d’informations sur l’installation d’assemblys dans le GAC, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="f0cc9-108">La table ServiceControl contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="f0cc9-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="f0cc9-109">Column</span></span>         | <span data-ttu-id="f0cc9-110">Type</span><span class="sxs-lookup"><span data-stu-id="f0cc9-110">Type</span></span>                         | <span data-ttu-id="f0cc9-111">Clé</span><span class="sxs-lookup"><span data-stu-id="f0cc9-111">Key</span></span> | <span data-ttu-id="f0cc9-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="f0cc9-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="f0cc9-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="f0cc9-113">ServiceControl</span></span> | [<span data-ttu-id="f0cc9-114">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f0cc9-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="f0cc9-115">O</span><span class="sxs-lookup"><span data-stu-id="f0cc9-115">Y</span></span>   | <span data-ttu-id="f0cc9-116">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-116">N</span></span>        |
| <span data-ttu-id="f0cc9-117">Nom</span><span class="sxs-lookup"><span data-stu-id="f0cc9-117">Name</span></span>           | [<span data-ttu-id="f0cc9-118">Correct</span><span class="sxs-lookup"><span data-stu-id="f0cc9-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f0cc9-119">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-119">N</span></span>   | <span data-ttu-id="f0cc9-120">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-120">N</span></span>        |
| <span data-ttu-id="f0cc9-121">Événement</span><span class="sxs-lookup"><span data-stu-id="f0cc9-121">Event</span></span>          | [<span data-ttu-id="f0cc9-122">Integer</span><span class="sxs-lookup"><span data-stu-id="f0cc9-122">Integer</span></span>](integer.md)       | <span data-ttu-id="f0cc9-123">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-123">N</span></span>   | <span data-ttu-id="f0cc9-124">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-124">N</span></span>        |
| <span data-ttu-id="f0cc9-125">Arguments</span><span class="sxs-lookup"><span data-stu-id="f0cc9-125">Arguments</span></span>      | [<span data-ttu-id="f0cc9-126">Correct</span><span class="sxs-lookup"><span data-stu-id="f0cc9-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="f0cc9-127">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-127">N</span></span>   | <span data-ttu-id="f0cc9-128">O</span><span class="sxs-lookup"><span data-stu-id="f0cc9-128">Y</span></span>        |
| <span data-ttu-id="f0cc9-129">Wait</span><span class="sxs-lookup"><span data-stu-id="f0cc9-129">Wait</span></span>           | [<span data-ttu-id="f0cc9-130">Integer</span><span class="sxs-lookup"><span data-stu-id="f0cc9-130">Integer</span></span>](integer.md)       | <span data-ttu-id="f0cc9-131">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-131">N</span></span>   | <span data-ttu-id="f0cc9-132">O</span><span class="sxs-lookup"><span data-stu-id="f0cc9-132">Y</span></span>        |
| <span data-ttu-id="f0cc9-133">-\_</span><span class="sxs-lookup"><span data-stu-id="f0cc9-133">Component\_</span></span>    | [<span data-ttu-id="f0cc9-134">Identificateur</span><span class="sxs-lookup"><span data-stu-id="f0cc9-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="f0cc9-135">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-135">N</span></span>   | <span data-ttu-id="f0cc9-136">N</span><span class="sxs-lookup"><span data-stu-id="f0cc9-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f0cc9-137">Colonnes</span><span class="sxs-lookup"><span data-stu-id="f0cc9-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f0cc9-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="f0cc9-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-139">Il s’agit de la clé primaire de cette table.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="f0cc9-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="f0cc9-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-141">Cette colonne est la chaîne qui nomme le service.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-141">This column is the string naming the service.</span></span> <span data-ttu-id="f0cc9-142">Cette colonne peut être utilisée pour contrôler un service qui n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="f0cc9-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement</span><span class="sxs-lookup"><span data-stu-id="f0cc9-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-144">Cette colonne contient les opérations à effectuer sur le service nommé.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="f0cc9-145">Notez que lors de l’arrêt d’un service, tous les services qui dépendent de ce service sont également arrêtés.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="f0cc9-146">Lors de la suppression d’un service en cours d’exécution, le programme d’installation arrête le service.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="f0cc9-147">Les valeurs de ce champ sont des champs de bits qui peuvent être combinés en une valeur unique qui représente plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="f0cc9-148">Les valeurs suivantes sont utilisées uniquement durant une installation.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="f0cc9-149">Constante</span><span class="sxs-lookup"><span data-stu-id="f0cc9-149">Constant</span></span>                           | <span data-ttu-id="f0cc9-150">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="f0cc9-150">Hexadecimal</span></span> | <span data-ttu-id="f0cc9-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="f0cc9-151">Decimal</span></span> | <span data-ttu-id="f0cc9-152">Description</span><span class="sxs-lookup"><span data-stu-id="f0cc9-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cc9-153">**msidbServiceControlEventStart**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="f0cc9-154">0x001</span><span class="sxs-lookup"><span data-stu-id="f0cc9-154">0x001</span></span>       | <span data-ttu-id="f0cc9-155">1</span><span class="sxs-lookup"><span data-stu-id="f0cc9-155">1</span></span>       | <span data-ttu-id="f0cc9-156">Démarre le service pendant l' [action StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="f0cc9-157">**msidbServiceControlEventStop**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="f0cc9-158">0x002</span><span class="sxs-lookup"><span data-stu-id="f0cc9-158">0x002</span></span>       | <span data-ttu-id="f0cc9-159">2</span><span class="sxs-lookup"><span data-stu-id="f0cc9-159">2</span></span>       | <span data-ttu-id="f0cc9-160">Arrête le service pendant l' [action StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="f0cc9-161">(aucun)</span><span class="sxs-lookup"><span data-stu-id="f0cc9-161">(none)</span></span>                             | <span data-ttu-id="f0cc9-162">0x004</span><span class="sxs-lookup"><span data-stu-id="f0cc9-162">0x004</span></span>       | <span data-ttu-id="f0cc9-163">4</span><span class="sxs-lookup"><span data-stu-id="f0cc9-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="f0cc9-164">**msidbServiceControlEventDelete**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="f0cc9-165">0x008</span><span class="sxs-lookup"><span data-stu-id="f0cc9-165">0x008</span></span>       | <span data-ttu-id="f0cc9-166">8</span><span class="sxs-lookup"><span data-stu-id="f0cc9-166">8</span></span>       | <span data-ttu-id="f0cc9-167">Supprime le service pendant l' [action DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="f0cc9-168">Les valeurs suivantes sont utilisées uniquement pendant une désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="f0cc9-169">Constante</span><span class="sxs-lookup"><span data-stu-id="f0cc9-169">Constant</span></span>                                    | <span data-ttu-id="f0cc9-170">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="f0cc9-170">Hexadecimal</span></span> | <span data-ttu-id="f0cc9-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="f0cc9-171">Decimal</span></span> | <span data-ttu-id="f0cc9-172">Description</span><span class="sxs-lookup"><span data-stu-id="f0cc9-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cc9-173">**msidbServiceControlEventUninstallStart**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="f0cc9-174">0x010</span><span class="sxs-lookup"><span data-stu-id="f0cc9-174">0x010</span></span>       | <span data-ttu-id="f0cc9-175">16</span><span class="sxs-lookup"><span data-stu-id="f0cc9-175">16</span></span>      | <span data-ttu-id="f0cc9-176">Démarre le service pendant l' [action StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="f0cc9-177">**msidbServiceControlEventUninstallStop**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="f0cc9-178">0x020</span><span class="sxs-lookup"><span data-stu-id="f0cc9-178">0x020</span></span>       | <span data-ttu-id="f0cc9-179">32</span><span class="sxs-lookup"><span data-stu-id="f0cc9-179">32</span></span>      | <span data-ttu-id="f0cc9-180">Arrête le service pendant l' [action StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="f0cc9-181">(aucun)</span><span class="sxs-lookup"><span data-stu-id="f0cc9-181">(none)</span></span>                                      | <span data-ttu-id="f0cc9-182">0x040</span><span class="sxs-lookup"><span data-stu-id="f0cc9-182">0x040</span></span>       | <span data-ttu-id="f0cc9-183">64</span><span class="sxs-lookup"><span data-stu-id="f0cc9-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="f0cc9-184">**msidbServiceControlEventUninstallDelete**</span><span class="sxs-lookup"><span data-stu-id="f0cc9-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="f0cc9-185">0x080</span><span class="sxs-lookup"><span data-stu-id="f0cc9-185">0x080</span></span>       | <span data-ttu-id="f0cc9-186">128</span><span class="sxs-lookup"><span data-stu-id="f0cc9-186">128</span></span>     | <span data-ttu-id="f0cc9-187">Supprime le service pendant l' [action DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="f0cc9-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span><span class="sxs-lookup"><span data-stu-id="f0cc9-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-189">Liste d’arguments pour démarrer les services.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-189">A list of arguments for starting services.</span></span> <span data-ttu-id="f0cc9-190">Les arguments sont séparés par des caractères null \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="f0cc9-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="f0cc9-191">Par exemple, la liste des arguments un, deux et trois sont répertoriées comme suit : un \[ ~ \] deux \[ ~ \] trois.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="f0cc9-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Qu'</span><span class="sxs-lookup"><span data-stu-id="f0cc9-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-193">Si vous laissez ce champ null ou si vous entrez une valeur de 1, le programme d’installation attend un maximum de 30 secondes avant que le service ne se termine.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="f0cc9-194">L’attente peut être utilisée pour permettre à un événement critique de renvoyer une erreur d’échec.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="f0cc9-195">La valeur 0 dans ce champ signifie d’attendre uniquement jusqu’à ce que le gestionnaire de contrôle des services (SCM) signale que ce service est en état d’attente avant de poursuivre l’installation.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="f0cc9-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="f0cc9-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f0cc9-197">Clé externe vers la colonne de l’une des [tables de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0cc9-198">Notes</span><span class="sxs-lookup"><span data-stu-id="f0cc9-198">Remarks</span></span>

<span data-ttu-id="f0cc9-199">Les actions [StartServices](startservices-action.md), [StopServices](stopservices-action.md)et [DeleteServices](deleteservices-action.md) dans les [*tables de séquences*](s-gly.md) traitent les informations contenues dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="f0cc9-200">Pour plus d’informations sur l’utilisation des *tables de séquences*, consultez [utilisation d’une table de séquences](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc9-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="f0cc9-201">Utilisez la colonne nom pour démarrer, arrêter ou supprimer des services qui sont remplacés par l’installation ou qui dépendent d’un nouveau service en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="f0cc9-202">Par exemple, l’entrée de MyService dans la colonne ServiceControl peut lier ce service à MyComponent dans la \_ colonne Component.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="f0cc9-203">Si le champ de bits de la colonne d’événement est défini pour démarrer lors de l’installation de, le programme d’installation démarre MyService lors de l’installation de MonComposant.</span><span class="sxs-lookup"><span data-stu-id="f0cc9-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="f0cc9-204">Validation</span><span class="sxs-lookup"><span data-stu-id="f0cc9-204">Validation</span></span>

<dl>

[<span data-ttu-id="f0cc9-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="f0cc9-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f0cc9-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="f0cc9-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f0cc9-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="f0cc9-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f0cc9-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="f0cc9-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="f0cc9-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="f0cc9-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="f0cc9-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="f0cc9-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



