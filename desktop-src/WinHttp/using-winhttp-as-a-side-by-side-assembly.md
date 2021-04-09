---
description: Sur Windows Server 2003, WinHTTP est implémenté en tant qu’assembly côte à côte et doit être lié en tant que tel. Notez que cela ne s’applique pas à Windows Vista et versions ultérieures.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Utilisation de WinHTTP comme assembly côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751509"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="157b6-104">Utilisation de WinHTTP comme assembly côte à côte</span><span class="sxs-lookup"><span data-stu-id="157b6-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="157b6-105">Sur Windows Server 2003, WinHTTP est implémenté en tant qu’assembly côte à côte et doit être lié en tant que tel.</span><span class="sxs-lookup"><span data-stu-id="157b6-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="157b6-106">Notez que cela ne s’applique pas à Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="157b6-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="157b6-107">Assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="157b6-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="157b6-108">À compter de Microsoft Windows XP, un mécanisme d’assemblys côte à côte était fourni pour contrôler la liaison au moment de l’exécution afin d’éviter les conflits de contrôle de version de la bibliothèque de liens dynamiques (DLL).</span><span class="sxs-lookup"><span data-stu-id="157b6-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="157b6-109">Pour plus d’informations sur les assemblys côte à côte, consultez [à propos des applications isolées et des assemblys côte à côte](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span><span class="sxs-lookup"><span data-stu-id="157b6-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="157b6-110">Pour utiliser ce mécanisme afin de créer un lien vers la version 5,1 de WinHTTP sur Windows Server 2003, une application doit incorporer un manifeste qui spécifie WinHTTP comme assembly dépendant.</span><span class="sxs-lookup"><span data-stu-id="157b6-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="157b6-111">Pour plus d’informations sur la façon de procéder, consultez [utilisation d’assemblys côte à côte](/windows/desktop/SbsCs/using-side-by-side-assemblies) .</span><span class="sxs-lookup"><span data-stu-id="157b6-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="157b6-112">Exemple de manifeste d’application WinHTTP</span><span class="sxs-lookup"><span data-stu-id="157b6-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="157b6-113">L’exemple de manifeste ci-dessous illustre un manifeste d’application qui peut être utilisé pour la liaison à WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="157b6-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="157b6-114">Tous les attributs, à l’exception de « type » du « <assembly> <assemblyIdentity> », doivent être modifiés en fonction de votre application.</span><span class="sxs-lookup"><span data-stu-id="157b6-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="157b6-115">Il en va de même pour le contenu de &lt; l' &gt; élément « Description ».</span><span class="sxs-lookup"><span data-stu-id="157b6-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="157b6-116">En outre, assurez-vous que l’attribut « processorArchitecture » de « <dependentAssembly> <assemblyIdentity> » correspond à l’attribut « processorArchitecture » du « <assembly> <assemblyIdentity> ».</span><span class="sxs-lookup"><span data-stu-id="157b6-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="157b6-117">Ci-dessous, par exemple, les deux ont la valeur « x86 ».</span><span class="sxs-lookup"><span data-stu-id="157b6-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="157b6-118">Toutes les valeurs qui ne sont pas spécifiques à votre application doivent prendre les formes indiquées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="157b6-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
