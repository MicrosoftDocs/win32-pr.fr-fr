---
description: La table MsiAssembly et la table MsiAssemblyName spécifient Windows Installer paramètres pour les assemblys common language runtime et les assemblys Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Table MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531752"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="26ef6-103">Table MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="26ef6-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="26ef6-104">La [table MsiAssembly](msiassembly-table.md) et la table MsiAssemblyName spécifient Windows Installer paramètres pour les assemblys Common Language Runtime et les assemblys Win32.</span><span class="sxs-lookup"><span data-stu-id="26ef6-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="26ef6-105">Pour plus d’informations, consultez [installation d’assemblys dans le global assembly cache](installation-of-assemblies-to-the-global-assembly-cache.md) et [installation d’assemblys Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="26ef6-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="26ef6-106">La table MsiAssemblyName spécifie le schéma pour les éléments d’un nom de cache d’assembly fort pour un assembly .NET Framework ou Win32.</span><span class="sxs-lookup"><span data-stu-id="26ef6-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="26ef6-107">Le nom est construit en ajoutant tous les éléments avec la même clé de composant \_ .</span><span class="sxs-lookup"><span data-stu-id="26ef6-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="26ef6-108">Consultez l’exemple qui suit.</span><span class="sxs-lookup"><span data-stu-id="26ef6-108">See the following example.</span></span>

