---
description: Les tables suivantes sont requises dans un module de fusion standard.
ms.assetid: 2af6cea0-6d93-4aa5-a708-d305f11986ef
title: Tables de base de données de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a58240c589297cf2540625bc12180252efa42d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535513"
---
# <a name="merge-module-database-tables"></a><span data-ttu-id="2266f-103">Tables de base de données de module de fusion</span><span class="sxs-lookup"><span data-stu-id="2266f-103">Merge Module Database Tables</span></span>

<span data-ttu-id="2266f-104">Les tables suivantes sont requises dans un module de fusion standard.</span><span class="sxs-lookup"><span data-stu-id="2266f-104">The following tables are required in a standard merge module.</span></span>



| <span data-ttu-id="2266f-105">Nom de la table</span><span class="sxs-lookup"><span data-stu-id="2266f-105">Table name</span></span>                                       | <span data-ttu-id="2266f-106">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2266f-106">Comment</span></span>                                                                                          |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2266f-107">Composant</span><span class="sxs-lookup"><span data-stu-id="2266f-107">Component</span></span>](component-table.md)                 | <span data-ttu-id="2266f-108">SOUHAITÉE</span><span class="sxs-lookup"><span data-stu-id="2266f-108">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="2266f-109">Directory</span><span class="sxs-lookup"><span data-stu-id="2266f-109">Directory</span></span>](directory-table.md)                 | <span data-ttu-id="2266f-110">SOUHAITÉE</span><span class="sxs-lookup"><span data-stu-id="2266f-110">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="2266f-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="2266f-111">FeatureComponents</span></span>](featurecomponents-table.md) | <span data-ttu-id="2266f-112">SOUHAITÉE</span><span class="sxs-lookup"><span data-stu-id="2266f-112">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="2266f-113">File</span><span class="sxs-lookup"><span data-stu-id="2266f-113">File</span></span>](file-table.md)                           | <span data-ttu-id="2266f-114">SOUHAITÉE</span><span class="sxs-lookup"><span data-stu-id="2266f-114">(REQUIRED)</span></span>                                                                                       |
| [<span data-ttu-id="2266f-115">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="2266f-115">ModuleSignature</span></span>](modulesignature-table.md)     | <span data-ttu-id="2266f-116">SOUHAITÉE Fusionné dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2266f-116">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="2266f-117">Répertorie les informations identifiant un module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-117">Lists the information identifying a merge module.</span></span> |
| [<span data-ttu-id="2266f-118">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="2266f-118">ModuleComponents</span></span>](modulecomponents-table.md)   | <span data-ttu-id="2266f-119">SOUHAITÉE Fusionné dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2266f-119">(REQUIRED) Merged into the installer database.</span></span> <span data-ttu-id="2266f-120">Répertorie tous les composants du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-120">Lists all the components in the merge module.</span></span>     |



 

<span data-ttu-id="2266f-121">Les tables suivantes se trouvent uniquement dans des modules de fusion ou d’autres bases de données de programme d’installation qui ont déjà été combinées avec un module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-121">The following tables only occur in merge modules or other installer databases that have already been combined with a merge module.</span></span>



| <span data-ttu-id="2266f-122">Nom de la table</span><span class="sxs-lookup"><span data-stu-id="2266f-122">Table name</span></span>                                     | <span data-ttu-id="2266f-123">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2266f-123">Comment</span></span>                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2266f-124">ModuleDependency</span><span class="sxs-lookup"><span data-stu-id="2266f-124">ModuleDependency</span></span>](moduledependency-table.md) | <span data-ttu-id="2266f-125">Fusionné dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2266f-125">Merged into the installer database.</span></span> <span data-ttu-id="2266f-126">Répertorie les autres modules de fusion requis par ce module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-126">Lists other merge modules required by this merge module.</span></span>                |
| [<span data-ttu-id="2266f-127">ModuleExclusion</span><span class="sxs-lookup"><span data-stu-id="2266f-127">ModuleExclusion</span></span>](moduleexclusion-table.md)   | <span data-ttu-id="2266f-128">Fusionné dans la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="2266f-128">Merged into the installer database.</span></span> <span data-ttu-id="2266f-129">Répertorie les autres modules de fusion qui ne sont pas compatibles avec ce module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-129">Lists other merge modules that are incompatible with this merge module.</span></span> |



 

