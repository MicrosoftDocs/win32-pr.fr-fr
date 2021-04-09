---
description: La table CustomAction fournit les moyens d’intégrer du code personnalisé et des données dans l’installation. La source du code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un fichier exécutable existant.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Table CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752324"
---
# <a name="customaction-table"></a><span data-ttu-id="6971b-104">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="6971b-104">CustomAction Table</span></span>

<span data-ttu-id="6971b-105">La table CustomAction fournit les moyens d’intégrer du code personnalisé et des données dans l’installation.</span><span class="sxs-lookup"><span data-stu-id="6971b-105">The CustomAction table provides the means of integrating custom code and data into the installation.</span></span> <span data-ttu-id="6971b-106">La source du code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un fichier exécutable existant.</span><span class="sxs-lookup"><span data-stu-id="6971b-106">The source of the code that is executed can be a stream contained within the database, a recently installed file, or an existing executable file.</span></span>

<span data-ttu-id="6971b-107">La table CustomAction contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="6971b-107">The CustomAction table has the following columns.</span></span>



| <span data-ttu-id="6971b-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="6971b-108">Column</span></span>       | <span data-ttu-id="6971b-109">Type</span><span class="sxs-lookup"><span data-stu-id="6971b-109">Type</span></span>                               | <span data-ttu-id="6971b-110">Clé</span><span class="sxs-lookup"><span data-stu-id="6971b-110">Key</span></span> | <span data-ttu-id="6971b-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6971b-111">Nullable</span></span> |
|--------------|------------------------------------|-----|----------|
| <span data-ttu-id="6971b-112">Action</span><span class="sxs-lookup"><span data-stu-id="6971b-112">Action</span></span>       | [<span data-ttu-id="6971b-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="6971b-113">Identifier</span></span>](identifier.md)       | <span data-ttu-id="6971b-114">O</span><span class="sxs-lookup"><span data-stu-id="6971b-114">Y</span></span>   | <span data-ttu-id="6971b-115">N</span><span class="sxs-lookup"><span data-stu-id="6971b-115">N</span></span>        |
| <span data-ttu-id="6971b-116">Type</span><span class="sxs-lookup"><span data-stu-id="6971b-116">Type</span></span>         | [<span data-ttu-id="6971b-117">Integer</span><span class="sxs-lookup"><span data-stu-id="6971b-117">Integer</span></span>](integer.md)             | <span data-ttu-id="6971b-118">N</span><span class="sxs-lookup"><span data-stu-id="6971b-118">N</span></span>   | <span data-ttu-id="6971b-119">N</span><span class="sxs-lookup"><span data-stu-id="6971b-119">N</span></span>        |
| <span data-ttu-id="6971b-120">Source</span><span class="sxs-lookup"><span data-stu-id="6971b-120">Source</span></span>       | [<span data-ttu-id="6971b-121">CustomSource</span><span class="sxs-lookup"><span data-stu-id="6971b-121">CustomSource</span></span>](customsource.md)   | <span data-ttu-id="6971b-122">N</span><span class="sxs-lookup"><span data-stu-id="6971b-122">N</span></span>   | <span data-ttu-id="6971b-123">O</span><span class="sxs-lookup"><span data-stu-id="6971b-123">Y</span></span>        |
| <span data-ttu-id="6971b-124">Cible</span><span class="sxs-lookup"><span data-stu-id="6971b-124">Target</span></span>       | [<span data-ttu-id="6971b-125">Correct</span><span class="sxs-lookup"><span data-stu-id="6971b-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="6971b-126">N</span><span class="sxs-lookup"><span data-stu-id="6971b-126">N</span></span>   | <span data-ttu-id="6971b-127">O</span><span class="sxs-lookup"><span data-stu-id="6971b-127">Y</span></span>        |
| <span data-ttu-id="6971b-128">ExtendedType</span><span class="sxs-lookup"><span data-stu-id="6971b-128">ExtendedType</span></span> | [<span data-ttu-id="6971b-129">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="6971b-129">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="6971b-130">N</span><span class="sxs-lookup"><span data-stu-id="6971b-130">N</span></span>   | <span data-ttu-id="6971b-131">O</span><span class="sxs-lookup"><span data-stu-id="6971b-131">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6971b-132">Colonnes</span><span class="sxs-lookup"><span data-stu-id="6971b-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6971b-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="6971b-133"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="6971b-134">Nom de l'action.</span><span class="sxs-lookup"><span data-stu-id="6971b-134">Name of the action.</span></span> <span data-ttu-id="6971b-135">L’action apparaît normalement dans une table de séquence, sauf si elle est appelée par une autre action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6971b-135">The action normally appears in a sequence table unless it is called by another custom action.</span></span> <span data-ttu-id="6971b-136">Si le nom correspond à une action intégrée, l’action personnalisée n’est jamais appelée.</span><span class="sxs-lookup"><span data-stu-id="6971b-136">If the name matches any built-in action, then the custom action is never called.</span></span>

<span data-ttu-id="6971b-137">Clé de table primaire.</span><span class="sxs-lookup"><span data-stu-id="6971b-137">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="6971b-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer</span><span class="sxs-lookup"><span data-stu-id="6971b-138"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="6971b-139">Champ de bits d’indicateur spécifiant le type de base des actions personnalisées et des options.</span><span class="sxs-lookup"><span data-stu-id="6971b-139">A field of flag bits specifying the basic type of custom action and options.</span></span> <span data-ttu-id="6971b-140">Consultez la [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md) pour obtenir la liste des types de base.</span><span class="sxs-lookup"><span data-stu-id="6971b-140">See [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a list of the basic types.</span></span> <span data-ttu-id="6971b-141">Consultez Options de [traitement des retours d’actions](custom-action-return-processing-options.md)personnalisées, [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md), [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md)et [action personnalisée In-Script les options d’exécution](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="6971b-141">See [Custom Action Return Processing Options](custom-action-return-processing-options.md), [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md), [Custom Action Hidden Target Option](custom-action-hidden-target-option.md), and [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

</dd> <dt>

<span data-ttu-id="6971b-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code</span><span class="sxs-lookup"><span data-stu-id="6971b-142"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Source</span></span>
</dt> <dd>

<span data-ttu-id="6971b-143">Un nom de propriété ou une clé externe dans une autre table.</span><span class="sxs-lookup"><span data-stu-id="6971b-143">A property name or external key into another table.</span></span> <span data-ttu-id="6971b-144">Pour plus d’informations sur les sources d’action personnalisées possibles, consultez [sources d’action personnalisées](custom-action-sources.md) et [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="6971b-144">For a discussion of the possible custom action sources, see [Custom Action Sources](custom-action-sources.md) and the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span> <span data-ttu-id="6971b-145">Par exemple, la colonne source peut contenir une clé externe dans la première colonne de l’une des tables suivantes, contenant la source du code d’action personnalisé.</span><span class="sxs-lookup"><span data-stu-id="6971b-145">For example, the Source column may contain an external key into the first column of one of the following tables containing the source of the custom action code.</span></span>

<span data-ttu-id="6971b-146">[Table de répertoire](directory-table.md) pour l’appel d’exécutables existants.</span><span class="sxs-lookup"><span data-stu-id="6971b-146">[Directory table](directory-table.md) for calling existing executables.</span></span>

<span data-ttu-id="6971b-147">[Table de fichiers](file-table.md) pour appeler des exécutables et des dll qui viennent d’être installés.</span><span class="sxs-lookup"><span data-stu-id="6971b-147">[File table](file-table.md) for calling executables and DLLs that have just been installed.</span></span>

<span data-ttu-id="6971b-148">[Table binaire](binary-table.md) pour appeler des fichiers exécutables, des dll et des données stockées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="6971b-148">[Binary table](binary-table.md) for calling executables, DLLs, and data stored in the database.</span></span>

<span data-ttu-id="6971b-149">[Table de propriétés](property-table.md) permettant d’appeler des exécutables dont les chemins sont détenus par une propriété.</span><span class="sxs-lookup"><span data-stu-id="6971b-149">[Property table](property-table.md) for calling executables whose paths are held by a property.</span></span>

</dd> <dt>

<span data-ttu-id="6971b-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif</span><span class="sxs-lookup"><span data-stu-id="6971b-150"><span id="Target"></span><span id="target"></span><span id="TARGET"></span>Target</span></span>
</dt> <dd>

<span data-ttu-id="6971b-151">Paramètre d’exécution qui dépend du type de base de l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6971b-151">An execution parameter that depends on the basic type of custom action.</span></span> <span data-ttu-id="6971b-152">Consultez la [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md) pour obtenir une description de ce qui doit être entré dans ce champ pour chaque type d’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6971b-152">See the [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md) for a description of what should be entered in this field for each type of custom action.</span></span> <span data-ttu-id="6971b-153">Par exemple, ce champ peut contenir les éléments suivants en fonction de l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="6971b-153">For example, this field may contain the following depending on the custom action.</span></span>



| <span data-ttu-id="6971b-154">Cible</span><span class="sxs-lookup"><span data-stu-id="6971b-154">Target</span></span>                                    | <span data-ttu-id="6971b-155">Action personnalisée</span><span class="sxs-lookup"><span data-stu-id="6971b-155">Custom action</span></span>                         |
|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="6971b-156">Point d’entrée (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="6971b-156">Entry point (required)</span></span>                    | <span data-ttu-id="6971b-157">Appel d’une DLL.</span><span class="sxs-lookup"><span data-stu-id="6971b-157">Calling a DLL.</span></span>                        |
| <span data-ttu-id="6971b-158">Nom de l’exécutable avec arguments (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="6971b-158">Executable name with arguments (required)</span></span> | <span data-ttu-id="6971b-159">Appel d’un fichier exécutable existant.</span><span class="sxs-lookup"><span data-stu-id="6971b-159">Calling an existing executable.</span></span>       |
| <span data-ttu-id="6971b-160">Arguments de ligne de commande (facultatif)</span><span class="sxs-lookup"><span data-stu-id="6971b-160">Command line arguments (optional)</span></span>         | <span data-ttu-id="6971b-161">Appel d’un exécutable vient d’être installé.</span><span class="sxs-lookup"><span data-stu-id="6971b-161">Calling an executable just installed.</span></span> |
| <span data-ttu-id="6971b-162">Nom du fichier cible (obligatoire)</span><span class="sxs-lookup"><span data-stu-id="6971b-162">Target file name (required)</span></span>               | <span data-ttu-id="6971b-163">Création d’un fichier à partir de données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6971b-163">Creating a file from custom data.</span></span>     |
| <span data-ttu-id="6971b-164">Null</span><span class="sxs-lookup"><span data-stu-id="6971b-164">Null</span></span>                                      | <span data-ttu-id="6971b-165">Exécution du code de script.</span><span class="sxs-lookup"><span data-stu-id="6971b-165">Executing script code.</span></span>                |



 

</dd> <dt>

<span data-ttu-id="6971b-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span><span class="sxs-lookup"><span data-stu-id="6971b-166"><span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType</span></span>
</dt> <dd>

<span data-ttu-id="6971b-167">Entrez la valeur **msidbCustomActionTypePatchUninstall** dans ce champ pour spécifier une action personnalisée avec l' [option action personnalisée désinstaller le correctif](custom-action-patch-uninstall-option.md).</span><span class="sxs-lookup"><span data-stu-id="6971b-167">Enter the **msidbCustomActionTypePatchUninstall** value in this field to specify a custom action with the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md).</span></span>

<span data-ttu-id="6971b-168">**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6971b-168">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="6971b-169">Cette option est disponible à partir de Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="6971b-169">This option is available beginning with Windows Installer 4.5.</span></span>

</dd> </dl>

<span data-ttu-id="6971b-170">Pour plus d’informations, consultez toutes les rubriques sous [actions personnalisées](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="6971b-170">For more information, see all the topics under [Custom Actions](custom-actions.md).</span></span>

## <a name="validation"></a><span data-ttu-id="6971b-171">Validation</span><span class="sxs-lookup"><span data-stu-id="6971b-171">Validation</span></span>

<dl>

[<span data-ttu-id="6971b-172">ICE03</span><span class="sxs-lookup"><span data-stu-id="6971b-172">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6971b-173">ICE06</span><span class="sxs-lookup"><span data-stu-id="6971b-173">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6971b-174">ICE12</span><span class="sxs-lookup"><span data-stu-id="6971b-174">ICE12</span></span>](ice12.md)  
[<span data-ttu-id="6971b-175">ICE27</span><span class="sxs-lookup"><span data-stu-id="6971b-175">ICE27</span></span>](ice27.md)  
[<span data-ttu-id="6971b-176">ICE46</span><span class="sxs-lookup"><span data-stu-id="6971b-176">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="6971b-177">ICE63</span><span class="sxs-lookup"><span data-stu-id="6971b-177">ICE63</span></span>](ice63.md)  
[<span data-ttu-id="6971b-178">ICE68</span><span class="sxs-lookup"><span data-stu-id="6971b-178">ICE68</span></span>](ice68.md)  
[<span data-ttu-id="6971b-179">ICE72</span><span class="sxs-lookup"><span data-stu-id="6971b-179">ICE72</span></span>](ice72.md)  
[<span data-ttu-id="6971b-180">ICE75</span><span class="sxs-lookup"><span data-stu-id="6971b-180">ICE75</span></span>](ice75.md)  
[<span data-ttu-id="6971b-181">ICE77</span><span class="sxs-lookup"><span data-stu-id="6971b-181">ICE77</span></span>](ice77.md)  
[<span data-ttu-id="6971b-182">ICE80</span><span class="sxs-lookup"><span data-stu-id="6971b-182">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="6971b-183">ICE88</span><span class="sxs-lookup"><span data-stu-id="6971b-183">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="6971b-184">ICE93</span><span class="sxs-lookup"><span data-stu-id="6971b-184">ICE93</span></span>](ice93.md)  
</dl>

 

 