<span data-ttu-id="26ef6-109">Windows Installer pouvez installer des assemblys Win32 en tant qu' [assemblys côte à côte](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="26ef6-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="26ef6-110">Pour plus d’informations, consultez l' [API d’assembly côte à côte](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="26ef6-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="26ef6-111">La table MsiAssemblyName contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="26ef6-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="26ef6-112">Colonne</span><span class="sxs-lookup"><span data-stu-id="26ef6-112">Column</span></span>      | <span data-ttu-id="26ef6-113">Type</span><span class="sxs-lookup"><span data-stu-id="26ef6-113">Type</span></span>                         | <span data-ttu-id="26ef6-114">Clé</span><span class="sxs-lookup"><span data-stu-id="26ef6-114">Key</span></span> | <span data-ttu-id="26ef6-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="26ef6-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="26ef6-116">-\_</span><span class="sxs-lookup"><span data-stu-id="26ef6-116">Component\_</span></span> | [<span data-ttu-id="26ef6-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="26ef6-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="26ef6-118">O</span><span class="sxs-lookup"><span data-stu-id="26ef6-118">Y</span></span>   | <span data-ttu-id="26ef6-119">N</span><span class="sxs-lookup"><span data-stu-id="26ef6-119">N</span></span>        |
| <span data-ttu-id="26ef6-120">Nom</span><span class="sxs-lookup"><span data-stu-id="26ef6-120">Name</span></span>        | [<span data-ttu-id="26ef6-121">Text</span><span class="sxs-lookup"><span data-stu-id="26ef6-121">Text</span></span>](text.md)             | <span data-ttu-id="26ef6-122">O</span><span class="sxs-lookup"><span data-stu-id="26ef6-122">Y</span></span>   | <span data-ttu-id="26ef6-123">N</span><span class="sxs-lookup"><span data-stu-id="26ef6-123">N</span></span>        |
| <span data-ttu-id="26ef6-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ef6-124">Value</span></span>       | [<span data-ttu-id="26ef6-125">Text</span><span class="sxs-lookup"><span data-stu-id="26ef6-125">Text</span></span>](text.md)             | <span data-ttu-id="26ef6-126">N</span><span class="sxs-lookup"><span data-stu-id="26ef6-126">N</span></span>   | <span data-ttu-id="26ef6-127">N</span><span class="sxs-lookup"><span data-stu-id="26ef6-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="26ef6-128">Colonnes</span><span class="sxs-lookup"><span data-stu-id="26ef6-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="26ef6-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="26ef6-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="26ef6-130">Clé dans la [table de composants](component-table.md) qui spécifie le composant Windows Installer qui contient cet assembly.</span><span class="sxs-lookup"><span data-stu-id="26ef6-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="26ef6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="26ef6-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="26ef6-132">Nom de l’attribut associé à la valeur spécifiée dans la colonne valeur.</span><span class="sxs-lookup"><span data-stu-id="26ef6-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="26ef6-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée</span><span class="sxs-lookup"><span data-stu-id="26ef6-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="26ef6-134">Valeur associée au nom spécifié dans la colonne nom.</span><span class="sxs-lookup"><span data-stu-id="26ef6-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26ef6-135">Notes</span><span class="sxs-lookup"><span data-stu-id="26ef6-135">Remarks</span></span>

<span data-ttu-id="26ef6-136">Les informations créées dans la table MsiAssemblyName doivent correspondre aux informations contenues dans le fichier manifeste de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="26ef6-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="26ef6-137">Si les informations contenues dans le manifeste et la table MsiAssemblyName ne correspondent pas, la suppression de l’application peut permettre de conserver l’assembly sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="26ef6-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="26ef6-138">Pour les assemblys Win32, il doit y avoir une ligne dans la table MsiAssemblyName pour chacune des entrées suivantes dans le champ Name : type, Name, version, language, publicKeyToken et processorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="26ef6-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="26ef6-139">La valeur correspondante pour chaque nom peut être entrée dans le champ valeur.</span><span class="sxs-lookup"><span data-stu-id="26ef6-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="26ef6-140">Les paires nom-valeur dans la table MsiAssemblyName doivent correspondre aux attributs type, Name, version, language, publicKeyToken et processorArchitecture dans le manifeste de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="26ef6-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="26ef6-141">Pour les assemblys common language runtime privés (.NET FrameworkVersions 1,0 et 1,1), la table MsiAssemblyName doit inclure une ligne pour chacune des entrées suivantes dans le champ Nom : nom, version et culture.</span><span class="sxs-lookup"><span data-stu-id="26ef6-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="26ef6-142">La valeur correspondante pour chaque nom peut être entrée dans le champ valeur.</span><span class="sxs-lookup"><span data-stu-id="26ef6-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="26ef6-143">Pour les assemblys common language runtime globaux (.NET Framework versions 1,0 et 1,1), la table MsiAssemblyName doit inclure une ligne pour chacune des entrées suivantes dans le champ Nom : nom, version, culture et PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="26ef6-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="26ef6-144">La valeur correspondante pour chaque nom peut être entrée dans le champ valeur.</span><span class="sxs-lookup"><span data-stu-id="26ef6-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="26ef6-145">Le .NET Framework version 1,1 est la version minimale qui peut être utilisée pour effectuer une mise à jour sur place d’un assembly de common language runtime global.</span><span class="sxs-lookup"><span data-stu-id="26ef6-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="26ef6-146">Vous pouvez vérifier la version de la propriété [**MsiNetAssemblySupport**](msinetassemblysupport.md) .</span><span class="sxs-lookup"><span data-stu-id="26ef6-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="26ef6-147">La table MsiAssemblyName doit également avoir un champ FileVersion, car ce type de mise à jour d’assembly modifie uniquement la FileVersion.</span><span class="sxs-lookup"><span data-stu-id="26ef6-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="26ef6-148">Pour plus d’informations, consultez [mise à jour des assemblys](updating-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="26ef6-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="26ef6-149">Par exemple, le manifeste de l’assembly pour le composant a peut avoir une section assemblyIdentity comme suit pour un assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="26ef6-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="26ef6-150">Dans ce cas, remplissez la table MsiAssemblyName comme suit.</span><span class="sxs-lookup"><span data-stu-id="26ef6-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="26ef6-151">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-151">Component</span></span>  | <span data-ttu-id="26ef6-152">Nom</span><span class="sxs-lookup"><span data-stu-id="26ef6-152">Name</span></span>                  | <span data-ttu-id="26ef6-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ef6-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="26ef6-154">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-154">ComponentA</span></span> | <span data-ttu-id="26ef6-155">type</span><span class="sxs-lookup"><span data-stu-id="26ef6-155">type</span></span>                  | <span data-ttu-id="26ef6-156">32</span><span class="sxs-lookup"><span data-stu-id="26ef6-156">win32</span></span>             |
| <span data-ttu-id="26ef6-157">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-157">ComponentA</span></span> | <span data-ttu-id="26ef6-158">name</span><span class="sxs-lookup"><span data-stu-id="26ef6-158">name</span></span>                  | <span data-ttu-id="26ef6-159">MS-sxstest-simple</span><span class="sxs-lookup"><span data-stu-id="26ef6-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="26ef6-160">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-160">ComponentA</span></span> | <span data-ttu-id="26ef6-161">version</span><span class="sxs-lookup"><span data-stu-id="26ef6-161">version</span></span>               | <span data-ttu-id="26ef6-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="26ef6-162">1.0.0.0</span></span>           |
| <span data-ttu-id="26ef6-163">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-163">ComponentA</span></span> | <span data-ttu-id="26ef6-164">langage</span><span class="sxs-lookup"><span data-stu-id="26ef6-164">language</span></span>              | <span data-ttu-id="26ef6-165">en</span><span class="sxs-lookup"><span data-stu-id="26ef6-165">en</span></span>                |
| <span data-ttu-id="26ef6-166">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-166">ComponentA</span></span> | <span data-ttu-id="26ef6-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="26ef6-167">publicKeyToken</span></span>        | <span data-ttu-id="26ef6-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="26ef6-168">1111111111222222</span></span>  |
| <span data-ttu-id="26ef6-169">Composant</span><span class="sxs-lookup"><span data-stu-id="26ef6-169">ComponentA</span></span> | <span data-ttu-id="26ef6-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="26ef6-170">processorArchitecture</span></span> | <span data-ttu-id="26ef6-171">x86</span><span class="sxs-lookup"><span data-stu-id="26ef6-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="26ef6-172">Validation</span><span class="sxs-lookup"><span data-stu-id="26ef6-172">Validation</span></span>

<dl>

[<span data-ttu-id="26ef6-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="26ef6-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="26ef6-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="26ef6-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="26ef6-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="26ef6-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="26ef6-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="26ef6-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="26ef6-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="26ef6-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