<span data-ttu-id="2266f-130">Les tables ModuleSequence suivantes se trouvent uniquement dans les modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-130">The following ModuleSequence tables only occur in merge modules.</span></span>



| <span data-ttu-id="2266f-131">Nom de la table</span><span class="sxs-lookup"><span data-stu-id="2266f-131">Table name</span></span>                                                             | <span data-ttu-id="2266f-132">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2266f-132">Comment</span></span>                                                                                   |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2266f-133">ModuleAdminUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-133">ModuleAdminUISequence</span></span>](moduleadminuisequence-table.md)               | <span data-ttu-id="2266f-134">Fusionne des actions dans la [table AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-134">Merges actions into the [AdminUISequence table](adminuisequence-table.md).</span></span>               |
| [<span data-ttu-id="2266f-135">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-135">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)     | <span data-ttu-id="2266f-136">Fusionne des actions dans la [table AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-136">Merges actions into the [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>     |
| [<span data-ttu-id="2266f-137">ModuleAdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-137">ModuleAdvtUISequence</span></span>](moduleadvtuisequence-table.md)                 | <span data-ttu-id="2266f-138">N’utilisez pas cette table.</span><span class="sxs-lookup"><span data-stu-id="2266f-138">Do not use this table.</span></span> <span data-ttu-id="2266f-139">Pour plus d’informations, consultez la [table AdvtUISequence](advtuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-139">For details, see [AdvtUISequence table](advtuisequence-table.md).</span></span> |
| [<span data-ttu-id="2266f-140">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-140">ModuleAdvtExecuteSequence</span></span>](moduleadvtexecutesequence-table.md)       | <span data-ttu-id="2266f-141">Fusionne des actions dans la [table AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-141">Merges actions into the [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>       |
| [<span data-ttu-id="2266f-142">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="2266f-142">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)                       | <span data-ttu-id="2266f-143">Répertorie les tables du module qui ne sont pas fusionnées dans le fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="2266f-143">Lists tables in the module that are not merged into the .msi file.</span></span>                        |
| [<span data-ttu-id="2266f-144">ModuleInstallUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-144">ModuleInstallUISequence</span></span>](moduleinstalluisequence-table.md)           | <span data-ttu-id="2266f-145">Fusionne des actions dans la [table InstallUISequence](installuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-145">Merges actions into the [InstallUISequence table](installuisequence-table.md).</span></span>           |
| [<span data-ttu-id="2266f-146">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-146">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md) | <span data-ttu-id="2266f-147">Fusionne des actions dans la [table InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-147">Merges actions into the [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> |



 

<span data-ttu-id="2266f-148">Les tables suivantes sont requises dans chaque module de fusion configurable.</span><span class="sxs-lookup"><span data-stu-id="2266f-148">The following tables are required in every configurable merge module.</span></span> <span data-ttu-id="2266f-149">Mergemod.dll 2,0 ou version ultérieure est requis pour créer un module de fusion configurable.</span><span class="sxs-lookup"><span data-stu-id="2266f-149">Mergemod.dll 2.0 or later is required to create configurable merge module.</span></span> <span data-ttu-id="2266f-150">Pour plus d’informations, consultez [modules de fusion configurables](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="2266f-150">For details, see [Configurable Merge Modules](configurable-merge-modules.md).</span></span>



| <span data-ttu-id="2266f-151">Nom de la table</span><span class="sxs-lookup"><span data-stu-id="2266f-151">Table name</span></span>                                                 | <span data-ttu-id="2266f-152">Commentaire</span><span class="sxs-lookup"><span data-stu-id="2266f-152">Comment</span></span>                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2266f-153">Table ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="2266f-153">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)   | <span data-ttu-id="2266f-154">SOUHAITÉE Cette table n’est pas fusionnée dans la base de données d’installation cible.</span><span class="sxs-lookup"><span data-stu-id="2266f-154">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="2266f-155">Spécifie les champs configurables dans la base de données cible et fournit un modèle pour la configuration de chaque champ.</span><span class="sxs-lookup"><span data-stu-id="2266f-155">Specifies the configurable fields in the target database and provides a template for the configuration of each field.</span></span> |
| [<span data-ttu-id="2266f-156">Table ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2266f-156">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md) | <span data-ttu-id="2266f-157">SOUHAITÉE Cette table n’est pas fusionnée dans la base de données d’installation cible.</span><span class="sxs-lookup"><span data-stu-id="2266f-157">(REQUIRED) This table is not merged into the target installation database.</span></span> <span data-ttu-id="2266f-158">Identifie les attributs configurables du module.</span><span class="sxs-lookup"><span data-stu-id="2266f-158">Identifies the configurable attributes of the module.</span></span>                                                                 |



 

<span data-ttu-id="2266f-159">Les tables de programme d’installation suivantes ne peuvent pas se produire dans un module de fusion standard.</span><span class="sxs-lookup"><span data-stu-id="2266f-159">The following installer tables cannot occur in a standard merge module.</span></span>

-   [<span data-ttu-id="2266f-160">BBControl</span><span class="sxs-lookup"><span data-stu-id="2266f-160">BBControl</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="2266f-161">Blanc</span><span class="sxs-lookup"><span data-stu-id="2266f-161">Billboard</span></span>](billboard-table.md)
-   [<span data-ttu-id="2266f-162">CCPSearch</span><span class="sxs-lookup"><span data-stu-id="2266f-162">CCPSearch</span></span>](ccpsearch-table.md)
-   [<span data-ttu-id="2266f-163">Error</span><span class="sxs-lookup"><span data-stu-id="2266f-163">Error</span></span>](error-table.md)
-   [<span data-ttu-id="2266f-164">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="2266f-164">Feature</span></span>](feature-table.md)
-   [<span data-ttu-id="2266f-165">Table LaunchCondition</span><span class="sxs-lookup"><span data-stu-id="2266f-165">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="2266f-166">Média</span><span class="sxs-lookup"><span data-stu-id="2266f-166">Media</span></span>](media-table.md)
-   [<span data-ttu-id="2266f-167">Patch</span><span class="sxs-lookup"><span data-stu-id="2266f-167">Patch</span></span>](patch-table.md)
-   [<span data-ttu-id="2266f-168">Mettre à niveau</span><span class="sxs-lookup"><span data-stu-id="2266f-168">Upgrade</span></span>](upgrade-table.md)

<span data-ttu-id="2266f-169">Les tables de programme d’installation suivantes sont facultatives dans les modules de fusion.</span><span class="sxs-lookup"><span data-stu-id="2266f-169">The following installer tables are optional in merge modules.</span></span>

-   [<span data-ttu-id="2266f-170">ActionText</span><span class="sxs-lookup"><span data-stu-id="2266f-170">ActionText</span></span>](actiontext-table.md)
-   [<span data-ttu-id="2266f-171">AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-171">AdminExecuteSequence</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="2266f-172">AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-172">AdminUISequence</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="2266f-173">AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-173">AdvtExecuteSequence</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="2266f-174">AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-174">AdvtUISequence</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="2266f-175">AppId</span><span class="sxs-lookup"><span data-stu-id="2266f-175">AppId</span></span>](appid-table.md)
-   [<span data-ttu-id="2266f-176">AppSearch</span><span class="sxs-lookup"><span data-stu-id="2266f-176">AppSearch</span></span>](appsearch-table.md)
-   [<span data-ttu-id="2266f-177">BindImage</span><span class="sxs-lookup"><span data-stu-id="2266f-177">BindImage</span></span>](bindimage-table.md)
-   [<span data-ttu-id="2266f-178">CheckBox</span><span class="sxs-lookup"><span data-stu-id="2266f-178">CheckBox</span></span>](checkbox-table.md)
-   [<span data-ttu-id="2266f-179">Classe</span><span class="sxs-lookup"><span data-stu-id="2266f-179">Class</span></span>](class-table.md)
-   [<span data-ttu-id="2266f-180">ComboBox</span><span class="sxs-lookup"><span data-stu-id="2266f-180">ComboBox</span></span>](combobox-table.md)
-   [<span data-ttu-id="2266f-181">CompLocator</span><span class="sxs-lookup"><span data-stu-id="2266f-181">CompLocator</span></span>](complocator-table.md)
-   [<span data-ttu-id="2266f-182">Contrôle</span><span class="sxs-lookup"><span data-stu-id="2266f-182">Control</span></span>](control-table.md)
-   [<span data-ttu-id="2266f-183">ControlCondition</span><span class="sxs-lookup"><span data-stu-id="2266f-183">ControlCondition</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="2266f-184">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="2266f-184">CreateFolder</span></span>](createfolder-table.md)
-   [<span data-ttu-id="2266f-185">CustomAction</span><span class="sxs-lookup"><span data-stu-id="2266f-185">CustomAction</span></span>](customaction-table.md)
-   [<span data-ttu-id="2266f-186">Dialogue</span><span class="sxs-lookup"><span data-stu-id="2266f-186">Dialog</span></span>](dialog-table.md)
-   [<span data-ttu-id="2266f-187">DrLocator</span><span class="sxs-lookup"><span data-stu-id="2266f-187">DrLocator</span></span>](drlocator-table.md)
-   [<span data-ttu-id="2266f-188">DuplicateFile</span><span class="sxs-lookup"><span data-stu-id="2266f-188">DuplicateFile</span></span>](duplicatefile-table.md)
-   [<span data-ttu-id="2266f-189">Environment</span><span class="sxs-lookup"><span data-stu-id="2266f-189">Environment</span></span>](environment-table.md)
-   [<span data-ttu-id="2266f-190">EventMapping</span><span class="sxs-lookup"><span data-stu-id="2266f-190">EventMapping</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="2266f-191">Extension</span><span class="sxs-lookup"><span data-stu-id="2266f-191">Extension</span></span>](extension-table.md)
-   [<span data-ttu-id="2266f-192">Police</span><span class="sxs-lookup"><span data-stu-id="2266f-192">Font</span></span>](font-table.md)
-   [<span data-ttu-id="2266f-193">Icône</span><span class="sxs-lookup"><span data-stu-id="2266f-193">Icon</span></span>](icon-table.md)
-   [<span data-ttu-id="2266f-194">IniFile</span><span class="sxs-lookup"><span data-stu-id="2266f-194">IniFile</span></span>](inifile-table.md)
-   [<span data-ttu-id="2266f-195">IniLocator</span><span class="sxs-lookup"><span data-stu-id="2266f-195">IniLocator</span></span>](inilocator-table.md)
-   [<span data-ttu-id="2266f-196">InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2266f-196">InstallExecuteSequence</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="2266f-197">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="2266f-197">InstallUISequence</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="2266f-198">ListBox</span><span class="sxs-lookup"><span data-stu-id="2266f-198">ListBox</span></span>](listbox-table.md)
-   [<span data-ttu-id="2266f-199">ListView</span><span class="sxs-lookup"><span data-stu-id="2266f-199">ListView</span></span>](listview-table.md)
-   [<span data-ttu-id="2266f-200">MIME</span><span class="sxs-lookup"><span data-stu-id="2266f-200">MIME</span></span>](mime-table.md)
-   [<span data-ttu-id="2266f-201">MoveFile</span><span class="sxs-lookup"><span data-stu-id="2266f-201">MoveFile</span></span>](movefile-table.md)
-   [<span data-ttu-id="2266f-202">ODBCAttribute</span><span class="sxs-lookup"><span data-stu-id="2266f-202">ODBCAttribute</span></span>](odbcattribute-table.md)
-   [<span data-ttu-id="2266f-203">ODBCDataSource</span><span class="sxs-lookup"><span data-stu-id="2266f-203">ODBCDataSource</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="2266f-204">ODBCDriver</span><span class="sxs-lookup"><span data-stu-id="2266f-204">ODBCDriver</span></span>](odbcdriver-table.md)
-   [<span data-ttu-id="2266f-205">ODBCSourceAttribute</span><span class="sxs-lookup"><span data-stu-id="2266f-205">ODBCSourceAttribute</span></span>](odbcsourceattribute-table.md)
-   [<span data-ttu-id="2266f-206">ODBCTranslator</span><span class="sxs-lookup"><span data-stu-id="2266f-206">ODBCTranslator</span></span>](odbctranslator-table.md)
-   [<span data-ttu-id="2266f-207">Table ProgID</span><span class="sxs-lookup"><span data-stu-id="2266f-207">ProgID Table</span></span>](progid-table.md)
-   [<span data-ttu-id="2266f-208">Propriété</span><span class="sxs-lookup"><span data-stu-id="2266f-208">Property</span></span>](property-table.md)
-   [<span data-ttu-id="2266f-209">PublishComponent</span><span class="sxs-lookup"><span data-stu-id="2266f-209">PublishComponent</span></span>](publishcomponent-table.md)
-   [<span data-ttu-id="2266f-210">RadioButton</span><span class="sxs-lookup"><span data-stu-id="2266f-210">RadioButton</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="2266f-211">Table du Registre</span><span class="sxs-lookup"><span data-stu-id="2266f-211">Registry Table</span></span>](registry-table.md)
-   [<span data-ttu-id="2266f-212">RegLocator</span><span class="sxs-lookup"><span data-stu-id="2266f-212">RegLocator</span></span>](reglocator-table.md)
-   [<span data-ttu-id="2266f-213">RemoveFile</span><span class="sxs-lookup"><span data-stu-id="2266f-213">RemoveFile</span></span>](removefile-table.md)
-   [<span data-ttu-id="2266f-214">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="2266f-214">RemoveIniFile</span></span>](removeinifile-table.md)
-   [<span data-ttu-id="2266f-215">RemoveRegistry</span><span class="sxs-lookup"><span data-stu-id="2266f-215">RemoveRegistry</span></span>](removeregistry-table.md)
-   [<span data-ttu-id="2266f-216">ReserveCost</span><span class="sxs-lookup"><span data-stu-id="2266f-216">ReserveCost</span></span>](reservecost-table.md)
-   [<span data-ttu-id="2266f-217">SelfReg</span><span class="sxs-lookup"><span data-stu-id="2266f-217">SelfReg</span></span>](selfreg-table.md)
-   [<span data-ttu-id="2266f-218">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="2266f-218">ServiceControl</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="2266f-219">ServiceInstall</span><span class="sxs-lookup"><span data-stu-id="2266f-219">ServiceInstall</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="2266f-220">Raccourci</span><span class="sxs-lookup"><span data-stu-id="2266f-220">Shortcut</span></span>](shortcut-table.md)
-   [<span data-ttu-id="2266f-221">Signature</span><span class="sxs-lookup"><span data-stu-id="2266f-221">Signature</span></span>](signature-table.md)
-   [<span data-ttu-id="2266f-222">TextStyle</span><span class="sxs-lookup"><span data-stu-id="2266f-222">TextStyle</span></span>](textstyle-table.md)
-   [<span data-ttu-id="2266f-223">Exportation</span><span class="sxs-lookup"><span data-stu-id="2266f-223">TypeLib</span></span>](typelib-table.md)
-   [<span data-ttu-id="2266f-224">UIText</span><span class="sxs-lookup"><span data-stu-id="2266f-224">UIText</span></span>](uitext-table.md)
-   [<span data-ttu-id="2266f-225">Verbe</span><span class="sxs-lookup"><span data-stu-id="2266f-225">Verb</span></span>](verb-table.md)

 

 



