---
description: Un fichier de configuration d’éditeur est un fichier XML qui redirige globalement les applications et les assemblys de à l’aide d’une version d’un assembly côte à côte vers une autre version du même assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Fichiers de configuration du serveur de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867889"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="d3c84-103">Fichiers de configuration du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="d3c84-103">Publisher Configuration Files</span></span>

<span data-ttu-id="d3c84-104">Un fichier de configuration d’éditeur est un fichier XML qui redirige globalement les applications et les assemblys de à l’aide d’une version d’un assembly côte à côte vers une autre version du même assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="d3c84-105">En règle générale, l’éditeur de l’assembly émet une mise à jour ou un correctif de sécurité compatible pour chaque assembly en émettant un fichier de configuration d’éditeur à installer avec une mise à jour Service Pack.</span><span class="sxs-lookup"><span data-stu-id="d3c84-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="d3c84-106">C’est ce que l’on appelle la configuration du serveur de [publication](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="d3c84-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="d3c84-107">Pour plus d’informations sur ce type de [configuration](configuration.md) , consultez Configuration de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="d3c84-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="d3c84-108">Les fichiers de configuration du serveur de publication possèdent les éléments et les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d3c84-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="d3c84-109">Pour obtenir une liste complète du schéma XML, consultez [schéma du fichier de configuration](publisher-configuration-file-schema.md)de l’éditeur.</span><span class="sxs-lookup"><span data-stu-id="d3c84-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="d3c84-110">Élément</span><span class="sxs-lookup"><span data-stu-id="d3c84-110">Element</span></span>               | <span data-ttu-id="d3c84-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="d3c84-111">Attributes</span></span>                | <span data-ttu-id="d3c84-112">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d3c84-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="d3c84-113">**assembly**</span><span class="sxs-lookup"><span data-stu-id="d3c84-113">**assembly**</span></span>          |                           | <span data-ttu-id="d3c84-114">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-114">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-115">**manifestVersion**</span></span>       | <span data-ttu-id="d3c84-116">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-116">Yes</span></span>      |
| <span data-ttu-id="d3c84-117">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="d3c84-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="d3c84-118">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-118">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-119">**type**</span><span class="sxs-lookup"><span data-stu-id="d3c84-119">**type**</span></span>                  | <span data-ttu-id="d3c84-120">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-120">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-121">**name**</span><span class="sxs-lookup"><span data-stu-id="d3c84-121">**name**</span></span>                  | <span data-ttu-id="d3c84-122">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-122">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-123">**language**</span><span class="sxs-lookup"><span data-stu-id="d3c84-123">**language**</span></span>              | <span data-ttu-id="d3c84-124">Non</span><span class="sxs-lookup"><span data-stu-id="d3c84-124">No</span></span>       |
|                       | <span data-ttu-id="d3c84-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d3c84-125">**processorArchitecture**</span></span> | <span data-ttu-id="d3c84-126">Non</span><span class="sxs-lookup"><span data-stu-id="d3c84-126">No</span></span>       |
|                       | <span data-ttu-id="d3c84-127">**version**</span><span class="sxs-lookup"><span data-stu-id="d3c84-127">**version**</span></span>               | <span data-ttu-id="d3c84-128">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-128">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="d3c84-129">**publicKeyToken**</span></span>        | <span data-ttu-id="d3c84-130">Non</span><span class="sxs-lookup"><span data-stu-id="d3c84-130">No</span></span>       |
| <span data-ttu-id="d3c84-131">**dépendance**</span><span class="sxs-lookup"><span data-stu-id="d3c84-131">**dependency**</span></span>        |                           | <span data-ttu-id="d3c84-132">Non</span><span class="sxs-lookup"><span data-stu-id="d3c84-132">No</span></span>       |
| <span data-ttu-id="d3c84-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="d3c84-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="d3c84-134">Non</span><span class="sxs-lookup"><span data-stu-id="d3c84-134">No</span></span>       |
| <span data-ttu-id="d3c84-135">**Direction**</span><span class="sxs-lookup"><span data-stu-id="d3c84-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="d3c84-136">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-136">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-137">**oldVersion**</span></span>            | <span data-ttu-id="d3c84-138">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-138">Yes</span></span>      |
|                       | <span data-ttu-id="d3c84-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-139">**newVersion**</span></span>            | <span data-ttu-id="d3c84-140">Oui</span><span class="sxs-lookup"><span data-stu-id="d3c84-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="d3c84-141">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="d3c84-141">File Location</span></span>

