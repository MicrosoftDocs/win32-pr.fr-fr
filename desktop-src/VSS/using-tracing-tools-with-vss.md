---
description: Pour collecter des informations de suivi pour l’infrastructure VSS, vous pouvez utiliser l’outil VssTrace, logman ou l’outil tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Utilisation des outils de suivi avec VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201458"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="52ab6-103">Utilisation des outils de suivi avec VSS</span><span class="sxs-lookup"><span data-stu-id="52ab6-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="52ab6-104">Pour collecter des informations de suivi pour l’infrastructure VSS, vous pouvez utiliser l’outil VssTrace, logman ou l’outil tracelog.</span><span class="sxs-lookup"><span data-stu-id="52ab6-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="52ab6-105">VssTrace est disponible dans le kit de développement logiciel (SDK) Microsoft Windows et peut être utilisé pour suivre des applications VSS sur Windows 7 et les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="52ab6-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="52ab6-106">Logman est un contrôleur de trace pour les événements de trace et les compteurs de performance. Il peut également être utilisé pour effectuer le suivi des applications VSS sur Windows 7 et les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="52ab6-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="52ab6-107">Tracelog est inclus dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="52ab6-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="52ab6-108">Pour utiliser les outils de suivi avec la [récupération automatique du système (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), consultez [utilisation des outils de suivi avec les applications ASR](using-tracing-tools-with-vss-asr-applications.md).</span><span class="sxs-lookup"><span data-stu-id="52ab6-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="52ab6-109">VssTrace, logman et tracelog requièrent tous des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="52ab6-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="52ab6-110">Pour plus d’informations sur chaque outil, consultez les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="52ab6-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="52ab6-111">Utilisation de VssTrace</span><span class="sxs-lookup"><span data-stu-id="52ab6-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="52ab6-112">Options de Command-Line VssTrace</span><span class="sxs-lookup"><span data-stu-id="52ab6-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="52ab6-113">Utilisation de logman</span><span class="sxs-lookup"><span data-stu-id="52ab6-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="52ab6-114">Utilisation de tracelog</span><span class="sxs-lookup"><span data-stu-id="52ab6-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="52ab6-115">Utilisation de VssTrace</span><span class="sxs-lookup"><span data-stu-id="52ab6-115">Using VssTrace</span></span>

<span data-ttu-id="52ab6-116">Pour exécuter l’outil VssTrace à partir de la ligne de commande, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="52ab6-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="52ab6-117"> *options de ligne de commande* vsstrace</span><span class="sxs-lookup"><span data-stu-id="52ab6-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="52ab6-118">Pour afficher une aide concise sur la ligne de commande pour l’outil VssTrace, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="52ab6-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="52ab6-119">**vsstrace-aide**</span><span class="sxs-lookup"><span data-stu-id="52ab6-119">**vsstrace -help**</span></span>

<span data-ttu-id="52ab6-120">Pour afficher une aide détaillée sur la ligne de commande de l’outil VssTrace, utilisez la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="52ab6-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="52ab6-121">**vsstrace-help all**</span><span class="sxs-lookup"><span data-stu-id="52ab6-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="52ab6-122">Options de Command-Line VssTrace</span><span class="sxs-lookup"><span data-stu-id="52ab6-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="52ab6-123">L’outil VssTrace utilise les options de ligne de commande suivantes :</span><span class="sxs-lookup"><span data-stu-id="52ab6-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="52ab6-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f (** *indicateurs* )</span><span class="sxs-lookup"><span data-stu-id="52ab6-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-125">Activez les modules dont les indicateurs sont spécifiés par le masque de masque des *indicateurs* .</span><span class="sxs-lookup"><span data-stu-id="52ab6-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="52ab6-126">Chaque indicateur correspond à un module VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="52ab6-127">Si *Flags* est égal à zéro, aucun module n’est activé.</span><span class="sxs-lookup"><span data-stu-id="52ab6-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="52ab6-128">Notez que la plupart des modules sont activés par défaut.</span><span class="sxs-lookup"><span data-stu-id="52ab6-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="52ab6-129">Cette option peut être combinée avec l' **+** option _module_ .</span><span class="sxs-lookup"><span data-stu-id="52ab6-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="52ab6-130">Par exemple, **vsstrace-f 0 + Writer + Coord** désactive le suivi de tous les modules qui sont activés par défaut et active le suivi des enregistreurs VSS et du service VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="52ab6-131">Sinon, **vsstrace + f 0xFFFF-Coord** active le suivi de tous les modules à l’exception du service VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="52ab6-132">Si vous utilisez l’option **-f** avec l’option **+** _module_ , le **-f** doit apparaître avant l’option **+** _module_ .</span><span class="sxs-lookup"><span data-stu-id="52ab6-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="52ab6-133">Le tableau suivant répertorie le nom et l’indicateur du module pour chaque module disponible.</span><span class="sxs-lookup"><span data-stu-id="52ab6-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="52ab6-134">Module</span><span class="sxs-lookup"><span data-stu-id="52ab6-134">Module</span></span> | <span data-ttu-id="52ab6-135">Indicateur</span><span class="sxs-lookup"><span data-stu-id="52ab6-135">Flag</span></span>       | <span data-ttu-id="52ab6-136">Activée par défaut</span><span class="sxs-lookup"><span data-stu-id="52ab6-136">Enabled by default</span></span> | <span data-ttu-id="52ab6-137">Éléments suivis</span><span class="sxs-lookup"><span data-stu-id="52ab6-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ab6-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="52ab6-138">EXCEPT</span></span> | <span data-ttu-id="52ab6-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="52ab6-139">0x00000001</span></span> | <span data-ttu-id="52ab6-140">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-140">Yes</span></span>                | <span data-ttu-id="52ab6-141">Gestion des exceptions C++.</span><span class="sxs-lookup"><span data-stu-id="52ab6-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="52ab6-142">COORDONNÉES</span><span class="sxs-lookup"><span data-stu-id="52ab6-142">COORD</span></span>  | <span data-ttu-id="52ab6-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="52ab6-143">0x00000002</span></span> | <span data-ttu-id="52ab6-144">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-144">Yes</span></span>                | <span data-ttu-id="52ab6-145">Le service VSS, également appelé coordinateur VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="52ab6-146">SWPRV</span><span class="sxs-lookup"><span data-stu-id="52ab6-146">SWPRV</span></span>  | <span data-ttu-id="52ab6-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="52ab6-147">0x00000004</span></span> | <span data-ttu-id="52ab6-148">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-148">Yes</span></span>                | <span data-ttu-id="52ab6-149">Service du fournisseur de clichés instantanés du système VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="52ab6-150">BUCOMP</span><span class="sxs-lookup"><span data-stu-id="52ab6-150">BUCOMP</span></span> | <span data-ttu-id="52ab6-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="52ab6-151">0x00000008</span></span> | <span data-ttu-id="52ab6-152">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-152">Yes</span></span>                | <span data-ttu-id="52ab6-153">Le demandeur VSS et le traitement des métadonnées de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="52ab6-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="52ab6-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="52ab6-154">WRITER</span></span> | <span data-ttu-id="52ab6-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="52ab6-155">0x00000010</span></span> | <span data-ttu-id="52ab6-156">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-156">Yes</span></span>                | <span data-ttu-id="52ab6-157">Les opérations de l’enregistreur VSS et les implémentations du writer hébergé VSS, telles que l’enregistreur du Registre Windows.</span><span class="sxs-lookup"><span data-stu-id="52ab6-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="52ab6-158">VSSAPI</span><span class="sxs-lookup"><span data-stu-id="52ab6-158">VSSAPI</span></span> | <span data-ttu-id="52ab6-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="52ab6-159">0x00000020</span></span> | <span data-ttu-id="52ab6-160">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-160">Yes</span></span>                | <span data-ttu-id="52ab6-161">Fonctions diverses de l’API VSS exportées par VSSAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="52ab6-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="52ab6-162">HWDIAG</span><span class="sxs-lookup"><span data-stu-id="52ab6-162">HWDIAG</span></span> | <span data-ttu-id="52ab6-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="52ab6-163">0x00000040</span></span> | <span data-ttu-id="52ab6-164">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-164">Yes</span></span>                | <span data-ttu-id="52ab6-165">L’infrastructure et les opérations du fournisseur de matériel VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="52ab6-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="52ab6-166">ADMIN</span></span>  | <span data-ttu-id="52ab6-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="52ab6-167">0x00000080</span></span> | <span data-ttu-id="52ab6-168">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-168">Yes</span></span>                | <span data-ttu-id="52ab6-169">Les utilitaires de ligne de commande VSS tels que VSSADMIN.EXE et DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="52ab6-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="52ab6-170">VSSUI</span><span class="sxs-lookup"><span data-stu-id="52ab6-170">VSSUI</span></span>  | <span data-ttu-id="52ab6-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="52ab6-171">0x00000100</span></span> | <span data-ttu-id="52ab6-172">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-172">Yes</span></span>                | <span data-ttu-id="52ab6-173">Interface utilisateur de configuration de clichés instantanés pour dossiers partagés.</span><span class="sxs-lookup"><span data-stu-id="52ab6-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="52ab6-174">L’interface utilisateur est disponible uniquement sur les systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="52ab6-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="52ab6-175">TEST</span><span class="sxs-lookup"><span data-stu-id="52ab6-175">TEST</span></span>   | <span data-ttu-id="52ab6-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="52ab6-176">0x00000200</span></span> | <span data-ttu-id="52ab6-177">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-177">Yes</span></span>                | <span data-ttu-id="52ab6-178">Non applicable.</span><span class="sxs-lookup"><span data-stu-id="52ab6-178">Not applicable.</span></span> <span data-ttu-id="52ab6-179">(Ce module de traçage est réservé.)</span><span class="sxs-lookup"><span data-stu-id="52ab6-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="52ab6-180">IOCTL</span><span class="sxs-lookup"><span data-stu-id="52ab6-180">IOCTL</span></span>  | <span data-ttu-id="52ab6-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="52ab6-181">0x00000400</span></span> | <span data-ttu-id="52ab6-182">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-182">Yes</span></span>                | <span data-ttu-id="52ab6-183">Détails des opérations FSCTL et IOCTL que le service VSS a lancées en appelant la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="52ab6-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="52ab6-184">GÉNÉRAL</span><span class="sxs-lookup"><span data-stu-id="52ab6-184">GEN</span></span>    | <span data-ttu-id="52ab6-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="52ab6-185">0x00000800</span></span> | <span data-ttu-id="52ab6-186">Oui</span><span class="sxs-lookup"><span data-stu-id="52ab6-186">Yes</span></span>                | <span data-ttu-id="52ab6-187">Fonctions générales de l’utilitaire VSS, telles que les allocateurs, les classes de chaîne et les opérations de Registre et de volume.</span><span class="sxs-lookup"><span data-stu-id="52ab6-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="52ab6-188">WRXML</span><span class="sxs-lookup"><span data-stu-id="52ab6-188">WRXML</span></span>  | <span data-ttu-id="52ab6-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="52ab6-189">0x00001000</span></span> | <span data-ttu-id="52ab6-190">Non</span><span class="sxs-lookup"><span data-stu-id="52ab6-190">No</span></span>                 | <span data-ttu-id="52ab6-191">Traitement XML pour les métadonnées de l’enregistreur.</span><span class="sxs-lookup"><span data-stu-id="52ab6-191">XML processing for writer metadata.</span></span> <span data-ttu-id="52ab6-192">Ce module présente un niveau de bruit très élevé.</span><span class="sxs-lookup"><span data-stu-id="52ab6-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="52ab6-193">VSSXML</span><span class="sxs-lookup"><span data-stu-id="52ab6-193">VSSXML</span></span> | <span data-ttu-id="52ab6-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="52ab6-194">0x00002000</span></span> | <span data-ttu-id="52ab6-195">Non</span><span class="sxs-lookup"><span data-stu-id="52ab6-195">No</span></span>                 | <span data-ttu-id="52ab6-196">Classes de base de traitement XML.</span><span class="sxs-lookup"><span data-stu-id="52ab6-196">XML processing base classes.</span></span> <span data-ttu-id="52ab6-197">Ce module présente un niveau de bruit très élevé.</span><span class="sxs-lookup"><span data-stu-id="52ab6-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="52ab6-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modules_</span><span class="sxs-lookup"><span data-stu-id="52ab6-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-199">Active le module spécifié par le *module*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="52ab6-200">Plusieurs modules peuvent être activés à la fois.</span><span class="sxs-lookup"><span data-stu-id="52ab6-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="52ab6-201">Pour répertorier les modules disponibles, tapez **vsstrace – Help modules** à l’invite de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="52ab6-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modules_</span><span class="sxs-lookup"><span data-stu-id="52ab6-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-203">Désactive le module spécifié par le *module*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="52ab6-204">Pour répertorier les modules disponibles, tapez **vsstrace – Help modules** à l’invite de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="52ab6-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="52ab6-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-206">Activez le processus spécifié par *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="52ab6-207">Pour activer tous les processus, utilisez « \* » pour la valeur de *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="52ab6-208">Plusieurs options **PID** peuvent être spécifiées à la fois.</span><span class="sxs-lookup"><span data-stu-id="52ab6-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="52ab6-209">L’ordre des options détermine les processus qui sont activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="52ab6-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="52ab6-210">Par exemple, pour activer uniquement le processus dont l’identificateur de processus est 0xe8c, utilisez **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="52ab6-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="52ab6-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-212">Désactivez le processus spécifié par *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="52ab6-213">Pour désactiver tous les processus, utilisez « \* » pour la valeur de *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="52ab6-214">Plusieurs options **PID** peuvent être spécifiées à la fois.</span><span class="sxs-lookup"><span data-stu-id="52ab6-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="52ab6-215">L’ordre des options détermine les processus qui sont activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="52ab6-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="52ab6-216">Par exemple, pour désactiver tous les processus à l’exception du processus dont l’identificateur de processus est 0xe8c, utilisez **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="52ab6-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>*ThreadID* **+ TID**</span><span class="sxs-lookup"><span data-stu-id="52ab6-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-218">Active le thread spécifié par *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="52ab6-219">Pour activer tous les threads, utilisez « \* » pour la valeur de *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="52ab6-220">Plusieurs options **TID** peuvent être spécifiées à la fois.</span><span class="sxs-lookup"><span data-stu-id="52ab6-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="52ab6-221">L’ordre des options détermine les threads qui sont activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="52ab6-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="52ab6-222">Par exemple, pour activer uniquement le thread dont l’identificateur de processus est 0x31a, utilisez **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="52ab6-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="52ab6-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-224">Désactive le thread spécifié par *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="52ab6-225">Pour désactiver tous les threads, utilisez « \* » pour la valeur de *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="52ab6-226">Plusieurs options **TID** peuvent être spécifiées à la fois.</span><span class="sxs-lookup"><span data-stu-id="52ab6-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="52ab6-227">L’ordre des options détermine les threads qui sont activés ou désactivés.</span><span class="sxs-lookup"><span data-stu-id="52ab6-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="52ab6-228">Par exemple, pour désactiver tous les threads à l’exception du thread dont l’identificateur de processus est 0x31a, utilisez **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="52ab6-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *niveau*</span><span class="sxs-lookup"><span data-stu-id="52ab6-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-230">Utilisez le niveau de suivi spécifié par *niveau*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="52ab6-231">Plus le niveau est élevé, plus la sortie de trace est détaillée.</span><span class="sxs-lookup"><span data-stu-id="52ab6-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="52ab6-232">Chaque niveau comprend tous les niveaux inférieurs.</span><span class="sxs-lookup"><span data-stu-id="52ab6-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="52ab6-233">Le niveau par défaut est 170.</span><span class="sxs-lookup"><span data-stu-id="52ab6-233">The default level is 170.</span></span> <span data-ttu-id="52ab6-234">Les niveaux suivants sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="52ab6-234">The following levels are available.</span></span>



| <span data-ttu-id="52ab6-235">Level</span><span class="sxs-lookup"><span data-stu-id="52ab6-235">Level</span></span> | <span data-ttu-id="52ab6-236">Informations incluses dans la sortie de trace</span><span class="sxs-lookup"><span data-stu-id="52ab6-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="52ab6-237">000</span><span class="sxs-lookup"><span data-stu-id="52ab6-237">000</span></span>   | <span data-ttu-id="52ab6-238">Aucun</span><span class="sxs-lookup"><span data-stu-id="52ab6-238">None</span></span>                                     |
| <span data-ttu-id="52ab6-239">020</span><span class="sxs-lookup"><span data-stu-id="52ab6-239">020</span></span>   | <span data-ttu-id="52ab6-240">Erreurs irrécupérables</span><span class="sxs-lookup"><span data-stu-id="52ab6-240">Fatal errors</span></span>                             |
| <span data-ttu-id="52ab6-241">030</span><span class="sxs-lookup"><span data-stu-id="52ab6-241">030</span></span>   | <span data-ttu-id="52ab6-242">Exceptions non prises en charge</span><span class="sxs-lookup"><span data-stu-id="52ab6-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="52ab6-243">040</span><span class="sxs-lookup"><span data-stu-id="52ab6-243">040</span></span>   | <span data-ttu-id="52ab6-244">Erreurs</span><span class="sxs-lookup"><span data-stu-id="52ab6-244">Errors</span></span>                                   |
| <span data-ttu-id="52ab6-245">050</span><span class="sxs-lookup"><span data-stu-id="52ab6-245">050</span></span>   | <span data-ttu-id="52ab6-246">Assertions</span><span class="sxs-lookup"><span data-stu-id="52ab6-246">Assertions</span></span>                               |
| <span data-ttu-id="52ab6-247">060</span><span class="sxs-lookup"><span data-stu-id="52ab6-247">060</span></span>   | <span data-ttu-id="52ab6-248">Avertissements</span><span class="sxs-lookup"><span data-stu-id="52ab6-248">Warnings</span></span>                                 |
| <span data-ttu-id="52ab6-249">080</span><span class="sxs-lookup"><span data-stu-id="52ab6-249">080</span></span>   | <span data-ttu-id="52ab6-250">Gestion des exceptions</span><span class="sxs-lookup"><span data-stu-id="52ab6-250">Exception handling</span></span>                       |
| <span data-ttu-id="52ab6-251">100</span><span class="sxs-lookup"><span data-stu-id="52ab6-251">100</span></span>   | <span data-ttu-id="52ab6-252">Activité du journal des événements</span><span class="sxs-lookup"><span data-stu-id="52ab6-252">Event Log activity</span></span>                       |
| <span data-ttu-id="52ab6-253">120</span><span class="sxs-lookup"><span data-stu-id="52ab6-253">120</span></span>   | <span data-ttu-id="52ab6-254">Informations générales</span><span class="sxs-lookup"><span data-stu-id="52ab6-254">General information</span></span>                      |
| <span data-ttu-id="52ab6-255">140</span><span class="sxs-lookup"><span data-stu-id="52ab6-255">140</span></span>   | <span data-ttu-id="52ab6-256">Flux de code</span><span class="sxs-lookup"><span data-stu-id="52ab6-256">Code flow</span></span>                                |
| <span data-ttu-id="52ab6-257">160</span><span class="sxs-lookup"><span data-stu-id="52ab6-257">160</span></span>   | <span data-ttu-id="52ab6-258">Entrée et sortie de la fonction</span><span class="sxs-lookup"><span data-stu-id="52ab6-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="52ab6-259">170</span><span class="sxs-lookup"><span data-stu-id="52ab6-259">170</span></span>   | <span data-ttu-id="52ab6-260">Valeurs de retour de fonction</span><span class="sxs-lookup"><span data-stu-id="52ab6-260">Function return values</span></span>                   |
| <span data-ttu-id="52ab6-261">180</span><span class="sxs-lookup"><span data-stu-id="52ab6-261">180</span></span>   | <span data-ttu-id="52ab6-262">Paramètres de fonction (laconique)</span><span class="sxs-lookup"><span data-stu-id="52ab6-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="52ab6-263">190</span><span class="sxs-lookup"><span data-stu-id="52ab6-263">190</span></span>   | <span data-ttu-id="52ab6-264">Paramètres de fonction (verbose)</span><span class="sxs-lookup"><span data-stu-id="52ab6-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="52ab6-265">200</span><span class="sxs-lookup"><span data-stu-id="52ab6-265">200</span></span>   | <span data-ttu-id="52ab6-266">Niveau d’information détaillé 1</span><span class="sxs-lookup"><span data-stu-id="52ab6-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="52ab6-267">210</span><span class="sxs-lookup"><span data-stu-id="52ab6-267">210</span></span>   | <span data-ttu-id="52ab6-268">Informations détaillées niveau 2</span><span class="sxs-lookup"><span data-stu-id="52ab6-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="52ab6-269">220</span><span class="sxs-lookup"><span data-stu-id="52ab6-269">220</span></span>   | <span data-ttu-id="52ab6-270">Niveau d’information détaillé 3</span><span class="sxs-lookup"><span data-stu-id="52ab6-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="52ab6-271">230</span><span class="sxs-lookup"><span data-stu-id="52ab6-271">230</span></span>   | <span data-ttu-id="52ab6-272">Niveau de code rapide 1</span><span class="sxs-lookup"><span data-stu-id="52ab6-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="52ab6-273">240</span><span class="sxs-lookup"><span data-stu-id="52ab6-273">240</span></span>   | <span data-ttu-id="52ab6-274">Niveau de code rapide 2</span><span class="sxs-lookup"><span data-stu-id="52ab6-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="52ab6-275">250</span><span class="sxs-lookup"><span data-stu-id="52ab6-275">250</span></span>   | <span data-ttu-id="52ab6-276">Niveau de code rapide 3</span><span class="sxs-lookup"><span data-stu-id="52ab6-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="52ab6-277">255</span><span class="sxs-lookup"><span data-stu-id="52ab6-277">255</span></span>   | <span data-ttu-id="52ab6-278">Tous</span><span class="sxs-lookup"><span data-stu-id="52ab6-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="52ab6-279"><span id="_indent"></span><span id="_INDENT"></span>**+ retrait**</span><span class="sxs-lookup"><span data-stu-id="52ab6-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-280">Mettez en retrait la sortie de trace mise en forme à chaque limite de fonction et de sous-fonction.</span><span class="sxs-lookup"><span data-stu-id="52ab6-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-281"><span id="-indent"></span><span id="-INDENT"></span>**-Indent**</span><span class="sxs-lookup"><span data-stu-id="52ab6-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-282">Ne mettez pas en retrait la sortie de trace mise en forme.</span><span class="sxs-lookup"><span data-stu-id="52ab6-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*</span><span class="sxs-lookup"><span data-stu-id="52ab6-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-284">Convertit le fichier de sortie logman spécifié par *EtlFile* dans un format de texte lisible.</span><span class="sxs-lookup"><span data-stu-id="52ab6-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *fichier_sortie*</span><span class="sxs-lookup"><span data-stu-id="52ab6-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-286">Enregistrez les informations de traçage dans le fichier de sortie spécifié par *outputfile*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="52ab6-287">Pour des performances optimales, le fichier de sortie doit se trouver sur un volume qui ne fait pas partie du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="52ab6-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="52ab6-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*</span><span class="sxs-lookup"><span data-stu-id="52ab6-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="52ab6-289">Affichez l’aide de la ligne de commande spécifiée par *HelpOption*.</span><span class="sxs-lookup"><span data-stu-id="52ab6-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="52ab6-290">Les valeurs *HelpOption* valides sont **modules**, **levels** et **All**.</span><span class="sxs-lookup"><span data-stu-id="52ab6-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="52ab6-291">La spécification des **modules** entraîne la liste des modules.</span><span class="sxs-lookup"><span data-stu-id="52ab6-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="52ab6-292">La spécification de **niveaux** entraîne la liste des niveaux disponibles.</span><span class="sxs-lookup"><span data-stu-id="52ab6-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="52ab6-293">Si vous spécifiez **All** , l’aide détaillée est affichée.</span><span class="sxs-lookup"><span data-stu-id="52ab6-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="52ab6-294">Si aucune option n’est utilisée, une aide concise est affichée.</span><span class="sxs-lookup"><span data-stu-id="52ab6-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="52ab6-295">Utilisation de logman</span><span class="sxs-lookup"><span data-stu-id="52ab6-295">Using Logman</span></span>

<span data-ttu-id="52ab6-296">La procédure suivante décrit comment utiliser logman avec votre application VSS.</span><span class="sxs-lookup"><span data-stu-id="52ab6-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="52ab6-297">**Pour utiliser logman avec votre application VSS**</span><span class="sxs-lookup"><span data-stu-id="52ab6-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="52ab6-298">Utilisez la commande suivante pour démarrer le suivi :</span><span class="sxs-lookup"><span data-stu-id="52ab6-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="52ab6-299">**logman start VSS-o** *x : \\ \* \* \* VSS. etl-ETS-p {9138500e-3648-4EDB-aa4c-859e9f7b7c38} 0xFFF 170*\*</span><span class="sxs-lookup"><span data-stu-id="52ab6-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="52ab6-300">Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.</span><span class="sxs-lookup"><span data-stu-id="52ab6-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="52ab6-301">Utilisez la commande suivante pour arrêter le suivi :</span><span class="sxs-lookup"><span data-stu-id="52ab6-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="52ab6-302">**logman arrêter VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="52ab6-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="52ab6-303">Le fichier journal des traces est *x \\ :* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="52ab6-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="52ab6-304">Pour plus d’informations sur l’outil Logman, consultez [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="52ab6-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="52ab6-305">Utilisation de tracelog</span><span class="sxs-lookup"><span data-stu-id="52ab6-305">Using Tracelog</span></span>

<span data-ttu-id="52ab6-306">La procédure suivante décrit comment utiliser tracelog.</span><span class="sxs-lookup"><span data-stu-id="52ab6-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="52ab6-307">**Pour utiliser tracelog**</span><span class="sxs-lookup"><span data-stu-id="52ab6-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="52ab6-308">Créez un fichier texte nommé VSS. CTL qui contient uniquement le texte suivant :</span><span class="sxs-lookup"><span data-stu-id="52ab6-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="52ab6-309">**9138500e-3648-4EDB-aa4c-859e9f7b7c38 VSS**</span><span class="sxs-lookup"><span data-stu-id="52ab6-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="52ab6-310">Utilisez la commande suivante pour démarrer le suivi :</span><span class="sxs-lookup"><span data-stu-id="52ab6-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="52ab6-311">**tracelog-Start VSS-f** *x : \\ \* \* \* VSS. etl-GUID VSS. CTL-indicateur 0xFF-Level 0xAA*\*</span><span class="sxs-lookup"><span data-stu-id="52ab6-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="52ab6-312">Remplacez « x : \\ » par le chemin d’accès au répertoire où vous souhaitez que le fichier journal des traces soit stocké.</span><span class="sxs-lookup"><span data-stu-id="52ab6-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="52ab6-313">Utilisez la commande suivante pour arrêter le suivi :</span><span class="sxs-lookup"><span data-stu-id="52ab6-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="52ab6-314">**tracelog-arrêter VSS**</span><span class="sxs-lookup"><span data-stu-id="52ab6-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="52ab6-315">Le fichier journal des traces est *x \\ :* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="52ab6-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="52ab6-316">Pour plus d’informations sur l’outil tracelog, consultez [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="52ab6-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
