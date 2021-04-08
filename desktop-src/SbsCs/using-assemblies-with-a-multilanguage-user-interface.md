---
description: Si vous souhaitez que les utilisateurs de votre application ou de la DLL principale puissent modifier la langue de l’interface utilisateur, vous devez envisager de placer les ressources linguistiques dans des dll de ressource satellites distinctes.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Utilisation d’assemblys avec une interface utilisateur multilingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750948"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="e4f93-103">Utilisation d’assemblys avec une interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="e4f93-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="e4f93-104">Si vous souhaitez que les utilisateurs de votre application ou de la DLL principale puissent modifier la langue de l’interface utilisateur, vous devez envisager de placer les ressources linguistiques dans des dll de ressource satellites distinctes.</span><span class="sxs-lookup"><span data-stu-id="e4f93-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="e4f93-105">Pour plus d’informations sur l’utilisation des dll de ressource satellites, consultez [MUI (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="e4f93-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="e4f93-106">Chaque DLL satellite contient les ressources d’une langue différente.</span><span class="sxs-lookup"><span data-stu-id="e4f93-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="e4f93-107">La DLL principale peut être fournie en tant qu’assembly et chacune des dll satellites peut être fournie sous la forme d’assemblys satellites distincts.</span><span class="sxs-lookup"><span data-stu-id="e4f93-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="e4f93-108">Dans ce cas, chaque assembly satellite doit avoir son propre manifeste d’assembly auto-descriptif.</span><span class="sxs-lookup"><span data-stu-id="e4f93-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="e4f93-109">Le manifeste de l’assembly satellite ne doit pas décrire de dépendance vis-à-vis d’autres assemblys.</span><span class="sxs-lookup"><span data-stu-id="e4f93-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="e4f93-110">Toute dépendance des assemblys satellites sur d’autres assemblys doit plutôt être décrite dans le manifeste de l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="e4f93-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="e4f93-111">La version [MUI (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) de Windows permet aux utilisateurs de spécifier la langue de l’interface utilisateur en fonction de leurs préférences, à condition que la langue requise ait été ajoutée au système.</span><span class="sxs-lookup"><span data-stu-id="e4f93-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="e4f93-112">Un assembly principal peut prendre en charge plusieurs langues à l’aide de plusieurs assemblys MUI.</span><span class="sxs-lookup"><span data-stu-id="e4f93-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="e4f93-113">Dans ce cas, chaque assembly MUI doit avoir son propre manifeste et toutes les dépendances sur les autres assemblys doivent être décrites uniquement dans le manifeste de l’assembly principal.</span><span class="sxs-lookup"><span data-stu-id="e4f93-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="e4f93-114">Par exemple, proseware. Sample. pop peut être un assembly côte à côte fondamental qui dépend de l’assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="e4f93-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="e4f93-115">Si proseware. Sample. pop utilise MUI pour prendre en charge plusieurs langues, des assemblys MUI distincts peuvent être fournis pour chaque langue.</span><span class="sxs-lookup"><span data-stu-id="e4f93-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="e4f93-116">Chaque assembly MUI doit avoir son propre manifeste décrivant cette DLL de ressource satellite particulière.</span><span class="sxs-lookup"><span data-stu-id="e4f93-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="e4f93-117">Les manifestes de l’assembly MUI ne doivent pas inclure de référence aux dépendances sur d’autres assemblys.</span><span class="sxs-lookup"><span data-stu-id="e4f93-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="e4f93-118">Le manifeste décrivant l’assembly principal, proseware. Sample. pop, doit décrire la dépendance de proseware. Sample. pop sur l’assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="e4f93-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="e4f93-119">Les attributs de l’élément **assemblyIdentity** d’un assembly satellite sont similaires à ceux du manifeste de l’assembly de base.</span><span class="sxs-lookup"><span data-stu-id="e4f93-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="e4f93-120">L’attribut **Name** doit être identique à l’assembly de base, avec l’ajout de « Resources ».</span><span class="sxs-lookup"><span data-stu-id="e4f93-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="e4f93-121">Par exemple, si le nom est « proseware. Tools. orthographique. Runtime-Libraries » dans l’assembly de base, le nom dans l’assembly de ressource serait « proseware. Tools. orthographique. Runtime-Libraries. resources ».</span><span class="sxs-lookup"><span data-stu-id="e4f93-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="e4f93-122">L’attribut **Language** doit identifier la langue de l’assembly de ressource.</span><span class="sxs-lookup"><span data-stu-id="e4f93-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="e4f93-123">L’attribut **file** doit inclure la liste des fichiers qui sont des dll de ressource.</span><span class="sxs-lookup"><span data-stu-id="e4f93-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="e4f93-124">Voici un exemple du manifeste de l’assembly de ressources proseware. Tools. orthographique. Runtime-Libraries.</span><span class="sxs-lookup"><span data-stu-id="e4f93-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="e4f93-125">L’assembly de base décrit une dépendance facultative sur l’assembly de ressource.</span><span class="sxs-lookup"><span data-stu-id="e4f93-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="e4f93-126">Dans cet exemple, si un utilisateur exécute Windows avec les paramètres régionaux définis en allemand, une application qui utilise l’assembly proseware. Tools. orthographique afficherait du texte en allemand.</span><span class="sxs-lookup"><span data-stu-id="e4f93-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
