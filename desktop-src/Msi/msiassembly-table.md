---
description: La table MsiAssembly spécifie Windows Installer paramètres pour les assemblys Microsoft .NET Framework et les assemblys Win32. Pour plus d’informations, consultez Installation d’assemblys dans le global assembly cache et installation d’assemblys Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Table MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953083"
---
# <a name="msiassembly-table"></a><span data-ttu-id="23361-104">Table MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="23361-104">MsiAssembly Table</span></span>

<span data-ttu-id="23361-105">La table MsiAssembly spécifie Windows Installer paramètres pour les assemblys Microsoft .NET Framework et les assemblys Win32.</span><span class="sxs-lookup"><span data-stu-id="23361-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="23361-106">Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="23361-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="23361-107">Sur Windows XP, Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="23361-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="23361-108">Pour plus d’informations, consultez l' [API d’assembly côte à côte](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="23361-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="23361-109">**Windows 2000 :** Cette fonctionnalité n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="23361-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="23361-110">La table MsiAssembly contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="23361-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="23361-111">Colonne</span><span class="sxs-lookup"><span data-stu-id="23361-111">Column</span></span>            | <span data-ttu-id="23361-112">Type</span><span class="sxs-lookup"><span data-stu-id="23361-112">Type</span></span>                         | <span data-ttu-id="23361-113">Clé</span><span class="sxs-lookup"><span data-stu-id="23361-113">Key</span></span> | <span data-ttu-id="23361-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="23361-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="23361-115">-\_</span><span class="sxs-lookup"><span data-stu-id="23361-115">Component\_</span></span>       | [<span data-ttu-id="23361-116">Identificateur</span><span class="sxs-lookup"><span data-stu-id="23361-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="23361-117">O</span><span class="sxs-lookup"><span data-stu-id="23361-117">Y</span></span>   | <span data-ttu-id="23361-118">N</span><span class="sxs-lookup"><span data-stu-id="23361-118">N</span></span>        |
| <span data-ttu-id="23361-119">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="23361-119">Feature\_</span></span>         | [<span data-ttu-id="23361-120">Identificateur</span><span class="sxs-lookup"><span data-stu-id="23361-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="23361-121">N</span><span class="sxs-lookup"><span data-stu-id="23361-121">N</span></span>   | <span data-ttu-id="23361-122">N</span><span class="sxs-lookup"><span data-stu-id="23361-122">N</span></span>        |
| <span data-ttu-id="23361-123">Manifeste de fichier \_</span><span class="sxs-lookup"><span data-stu-id="23361-123">File\_Manifest</span></span>    | [<span data-ttu-id="23361-124">Identificateur</span><span class="sxs-lookup"><span data-stu-id="23361-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="23361-125">N</span><span class="sxs-lookup"><span data-stu-id="23361-125">N</span></span>   | <span data-ttu-id="23361-126">O</span><span class="sxs-lookup"><span data-stu-id="23361-126">Y</span></span>        |
| <span data-ttu-id="23361-127">Application de fichier \_</span><span class="sxs-lookup"><span data-stu-id="23361-127">File\_Application</span></span> | [<span data-ttu-id="23361-128">Identificateur</span><span class="sxs-lookup"><span data-stu-id="23361-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="23361-129">N</span><span class="sxs-lookup"><span data-stu-id="23361-129">N</span></span>   | <span data-ttu-id="23361-130">O</span><span class="sxs-lookup"><span data-stu-id="23361-130">Y</span></span>        |
| <span data-ttu-id="23361-131">Attributs</span><span class="sxs-lookup"><span data-stu-id="23361-131">Attributes</span></span>        | [<span data-ttu-id="23361-132">Integer</span><span class="sxs-lookup"><span data-stu-id="23361-132">Integer</span></span>](integer.md)       | <span data-ttu-id="23361-133">N</span><span class="sxs-lookup"><span data-stu-id="23361-133">N</span></span>   | <span data-ttu-id="23361-134">O</span><span class="sxs-lookup"><span data-stu-id="23361-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="23361-135">Colonnes</span><span class="sxs-lookup"><span data-stu-id="23361-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="23361-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="23361-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="23361-137">Clé dans la [table de composants](component-table.md) qui spécifie le composant Windows Installer qui contient cet assembly.</span><span class="sxs-lookup"><span data-stu-id="23361-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="23361-138">La valeur de ce champ ne doit pas être définie sur null.</span><span class="sxs-lookup"><span data-stu-id="23361-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="23361-139">Le champ keyPath du composant dans la [table Component](component-table.md) ne doit pas avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="23361-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="23361-140">Pour les assemblys Win32, le chemin d’accès du composant ne peut pas être le fichier manifeste spécifié dans le manifeste de fichier \_ .</span><span class="sxs-lookup"><span data-stu-id="23361-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="23361-141">Le manifeste peut être le chemin d’accès du keyPath pour un .NET Framework ou un assembly de stratégie.</span><span class="sxs-lookup"><span data-stu-id="23361-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="23361-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="23361-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="23361-143">Clé dans la [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="23361-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="23361-144">Lorsque l’assembly doit être installé par une installation de fonctionnalité, Windows Installer installe la fonctionnalité vers laquelle pointe ce champ.</span><span class="sxs-lookup"><span data-stu-id="23361-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="23361-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifeste de fichier \_</span><span class="sxs-lookup"><span data-stu-id="23361-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="23361-146">Clé externe dans la [table de fichiers](file-table.md) qui spécifie le fichier qui contient le manifeste d’un assembly .NET Framework ou d’un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="23361-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="23361-147">Pour un assembly Win32, ne spécifiez pas ce fichier comme fichier de chemin d’accès de la clé du composant dans le champ keyPath de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="23361-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="23361-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Application de fichier \_</span><span class="sxs-lookup"><span data-stu-id="23361-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="23361-149">Pour installer l’assembly à un emplacement privé, entrez le fichier du chemin d’accès de la clé pour le composant d’assembly dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="23361-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="23361-150">Il s’agit de la valeur qui apparaît dans le champ keyPath (chemin d’accès) de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="23361-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="23361-151">Le programme d’installation peut ensuite installer l’assembly dans la structure de répertoires du composant spécifié dans la [table de répertoires](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="23361-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="23361-152">Ce champ doit avoir la valeur null si l’assembly doit être installé dans le Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="23361-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="23361-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="23361-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="23361-154">Entrez la valeur 1 (un) pour un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="23361-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="23361-155">Entrez la valeur 0 (zéro) pour un assembly de .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="23361-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="23361-156">Si la colonne d’attributs a la valeur NULL, le programme d’installation traite l’assembly comme un .NET Framework assembly.</span><span class="sxs-lookup"><span data-stu-id="23361-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23361-157">Notes</span><span class="sxs-lookup"><span data-stu-id="23361-157">Remarks</span></span>

<span data-ttu-id="23361-158">S’il existe au moins une entrée dans la table MsiAssembly, la [table InstallExecuteSequence](installexecutesequence-table.md) doit contenir l' [action MsiPublishAssemblies](msipublishassemblies-action.md)et l' [action MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="23361-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="23361-159">Étant donné que les assemblys ne peuvent pas être restaurés une fois qu’ils ont été validés, Windows Installer utilise un processus d’installation en deux étapes.</span><span class="sxs-lookup"><span data-stu-id="23361-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="23361-160">Les interfaces vers les assemblys sont créées pendant les opérations d’installation qui sont générées par l' [action MsiPublishAssemblies](msipublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="23361-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="23361-161">Les assemblys ne sont pas validés avant la réussite de l’exécution de l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="23361-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="23361-162">Cela signifie que si vous créez une action ou une ressource personnalisée qui s’appuie sur l’assembly, elle doit être séquencée après l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="23361-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="23361-163">Par exemple, si vous devez démarrer un service qui dépend d’un assembly dans le global assembly cache (GAC), vous devez planifier le démarrage de ce service après l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="23361-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="23361-164">Cela signifie que vous ne pouvez pas utiliser la [table ServiceControl](servicecontrol-table.md) pour démarrer le service. au lieu de cela, vous devez utiliser une action personnalisée qui est séquencée après InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="23361-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="23361-165">Validation</span><span class="sxs-lookup"><span data-stu-id="23361-165">Validation</span></span>

<dl>

[<span data-ttu-id="23361-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="23361-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="23361-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="23361-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="23361-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="23361-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="23361-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="23361-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="23361-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="23361-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="23361-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="23361-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
