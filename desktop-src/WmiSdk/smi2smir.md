---
description: Le compilateur SNMP s’exécute en tant que fichier exécutable unique dans le mode de ligne de commande.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210555"
---
# <a name="smi2smir"></a><span data-ttu-id="98a08-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="98a08-103">smi2smir</span></span>

<span data-ttu-id="98a08-104">Le compilateur SNMP s’exécute en tant que fichier exécutable unique dans le mode de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="98a08-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="98a08-105">Le compilateur accepte un module d’informations SNMP comme entrée et accepte tous les modules supplémentaires nécessaires à la résolution des références externes.</span><span class="sxs-lookup"><span data-stu-id="98a08-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="98a08-106">Utilisez l’un des exemples de syntaxe de ligne de commande suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="98a08-107">Pour plus d’informations sur l’utilisation de ce compilateur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="98a08-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="98a08-108">Commutateurs</span><span class="sxs-lookup"><span data-stu-id="98a08-108">Switches</span></span>

<dl> <span data-ttu-id="98a08-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-110">Le compilateur accepte les arguments de diagnostic suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _niveau de diagnostic_*_>_*</span><span class="sxs-lookup"><span data-stu-id="98a08-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-112">Type de diagnostic à afficher.</span><span class="sxs-lookup"><span data-stu-id="98a08-112">Type of diagnostics to display.</span></span> <span data-ttu-id="98a08-113">La valeur par défaut est 2.</span><span class="sxs-lookup"><span data-stu-id="98a08-113">The default is 2.</span></span>

