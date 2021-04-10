---
description: Utilisez la procédure suivante pour développer une nouvelle application, ou mettre à jour une application existante, pour utiliser les assemblys côte à côte disponibles à partir de Microsoft ou d’autres éditeurs d’assembly côte à côte.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Utilisation d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862330"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="a5c84-103">Utilisation d’assemblys côte à côte</span><span class="sxs-lookup"><span data-stu-id="a5c84-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="a5c84-104">Utilisez la procédure suivante pour développer une nouvelle application, ou mettre à jour une application existante, pour utiliser les [assemblys côte à côte](about-side-by-side-assemblies-.md) disponibles à partir de Microsoft ou d’autres éditeurs d’assembly côte à côte.</span><span class="sxs-lookup"><span data-stu-id="a5c84-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="a5c84-105">Pour obtenir la liste des assemblys côte à côte actuellement fournis par Microsoft, consultez [assemblys côte à côte pris en charge](supported-microsoft-side-by-side-assemblies.md)par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a5c84-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="a5c84-106">Notez que l’application doit être exécutée sur au moins Windows XP pour installer les assemblys en tant qu’assemblys côte à côte.</span><span class="sxs-lookup"><span data-stu-id="a5c84-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="a5c84-107">Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="a5c84-108">**Pour ajouter un assembly côte à côte à une application**</span><span class="sxs-lookup"><span data-stu-id="a5c84-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="a5c84-109">Identifiez les assemblys côte à côte nécessaires à votre application.</span><span class="sxs-lookup"><span data-stu-id="a5c84-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="a5c84-110">À compter de Windows XP, ces assemblys côte à côte et leurs manifestes d’assembly sont installés avec le système d’exploitation, mais ils ne sont pas inscrits globalement.</span><span class="sxs-lookup"><span data-stu-id="a5c84-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="a5c84-111">Utilisez un éditeur XML pour créer un [manifeste d’application](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="a5c84-112">Consultez l’exemple de manifeste d’application ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="a5c84-112">See the example application manifest below.</span></span> <span data-ttu-id="a5c84-113">Pour plus d’informations, consultez [manifestes d’application](application-manifests.md) dans la [référence des fichiers manifeste](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="a5c84-114">Entrez les valeurs d’attribut dans le sous [*-élément assemblyIdentity du contexte de définition*](d-sbscs-gly.md) du manifeste d’application qui définit l’application de façon unique.</span><span class="sxs-lookup"><span data-stu-id="a5c84-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="a5c84-115">Pour plus d’informations sur le **assemblyIdentity**-Context def, consultez [manifestes d’application](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="a5c84-116">Si l’assembly contient des assemblys dépendants, entrez des valeurs d’attribut dans les sous [*-éléments AssemblyIdentity du contexte de référence*](r-sbscs-gly.md) correspondants du manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="a5c84-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="a5c84-117">Pour plus d’informations sur le **assemblyIdentity** du contexte de référence, consultez [manifestes d’application](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="a5c84-118">Vous pouvez inclure le manifeste de l’application dans le fichier d’en-tête binaire de l’application.</span><span class="sxs-lookup"><span data-stu-id="a5c84-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="a5c84-119">Dans ce cas, ajoutez également la ligne suivante au fichier d’en-tête de l’application :</span><span class="sxs-lookup"><span data-stu-id="a5c84-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="a5c84-120">Nom de la \_ ressource du manifeste CREATEPROCESS \_ \_ \_ « YourApp.exe. manifest »</span><span class="sxs-lookup"><span data-stu-id="a5c84-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="a5c84-121">Vous pouvez également placer un fichier manifeste distinct dans le même répertoire que le fichier exécutable de votre application.</span><span class="sxs-lookup"><span data-stu-id="a5c84-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="a5c84-122">Le système d’exploitation charge d’abord le manifeste à partir du système de fichiers, puis vérifie la section de la ressource du fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="a5c84-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="a5c84-123">La version du système de fichiers est prioritaire.</span><span class="sxs-lookup"><span data-stu-id="a5c84-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="a5c84-124">Les [assemblys partagés](/windows/desktop/Msi/shared-assemblies) doivent être installés à l’aide de la version 2,0 de [Windows Installer](../msi/windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a5c84-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="a5c84-125">Créez un package Windows Installer comme décrit dans [Comment installer des assemblys Win32 pour le partage côte à côte sur Windows XP ?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="a5c84-126">Les [assemblys privés](/windows/desktop/Msi/private-assemblies) peuvent être installés à l’aide de la version 2,0 de [Windows Installer](../msi/windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a5c84-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="a5c84-127">Créez un package Windows Installer comme décrit dans [Comment installer des assemblys Win32 pour l’utilisation privée d’une application sur Windows XP ?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="a5c84-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="a5c84-128">Vous pouvez également utiliser n’importe quel autre programme d’installation pour copier un assembly privé et son manifeste dans le même dossier que le fichier exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="a5c84-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="a5c84-129">Testez votre application pour vérifier les résultats.</span><span class="sxs-lookup"><span data-stu-id="a5c84-129">Test your application to ensure the results.</span></span> <span data-ttu-id="a5c84-130">Notez que l’assembly côte à côte ne doit pas être inscrit sur votre ordinateur de test.</span><span class="sxs-lookup"><span data-stu-id="a5c84-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="a5c84-131">Déployez votre application ou mettez à jour en tant que package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a5c84-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="a5c84-132">Exemple de manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="a5c84-132">Example Application Manifest</span></span>

<span data-ttu-id="a5c84-133">Voici un exemple de manifeste d’application :</span><span class="sxs-lookup"><span data-stu-id="a5c84-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