<span data-ttu-id="d3c84-142">Les fichiers de configuration du serveur de publication doivent être installés dans le dossier WinSxS.</span><span class="sxs-lookup"><span data-stu-id="d3c84-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="d3c84-143">Ils sont généralement installés en tant que fichiers distincts, mais les fichiers de configuration du serveur de publication peuvent également être inclus en tant que ressource dans une DLL.</span><span class="sxs-lookup"><span data-stu-id="d3c84-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="d3c84-144">Un fichier de configuration d’éditeur ne peut pas être inclus en tant que ressource dans un fichier EXE.</span><span class="sxs-lookup"><span data-stu-id="d3c84-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="d3c84-145">Un fichier EXE peut inclure un [manifeste d’application](application-manifests.md) en tant que ressource.</span><span class="sxs-lookup"><span data-stu-id="d3c84-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="d3c84-146">Syntaxe du nom de fichier</span><span class="sxs-lookup"><span data-stu-id="d3c84-146">File Name Syntax</span></span>

<span data-ttu-id="d3c84-147">Le nom de fichier d’un fichier de configuration d’éditeur possède la *stratégie* de formulaire. *majeure*. *mineure*. *AssemblyName* , où *major* et *Minor* font référence aux parties majeures et secondaires de la [version d’assembly](assembly-versions.md) qui est affectée.</span><span class="sxs-lookup"><span data-stu-id="d3c84-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="d3c84-148">Le *AssemblyName* fait référence au nom de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="d3c84-149">Par exemple, un fichier de configuration d’éditeur pour la version 6,0 de l’assembly Microsoft. Windows. Common-Controls porterait le nom suivant :</span><span class="sxs-lookup"><span data-stu-id="d3c84-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="d3c84-150">Policy. 6.0. Microsoft. Windows. Common-Controls</span><span class="sxs-lookup"><span data-stu-id="d3c84-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="d3c84-151">N’utilisez pas de fichiers de configuration de stratégie pour incrémenter la version majeure ou mineure d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="d3c84-152">Par exemple, ne redirigez pas la version 6.0.0.0 vers 7.0.0.0 ou 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="d3c84-153">Lorsqu’une application fait référence à une version d’assembly, telle que 6.0.0.0, côte à côte vérifie la présence de fichiers de configuration de stratégie avec les versions principales et secondaires spécifiées, par exemple 6,0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="d3c84-154">L’application est ensuite redirigée vers une autre version de l’assembly, par exemple 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="d3c84-155">Si un fichier de configuration d’éditeur incrémente la version majeure ou mineure d’un assembly, la redirection ultérieure de l’assembly peut nécessiter l’émission de plusieurs fichiers de configuration de stratégie.</span><span class="sxs-lookup"><span data-stu-id="d3c84-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="d3c84-156">Éléments</span><span class="sxs-lookup"><span data-stu-id="d3c84-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="d3c84-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**chargeur**</span><span class="sxs-lookup"><span data-stu-id="d3c84-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="d3c84-158">Élément conteneur.</span><span class="sxs-lookup"><span data-stu-id="d3c84-158">A container element.</span></span> <span data-ttu-id="d3c84-159">Son premier sous-élément doit être un **assemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="d3c84-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="d3c84-160">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3c84-160">Required.</span></span>

<span data-ttu-id="d3c84-161">L’élément assembly doit se trouver dans l’espace de noms **urn : schemas-microsoft-com : ASM. v1**.</span><span class="sxs-lookup"><span data-stu-id="d3c84-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="d3c84-162">Les éléments enfants de l’assembly doivent également être dans cet espace de noms, par héritage ou par balisage.</span><span class="sxs-lookup"><span data-stu-id="d3c84-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="d3c84-163">L’élément **assembly** a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d3c84-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="d3c84-164">Attribut</span><span class="sxs-lookup"><span data-stu-id="d3c84-164">Attribute</span></span>           | <span data-ttu-id="d3c84-165">Description</span><span class="sxs-lookup"><span data-stu-id="d3c84-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="d3c84-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-166">**manifestVersion**</span></span> | <span data-ttu-id="d3c84-167">L’attribut **manifestVersion** doit avoir la valeur 1,0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d3c84-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="d3c84-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="d3c84-169">Décrit et identifie de façon unique un assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d3c84-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="d3c84-170">En tant que premier sous-élément d’un élément **assembly** , l’élément **assemblyIdentity** décrit l’assembly côte à côte dont une ou plusieurs de ses dépendances d’assembly ont été modifiées.</span><span class="sxs-lookup"><span data-stu-id="d3c84-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="d3c84-171">Le fichier de configuration du serveur de publication redirige les dépendances de l’assembly identifié.</span><span class="sxs-lookup"><span data-stu-id="d3c84-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="d3c84-172">Par exemple, l' **assemblyIdentity** suivant indique que le fichier de configuration du serveur de publication affecte les dépendances de l’assembly x86 Microsoft. Windows. pop 6.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="d3c84-173">En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit une dépendance d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="d3c84-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="d3c84-174">Le fichier de configuration du serveur de publication reconfigure l’identité de cet assembly côte à côte obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3c84-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="d3c84-175">La modification est spécifiée dans une **bindingRedirect**.</span><span class="sxs-lookup"><span data-stu-id="d3c84-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="d3c84-176">Par exemple, l’état **assemblyIdentity** suivant modifie les dépendances de Microsoft. Windows. SampleAssembly version 2.0.0.0 avec une dépendance sur Microsoft. Windows. SampleAssembly version 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="d3c84-177">L’élément **assemblyIdentity** a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d3c84-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="d3c84-178">Il n’a pas de sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="d3c84-178">It has no sub-elements.</span></span>