<span data-ttu-id="98a08-114">La liste suivante répertorie les valeurs de niveau de diagnostic qui peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="98a08-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="98a08-115">0 = en mode silencieux</span><span class="sxs-lookup"><span data-stu-id="98a08-115">0 = Silent</span></span>
-   <span data-ttu-id="98a08-116">1 = irrécupérable</span><span class="sxs-lookup"><span data-stu-id="98a08-116">1 = Fatal</span></span>
-   <span data-ttu-id="98a08-117">2 = fatal et avertissement</span><span class="sxs-lookup"><span data-stu-id="98a08-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="98a08-118">3 = messages fatals, d’avertissement et d’informations</span><span class="sxs-lookup"><span data-stu-id="98a08-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="98a08-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _nombre_*_>_*</span><span class="sxs-lookup"><span data-stu-id="98a08-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-120">Nombre maximal de messages d’avertissement et d’erreur à afficher ; le *nombre* doit être un entier décimal positif.</span><span class="sxs-lookup"><span data-stu-id="98a08-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="98a08-121">Si vous ne spécifiez pas **/c** , le nombre d’erreurs pouvant être signalées est illimité.</span><span class="sxs-lookup"><span data-stu-id="98a08-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="98a08-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-123">Le compilateur accepte les arguments de version suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="98a08-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-125">Spécifie une conformité stricte à l’SMI SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="98a08-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="98a08-126">Le compilateur signale une erreur s’il détecte des instructions non-SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="98a08-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="98a08-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-128">Spécifie une conformité stricte à l’SMI SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="98a08-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="98a08-129">Le compilateur signale une erreur s’il détecte des instructions non-SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="98a08-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="98a08-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-131">Le compilateur accepte les arguments de commande suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="98a08-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-133">Supprime le module spécifié du stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="98a08-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-135">Supprime tous les modules dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="98a08-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-137">Répertorie tous les modules dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="98a08-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-139">Effectue une vérification de la syntaxe locale sur le module.</span><span class="sxs-lookup"><span data-stu-id="98a08-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ce** **\[<** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="98a08-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-141">Effectue des contrôles locaux et externes sur le module.</span><span class="sxs-lookup"><span data-stu-id="98a08-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="98a08-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-143">Effectue des contrôles locaux et externes et charge le module dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="98a08-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-145">Identique à **/a**, mais fonctionne en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="98a08-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="98a08-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-147">Génère un fichier stockage SMIR. mof que vous pouvez charger ultérieurement dans WMI à l’aide du compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="98a08-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="98a08-148">Utilisé par le fournisseur de classes SNMP pour fournir dynamiquement des classes à un ou plusieurs espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="98a08-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="98a08-149">Utilisez cette option lorsque vous ne savez pas quelles MIB sont pris en charge par les périphériques SNMP gérés.</span><span class="sxs-lookup"><span data-stu-id="98a08-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="98a08-150">Le fournisseur de classes SNMP vérifie l’appareil au moment de l’exécution pour la présence de ce MIB et fournit les classes de manière dynamique à l’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="98a08-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="98a08-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-152">Génère un fichier. mof statique qui peut être chargé ultérieurement dans WMI en tant que classes statiques pour un espace de noms particulier.</span><span class="sxs-lookup"><span data-stu-id="98a08-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="98a08-153">Utilisez cette option lorsque vous savez quelles MIB sont pris en charge par les périphériques SNMP gérés.</span><span class="sxs-lookup"><span data-stu-id="98a08-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="98a08-154">Vous pouvez définir le fichier. mof à générer en dirigeant la sortie de votre commande vers un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="98a08-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="98a08-155">N’utilisez pas with **/ext/o**.</span><span class="sxs-lookup"><span data-stu-id="98a08-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="98a08-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-157">Le compilateur accepte les modificateurs de commande suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Directory_*_>_*</span><span class="sxs-lookup"><span data-stu-id="98a08-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="98a08-159">Spécifie un répertoire dans lequel rechercher les modules MIB dépendants.</span><span class="sxs-lookup"><span data-stu-id="98a08-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="98a08-160">Utilisez avec **/a**, **/ce**, **/g**, **/GC** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="98a08-161">L’option **/i** peut apparaître plusieurs fois dans la commande ; les répertoires sont recherchés dans l’ordre spécifié dans la commande.</span><span class="sxs-lookup"><span data-stu-id="98a08-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span><span class="sxs-lookup"><span data-stu-id="98a08-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-163">Génère des informations de contexte, telles que la date, l’heure, l’hôte ou l’utilisateur, dans l’en-tête du fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="98a08-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="98a08-164">À utiliser avec **/g** et **/GC**.</span><span class="sxs-lookup"><span data-stu-id="98a08-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-165"><span id="_t"></span><span id="_T"></span>**commutateur**</span><span class="sxs-lookup"><span data-stu-id="98a08-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-166">Génère des classes [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="98a08-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="98a08-167">Utilisez avec **/a**, **/g** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span><span class="sxs-lookup"><span data-stu-id="98a08-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-169">Génère des classes [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="98a08-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="98a08-170">Utilisez avec **/a**, **/g** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="98a08-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-172">Génère uniquement des classes [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="98a08-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="98a08-173">Utilisez avec **/a**, **/g** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="98a08-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-175">Génère uniquement des classes [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="98a08-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="98a08-176">Utilisez avec **/a**, **/g** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-177"><span id="_s"></span><span id="_S"></span>**commutateur**</span><span class="sxs-lookup"><span data-stu-id="98a08-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-178">Ne mappe pas le texte de la clause DESCRIPTION.</span><span class="sxs-lookup"><span data-stu-id="98a08-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="98a08-179">Utilisez avec **/a**, **/g**, **/GC** et **/sa**.</span><span class="sxs-lookup"><span data-stu-id="98a08-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="98a08-180">Utilisez cette option lorsque vous souhaitez réduire les besoins de stockage.</span><span class="sxs-lookup"><span data-stu-id="98a08-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-181"><span id="_auto"></span><span id="_AUTO"></span>**/Auto**</span><span class="sxs-lookup"><span data-stu-id="98a08-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-182">Reconstruit la table de recherche MIB avant de terminer le commutateur <*CommandArg*>.</span><span class="sxs-lookup"><span data-stu-id="98a08-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="98a08-183">Utilisez avec **/a**, **/ce**, **/g** et **/GC**.</span><span class="sxs-lookup"><span data-stu-id="98a08-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="98a08-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-185">Le compilateur accepte les arguments de registre suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span><span class="sxs-lookup"><span data-stu-id="98a08-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-187">Ajoute le répertoire spécifié au registre.</span><span class="sxs-lookup"><span data-stu-id="98a08-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="98a08-188">L'emplacement par défaut est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="98a08-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-189"><span id="_pd"></span><span id="_PD"></span>**/PD**</span><span class="sxs-lookup"><span data-stu-id="98a08-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-190">Supprime le répertoire spécifié du Registre.</span><span class="sxs-lookup"><span data-stu-id="98a08-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="98a08-191">L'emplacement par défaut est le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="98a08-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span><span class="sxs-lookup"><span data-stu-id="98a08-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-193">Répertorie les répertoires de recherche MIB dans le registre.</span><span class="sxs-lookup"><span data-stu-id="98a08-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="98a08-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-195">Reconstruit l’intégralité de la table de recherche MIB.</span><span class="sxs-lookup"><span data-stu-id="98a08-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="98a08-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-197">Le compilateur accepte les arguments d’informations de module suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-198"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="98a08-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-199">Retourne le nom ASN. 1 du module spécifié.</span><span class="sxs-lookup"><span data-stu-id="98a08-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="98a08-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-201">Retourne les noms ASN. 1 de tous les modules d’importation référencés par le module d’entrée.</span><span class="sxs-lookup"><span data-stu-id="98a08-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="98a08-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="98a08-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="98a08-203">Le compilateur accepte les arguments d’aide suivants.</span><span class="sxs-lookup"><span data-stu-id="98a08-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="98a08-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="98a08-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-205">Affiche de l’aide sur la syntaxe du compilateur SNMP.</span><span class="sxs-lookup"><span data-stu-id="98a08-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="98a08-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="98a08-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="98a08-207">Affiche de l’aide sur la syntaxe du compilateur SNMP.</span><span class="sxs-lookup"><span data-stu-id="98a08-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98a08-208">Notes</span><span class="sxs-lookup"><span data-stu-id="98a08-208">Remarks</span></span>

<span data-ttu-id="98a08-209">Les modules d’informations SNMP sont écrits dans un sous-ensemble de la notation de syntaxe abstraite One (ASN. 1). le compilateur exécute les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="98a08-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="98a08-210">Charge les données à partir du module d’informations SNMP.</span><span class="sxs-lookup"><span data-stu-id="98a08-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="98a08-211">Effectue des opérations de vérification sur le module d’informations.</span><span class="sxs-lookup"><span data-stu-id="98a08-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="98a08-212">Par exemple, il vérifie la syntaxe locale et vérifie les références externes par rapport aux informations contenues dans les modules subsidiaires.</span><span class="sxs-lookup"><span data-stu-id="98a08-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="98a08-213">Supprime toutes les données précédemment chargées du stockage SMIR ou supprime les données chargées à partir d’un module d’informations.</span><span class="sxs-lookup"><span data-stu-id="98a08-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="98a08-214">Retourne le nom du module ASN. 1 d’un fichier spécifié ou retourne le nom du module ASN. 1 de tous les modules importés dans un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="98a08-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="98a08-215">Retourne les noms de module ASN.1 de tous les modules d’informations SNMP actuellement chargés dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="98a08-216">Effectue une résolution automatique des modules importés au lieu de demander aux utilisateurs de spécifier manuellement les modules requis.</span><span class="sxs-lookup"><span data-stu-id="98a08-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="98a08-217">Exécute un mode de chargement en mode silencieux qui ne génère pas de sortie, mais peut être utilisé pour charger des données dans stockage SMIR pendant une opération d’installation.</span><span class="sxs-lookup"><span data-stu-id="98a08-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="98a08-218">Renvoie les données du module informations SNMP dans le stockage SMIR.</span><span class="sxs-lookup"><span data-stu-id="98a08-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="98a08-219">Crée éventuellement un fichier MOF statique ou stockage SMIR contenant la sortie du module information.</span><span class="sxs-lookup"><span data-stu-id="98a08-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="98a08-220">Si nécessaire, vous pouvez charger le fichier. mof statique dans un espace de noms WMI.</span><span class="sxs-lookup"><span data-stu-id="98a08-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="98a08-221">Un fichier stockage SMIR. mof contient le nom de l’espace de noms SNMP dans lequel les classes doivent résider.</span><span class="sxs-lookup"><span data-stu-id="98a08-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="98a08-222">Exemples</span><span class="sxs-lookup"><span data-stu-id="98a08-222">Examples</span></span>

<span data-ttu-id="98a08-223">L’exemple suivant définit le fichier PRA. mof comme sortie du fichier PRA. MIB.</span><span class="sxs-lookup"><span data-stu-id="98a08-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="98a08-224">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98a08-224">Requirements</span></span>



| <span data-ttu-id="98a08-225">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98a08-225">Requirement</span></span> | <span data-ttu-id="98a08-226">Valeur</span><span class="sxs-lookup"><span data-stu-id="98a08-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="98a08-227">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98a08-227">Minimum supported client</span></span><br/> | <span data-ttu-id="98a08-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98a08-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="98a08-229">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="98a08-229">Minimum supported server</span></span><br/> | <span data-ttu-id="98a08-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98a08-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="98a08-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98a08-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a08-232">Messages d’erreur du compilateur SNMP</span><span class="sxs-lookup"><span data-stu-id="98a08-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="98a08-233">Configuration de l’environnement WMI SNMP</span><span class="sxs-lookup"><span data-stu-id="98a08-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="98a08-234">Accès aux appareils SNMP</span><span class="sxs-lookup"><span data-stu-id="98a08-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




