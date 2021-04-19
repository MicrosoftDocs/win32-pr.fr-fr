---
description: La table MsiServiceConfigFailureActions répertorie les opérations à exécuter après l’échec d’un service. Les opérations spécifiées dans ce tableau s’exécutent lors du prochain démarrage du système.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Table MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524374"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="a0042-104">Table MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a0042-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="a0042-105">La table MsiServiceConfigFailureActions répertorie les opérations à exécuter après l’échec d’un service.</span><span class="sxs-lookup"><span data-stu-id="a0042-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="a0042-106">Les opérations spécifiées dans ce tableau s’exécutent lors du prochain démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a0042-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="a0042-107">**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a0042-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="a0042-108">Cette table est disponible à partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="a0042-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="a0042-109">La table MsiServiceConfigFailureActions contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0042-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="a0042-110">Colonne</span><span class="sxs-lookup"><span data-stu-id="a0042-110">Column</span></span>                         | <span data-ttu-id="a0042-111">Type</span><span class="sxs-lookup"><span data-stu-id="a0042-111">Type</span></span>                         | <span data-ttu-id="a0042-112">Clé</span><span class="sxs-lookup"><span data-stu-id="a0042-112">Key</span></span> | <span data-ttu-id="a0042-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="a0042-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="a0042-114">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a0042-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="a0042-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a0042-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="a0042-116">O</span><span class="sxs-lookup"><span data-stu-id="a0042-116">Y</span></span>   | <span data-ttu-id="a0042-117">N</span><span class="sxs-lookup"><span data-stu-id="a0042-117">N</span></span>        |
| <span data-ttu-id="a0042-118">Nom</span><span class="sxs-lookup"><span data-stu-id="a0042-118">Name</span></span>                           | [<span data-ttu-id="a0042-119">Correct</span><span class="sxs-lookup"><span data-stu-id="a0042-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a0042-120">N</span><span class="sxs-lookup"><span data-stu-id="a0042-120">N</span></span>   | <span data-ttu-id="a0042-121">N</span><span class="sxs-lookup"><span data-stu-id="a0042-121">N</span></span>        |
| <span data-ttu-id="a0042-122">Événement</span><span class="sxs-lookup"><span data-stu-id="a0042-122">Event</span></span>                          | [<span data-ttu-id="a0042-123">Integer</span><span class="sxs-lookup"><span data-stu-id="a0042-123">Integer</span></span>](integer.md)       | <span data-ttu-id="a0042-124">N</span><span class="sxs-lookup"><span data-stu-id="a0042-124">N</span></span>   | <span data-ttu-id="a0042-125">N</span><span class="sxs-lookup"><span data-stu-id="a0042-125">N</span></span>        |
| <span data-ttu-id="a0042-126">ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="a0042-126">ResetPeriod</span></span>                    | [<span data-ttu-id="a0042-127">Integer</span><span class="sxs-lookup"><span data-stu-id="a0042-127">Integer</span></span>](integer.md)       | <span data-ttu-id="a0042-128">N</span><span class="sxs-lookup"><span data-stu-id="a0042-128">N</span></span>   | <span data-ttu-id="a0042-129">O</span><span class="sxs-lookup"><span data-stu-id="a0042-129">Y</span></span>        |
| <span data-ttu-id="a0042-130">RebootMessage</span><span class="sxs-lookup"><span data-stu-id="a0042-130">RebootMessage</span></span>                  | [<span data-ttu-id="a0042-131">Correct</span><span class="sxs-lookup"><span data-stu-id="a0042-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a0042-132">N</span><span class="sxs-lookup"><span data-stu-id="a0042-132">N</span></span>   | <span data-ttu-id="a0042-133">Y</span><span class="sxs-lookup"><span data-stu-id="a0042-133">Y</span></span>        |
| <span data-ttu-id="a0042-134">Commande</span><span class="sxs-lookup"><span data-stu-id="a0042-134">Command</span></span>                        | [<span data-ttu-id="a0042-135">Correct</span><span class="sxs-lookup"><span data-stu-id="a0042-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="a0042-136">N</span><span class="sxs-lookup"><span data-stu-id="a0042-136">N</span></span>   | <span data-ttu-id="a0042-137">O</span><span class="sxs-lookup"><span data-stu-id="a0042-137">Y</span></span>        |
| <span data-ttu-id="a0042-138">Actions</span><span class="sxs-lookup"><span data-stu-id="a0042-138">Actions</span></span>                        | [<span data-ttu-id="a0042-139">Text</span><span class="sxs-lookup"><span data-stu-id="a0042-139">Text</span></span>](text.md)             | <span data-ttu-id="a0042-140">N</span><span class="sxs-lookup"><span data-stu-id="a0042-140">N</span></span>   | <span data-ttu-id="a0042-141">O</span><span class="sxs-lookup"><span data-stu-id="a0042-141">Y</span></span>        |
| <span data-ttu-id="a0042-142">DelayActions</span><span class="sxs-lookup"><span data-stu-id="a0042-142">DelayActions</span></span>                   | [<span data-ttu-id="a0042-143">Text</span><span class="sxs-lookup"><span data-stu-id="a0042-143">Text</span></span>](text.md)             | <span data-ttu-id="a0042-144">N</span><span class="sxs-lookup"><span data-stu-id="a0042-144">N</span></span>   | <span data-ttu-id="a0042-145">O</span><span class="sxs-lookup"><span data-stu-id="a0042-145">Y</span></span>        |
| <span data-ttu-id="a0042-146">-\_</span><span class="sxs-lookup"><span data-stu-id="a0042-146">Component\_</span></span>                    | [<span data-ttu-id="a0042-147">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a0042-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="a0042-148">N</span><span class="sxs-lookup"><span data-stu-id="a0042-148">N</span></span>   | <span data-ttu-id="a0042-149">N</span><span class="sxs-lookup"><span data-stu-id="a0042-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a0042-150">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a0042-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a0042-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="a0042-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="a0042-152">Il s’agit de la clé primaire de cette table qui identifie une action d’échec.</span><span class="sxs-lookup"><span data-stu-id="a0042-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="a0042-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a0042-154">Cette colonne contient le nom d’un service qui fait partie de ce package ou qui est déjà installé.</span><span class="sxs-lookup"><span data-stu-id="a0042-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement</span><span class="sxs-lookup"><span data-stu-id="a0042-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="a0042-156">Cette colonne spécifie quand modifier la configuration du service.</span><span class="sxs-lookup"><span data-stu-id="a0042-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="a0042-157">Les valeurs suivantes sont des champs de bits qui peuvent être combinés pour représenter plusieurs opérations.</span><span class="sxs-lookup"><span data-stu-id="a0042-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="a0042-158">Toutes les autres valeurs de champ de bits sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="a0042-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="a0042-159">Constante</span><span class="sxs-lookup"><span data-stu-id="a0042-159">Constant</span></span>                                         | <span data-ttu-id="a0042-160">Description</span><span class="sxs-lookup"><span data-stu-id="a0042-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="a0042-161">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="a0042-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="a0042-162">Modification au cours de l’installation du composant.</span><span class="sxs-lookup"><span data-stu-id="a0042-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="a0042-163">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="a0042-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="a0042-164">Modification au cours de la désinstallation du composant.</span><span class="sxs-lookup"><span data-stu-id="a0042-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="a0042-165">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="a0042-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="a0042-166">Modification lors de la réinstallation du composant.</span><span class="sxs-lookup"><span data-stu-id="a0042-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a0042-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="a0042-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="a0042-168">Période de réinitialisation en secondes du nombre d’échecs du service.</span><span class="sxs-lookup"><span data-stu-id="a0042-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="a0042-169">Le [Gestionnaire de contrôle des services](../services/service-control-manager.md) (SCM) compte le nombre de fois où chaque service a échoué depuis le dernier redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="a0042-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="a0042-170">Le nombre est réinitialisé à zéro si le service n’échoue pas pendant la période de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="a0042-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="a0042-171">Lorsque le service échoue pour la nième fois, le système effectue l’action spécifiée dans l’élément \[ N-1 \] du tableau spécifié dans le champ actions.</span><span class="sxs-lookup"><span data-stu-id="a0042-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="a0042-172">Laissez le champ ResetPeriod vide pour indiquer que le nombre d’échecs ne doit jamais être réinitialisé.</span><span class="sxs-lookup"><span data-stu-id="a0042-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span><span class="sxs-lookup"><span data-stu-id="a0042-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="a0042-174">Message envoyé aux utilisateurs avant le redémarrage de l’ordinateur en réponse à une action de **\_ \_ redémarrage de l’action SC** spécifiée dans la colonne actions.</span><span class="sxs-lookup"><span data-stu-id="a0042-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="a0042-175">Vous pouvez utiliser une chaîne vide, "", pour envoyer le message actuel inchangé.</span><span class="sxs-lookup"><span data-stu-id="a0042-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="a0042-176">Vous pouvez utiliser \[ ~ \] la syntaxe du type de données [mis en forme](formatted.md) pour supprimer le message en cours et envoyer aucun message.</span><span class="sxs-lookup"><span data-stu-id="a0042-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Commande</span><span class="sxs-lookup"><span data-stu-id="a0042-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="a0042-178">La ligne de commande exécutée par le processus créé par la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en réponse à une action de **\_ commande sc action \_ Run \_** spécifiée dans la colonne actions.</span><span class="sxs-lookup"><span data-stu-id="a0042-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="a0042-179">Le nouveau processus s’exécute sous le même compte que le service et uniquement si le champ d’action est **\_ \_ \_ commande sc action Run**.</span><span class="sxs-lookup"><span data-stu-id="a0042-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="a0042-180">Vous pouvez utiliser une chaîne vide, "", pour utiliser la ligne de commande actuelle inchangée.</span><span class="sxs-lookup"><span data-stu-id="a0042-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="a0042-181">Vous pouvez utiliser \[ ~ \] la syntaxe du type de données [mis en forme](formatted.md) pour supprimer la ligne de commande actuelle et ne pas exécuter d’opération en cas d’échec du service.</span><span class="sxs-lookup"><span data-stu-id="a0042-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Interventions</span><span class="sxs-lookup"><span data-stu-id="a0042-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="a0042-183">Ce champ contient un tableau de valeurs entières qui spécifient les actions effectuées par le SCM en cas d’échec du service.</span><span class="sxs-lookup"><span data-stu-id="a0042-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="a0042-184">Séparez les valeurs dans le tableau par \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="a0042-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="a0042-185">La valeur entière dans le nième élément du tableau spécifie l’action exécutée lorsque le service échoue pour la nième heure.</span><span class="sxs-lookup"><span data-stu-id="a0042-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="a0042-186">Chaque membre du tableau est l’une des valeurs entières suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0042-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="a0042-187">Constante</span><span class="sxs-lookup"><span data-stu-id="a0042-187">Constant</span></span>                                 | <span data-ttu-id="a0042-188">Description</span><span class="sxs-lookup"><span data-stu-id="a0042-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="a0042-189">**SC \_ ACTION \_ None** 0</span><span class="sxs-lookup"><span data-stu-id="a0042-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="a0042-190">Aucune action.</span><span class="sxs-lookup"><span data-stu-id="a0042-190">No action.</span></span>            |
| <span data-ttu-id="a0042-191">**SC \_ ACTION de \_ redémarrage** 2</span><span class="sxs-lookup"><span data-stu-id="a0042-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="a0042-192">Redémarrez l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a0042-192">Restart the computer.</span></span> |
| <span data-ttu-id="a0042-193">**SC \_ ACTION \_ restart** 1</span><span class="sxs-lookup"><span data-stu-id="a0042-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="a0042-194">Redémarrez le service.</span><span class="sxs-lookup"><span data-stu-id="a0042-194">Restart the service.</span></span>  |
| <span data-ttu-id="a0042-195">**SC \_ ACTION \_ exécuter la \_ commande** 3</span><span class="sxs-lookup"><span data-stu-id="a0042-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="a0042-196">Exécutez une commande.</span><span class="sxs-lookup"><span data-stu-id="a0042-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="a0042-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span><span class="sxs-lookup"><span data-stu-id="a0042-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="a0042-198">Ce champ contient un tableau de valeurs entières qui spécifient le délai d’attente, en millisecondes, avant l’exécution de l’action spécifiée dans la colonne action.</span><span class="sxs-lookup"><span data-stu-id="a0042-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="a0042-199">Séparez les valeurs dans le tableau par \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="a0042-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="a0042-200">Le nombre d’éléments dans le tableau DelayActions doit être égal au nombre d’éléments dans le tableau d’actions.</span><span class="sxs-lookup"><span data-stu-id="a0042-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="a0042-201">Le nième élément du tableau DelayActions spécifie le délai d’exécution du nième élément du tableau d’actions.</span><span class="sxs-lookup"><span data-stu-id="a0042-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="a0042-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="a0042-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a0042-203">Clé externe vers la colonne de l’une des [tables de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="a0042-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="a0042-204">Validation</span><span class="sxs-lookup"><span data-stu-id="a0042-204">Validation</span></span>

<dl>

[<span data-ttu-id="a0042-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="a0042-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="a0042-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="a0042-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a0042-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="a0042-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a0042-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="a0042-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a0042-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="a0042-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="a0042-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="a0042-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="a0042-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="a0042-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