| <span data-ttu-id="d3c84-179">Attribut</span><span class="sxs-lookup"><span data-stu-id="d3c84-179">Attribute</span></span>                 | <span data-ttu-id="d3c84-180">Description</span><span class="sxs-lookup"><span data-stu-id="d3c84-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c84-181">**type**</span><span class="sxs-lookup"><span data-stu-id="d3c84-181">**type**</span></span>                  | <span data-ttu-id="d3c84-182">Spécifie le type d’assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-182">Specifies the assembly type.</span></span> <span data-ttu-id="d3c84-183">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3c84-183">Required.</span></span> <span data-ttu-id="d3c84-184">Dans le champ **assemblyIdentity** de l’assembly affecté, la valeur de l’attribut **type** doit être définie sur Win32-Policy.</span><span class="sxs-lookup"><span data-stu-id="d3c84-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="d3c84-185">La valeur Win32-Policy doit être en minuscules.</span><span class="sxs-lookup"><span data-stu-id="d3c84-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="d3c84-186">Dans le champ **assemblyIdentity** de la dépendance de l’assembly en cours de modification, la valeur de l’attribut **type** doit être définie sur Win32.</span><span class="sxs-lookup"><span data-stu-id="d3c84-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="d3c84-187">La valeur Win32 doit être en lettres minuscules.</span><span class="sxs-lookup"><span data-stu-id="d3c84-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="d3c84-188">**name**</span><span class="sxs-lookup"><span data-stu-id="d3c84-188">**name**</span></span>                  | <span data-ttu-id="d3c84-189">Nomme un assembly de manière unique.</span><span class="sxs-lookup"><span data-stu-id="d3c84-189">Uniquely names an assembly.</span></span> <span data-ttu-id="d3c84-190">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3c84-190">Required.</span></span> <span data-ttu-id="d3c84-191">Dans l’objet **assemblyIdentity** de l’assembly affecté, le nom a la *stratégie* de formulaire. *majeure*. *mineure*. *AssemblyName* , où *major* et *Minor* font référence aux parties majeures et secondaires de la version de l' [assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d3c84-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="d3c84-192">Dans l' **assemblyIdentity** pour la dépendance de l’assembly en cours de modification, le nom se présente sous la forme Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="d3c84-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="d3c84-193">Par exemple, Microsoft. Windows. MysampleApp.</span><span class="sxs-lookup"><span data-stu-id="d3c84-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="d3c84-194">**language**</span><span class="sxs-lookup"><span data-stu-id="d3c84-194">**language**</span></span>              | <span data-ttu-id="d3c84-195">Identifie le langage de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="d3c84-196">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d3c84-196">Optional.</span></span> <span data-ttu-id="d3c84-197">Dans l’objet **assemblyIdentity** de l’assembly affecté, si l’assembly est spécifique à une langue, spécifiez le code de langue DHTML.</span><span class="sxs-lookup"><span data-stu-id="d3c84-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="d3c84-198">Si l’assembly est destiné à une utilisation dans le monde entier (langue neutre), omettez cet attribut.</span><span class="sxs-lookup"><span data-stu-id="d3c84-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="d3c84-199">Dans le **assemblyIdentity** pour la dépendance de l’assembly en cours de modification, si l’assembly est spécifique à la langue, spécifiez le code de langue DHTML.</span><span class="sxs-lookup"><span data-stu-id="d3c84-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="d3c84-200">Si l’assembly est destiné à une utilisation mondiale (langue neutre), définissez la valeur sur « \* ».</span><span class="sxs-lookup"><span data-stu-id="d3c84-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="d3c84-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d3c84-201">**processorArchitecture**</span></span> | <span data-ttu-id="d3c84-202">Spécifie le processeur qui exécute l’application.</span><span class="sxs-lookup"><span data-stu-id="d3c84-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d3c84-203">**version**</span><span class="sxs-lookup"><span data-stu-id="d3c84-203">**version**</span></span>               | <span data-ttu-id="d3c84-204">Spécifie la version de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-204">Specifies the assembly version.</span></span> <span data-ttu-id="d3c84-205">Utilisez la syntaxe de version en quatre parties : MMMM. nnnn. oooo. pppp</span><span class="sxs-lookup"><span data-stu-id="d3c84-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="d3c84-206">Obligatoire uniquement dans le **assemblyIdentity** du contexte def.</span><span class="sxs-lookup"><span data-stu-id="d3c84-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="d3c84-207">Ne spécifiez pas l’attribut de version dans le **assemblyIdentity** du contexte de référence.</span><span class="sxs-lookup"><span data-stu-id="d3c84-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d3c84-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="d3c84-208">**publicKeyToken**</span></span>        | <span data-ttu-id="d3c84-209">Chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’assembly est signé.</span><span class="sxs-lookup"><span data-stu-id="d3c84-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="d3c84-210">La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="d3c84-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="d3c84-211">Un publicKeyToken est requis pour tous les assemblys côte à côte partagés.</span><span class="sxs-lookup"><span data-stu-id="d3c84-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="d3c84-212">Le publicKeyToken utilisé pour le fichier de configuration du serveur de publication doit être la même clé que celle utilisée pour l’assembly signé.</span><span class="sxs-lookup"><span data-stu-id="d3c84-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="d3c84-213">Les fichiers de configuration du serveur de publication peuvent être signés à l’aide des mêmes outils que ceux utilisés avec les assemblys. consultez [exemple de signature d’assembly](assembly-signing-example.md) et [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="d3c84-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="d3c84-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dépendance**</span><span class="sxs-lookup"><span data-stu-id="d3c84-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="d3c84-215">Élément conteneur facultatif pour au moins un élément **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="d3c84-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="d3c84-216">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d3c84-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d3c84-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="d3c84-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="d3c84-218">Chaque **dependentAssembly** doit se trouver à l’intérieur d’une seule **dépendance**.</span><span class="sxs-lookup"><span data-stu-id="d3c84-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="d3c84-219">Un **dependentAssembly** n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d3c84-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="d3c84-220">Le premier sous-élément de **dependentAssembly** doit être un **assemblyIdentity** pour l’assembly côte à côte qui est reconfiguré par la configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="d3c84-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d3c84-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**Direction**</span><span class="sxs-lookup"><span data-stu-id="d3c84-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="d3c84-222">L’élément **bindingRedirect** contient des informations de redirection pour la liaison de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d3c84-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="d3c84-223">Cet élément a les attributs répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d3c84-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="d3c84-224">Attribut</span><span class="sxs-lookup"><span data-stu-id="d3c84-224">Attribute</span></span>      | <span data-ttu-id="d3c84-225">Description</span><span class="sxs-lookup"><span data-stu-id="d3c84-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c84-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-226">**oldVersion**</span></span> | <span data-ttu-id="d3c84-227">Spécifie la version de l’assembly qui est substituée et redirigée.</span><span class="sxs-lookup"><span data-stu-id="d3c84-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="d3c84-228">Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="d3c84-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="d3c84-229">Spécifiez une plage de versions par un tiret sans espaces.</span><span class="sxs-lookup"><span data-stu-id="d3c84-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="d3c84-230">Par exemple, 2.14.3.0 ou 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="d3c84-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="d3c84-231">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d3c84-231">Required.</span></span> |
| <span data-ttu-id="d3c84-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="d3c84-232">**newVersion**</span></span> | <span data-ttu-id="d3c84-233">Spécifie la version de l’assembly de remplacement.</span><span class="sxs-lookup"><span data-stu-id="d3c84-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="d3c84-234">Utilisez la syntaxe de version en quatre parties nnnnn. nnnnn. nnnnn. nnnnn.</span><span class="sxs-lookup"><span data-stu-id="d3c84-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3c84-235">Notes</span><span class="sxs-lookup"><span data-stu-id="d3c84-235">Remarks</span></span>

<span data-ttu-id="d3c84-236">Les fichiers de configuration du serveur de publication ne spécifient pas de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d3c84-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="d3c84-237">Notez que les fichiers de stratégie spécifiques à une langue sont distincts du fichier de configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="d3c84-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="d3c84-238">Exemple</span><span class="sxs-lookup"><span data-stu-id="d3c84-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




