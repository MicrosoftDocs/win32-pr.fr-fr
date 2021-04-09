---
description: À partir de Windows XP, vous pouvez créer un assembly privé et le mettre à la disposition d’une application spécifique.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corriger une application existante à l’aide d’un assembly privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033924"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="762ef-103">Résolution d’une application existante à l’aide d’un assembly privé</span><span class="sxs-lookup"><span data-stu-id="762ef-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="762ef-104">À partir de Windows XP, vous pouvez créer un assembly privé et le mettre à la disposition d’une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="762ef-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="762ef-105">Cette fonctionnalité peut être utilisée pour corriger une application qui devient incompatible avec une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="762ef-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="762ef-106">Il peut s’agir, par exemple, d’une application qui devient incompatible avec la dernière version de MSVCRT.DLL après la mise à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="762ef-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="762ef-107">Dans ce cas, vous n’avez pas la possibilité de remplacer la version du système, car MSVCRT.DLL est un fichier protégé de Windows.</span><span class="sxs-lookup"><span data-stu-id="762ef-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="762ef-108">Plutôt que d’avoir à réécrire l’application pour utiliser la nouvelle version de MSVCRT, vous pouvez créer un assembly privé pour MSVCRT et l’installer dans votre dossier d’application.</span><span class="sxs-lookup"><span data-stu-id="762ef-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="762ef-109">Notez que tous les composants partagés ne sont pas un candidat approprié pour un assembly côte à côte privé, et que certains composants ont des restrictions de licence concernant l’emplacement d’installation de leurs composants.</span><span class="sxs-lookup"><span data-stu-id="762ef-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="762ef-110">Le composant doit répondre aux critères d’un composant côte à côte.</span><span class="sxs-lookup"><span data-stu-id="762ef-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="762ef-111">Demandez à l’éditeur du composant s’il peut fournir un assembly approprié.</span><span class="sxs-lookup"><span data-stu-id="762ef-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="762ef-112">Le manifeste de l’assembly privé et le manifeste de l’application doivent tous deux être installés dans le même dossier que l’exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="762ef-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="762ef-113">Lorsque l’application s’exécute, elle consulte le manifeste de l’application et charge la version de MSVCRT qui est privée pour l’application.</span><span class="sxs-lookup"><span data-stu-id="762ef-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="762ef-114">Pour cet exemple, l’assembly privé inclut à la fois MSVCRT.DLL et MSVCIRT.DLL comme dans le manifeste d’assembly suivant :</span><span class="sxs-lookup"><span data-stu-id="762ef-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="762ef-115">Voici un exemple de manifeste d’application possible.</span><span class="sxs-lookup"><span data-stu-id="762ef-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



