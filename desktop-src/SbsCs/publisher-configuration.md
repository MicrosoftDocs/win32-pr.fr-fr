---
description: Un fichier de configuration d’éditeur redirige globalement les applications et les assemblys qui dépendent d’une version d’un assembly côte à côte pour utiliser une autre version du même assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Configuration du serveur de publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210041"
---
# <a name="publisher-configuration"></a><span data-ttu-id="b9b92-103">Configuration du serveur de publication</span><span class="sxs-lookup"><span data-stu-id="b9b92-103">Publisher Configuration</span></span>

<span data-ttu-id="b9b92-104">Un [fichier de configuration d’éditeur](publisher-configuration-files.md) redirige globalement les applications et les assemblys qui dépendent d’une version d’un assembly côte à côte pour utiliser une autre version du même assembly.</span><span class="sxs-lookup"><span data-stu-id="b9b92-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="b9b92-105">Cela permet aux applications et aux assemblys d’utiliser l’assembly mis à jour sans avoir à recréer toutes les applications affectées.</span><span class="sxs-lookup"><span data-stu-id="b9b92-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="b9b92-106">Les [fichiers de configuration](publisher-configuration-files.md) du serveur de publication peuvent être fournis par le serveur de publication d’un assembly lors de l’émission d’une nouvelle version de l’assembly avec des correctifs de bogues compatibles ou des mises à jour de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b9b92-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="b9b92-107">La version mise à jour doit être entièrement à compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="b9b92-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="b9b92-108">Un fichier de configuration d’éditeur ne doit jamais être utilisé pour ajouter de nouvelles fonctionnalités, sauf si la mise à jour est entièrement rétrocompatible.</span><span class="sxs-lookup"><span data-stu-id="b9b92-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="b9b92-109">Les fichiers de configuration du serveur de publication ne doivent jamais être utilisés pour incrémenter la version majeure ou mineure d’un assembly.</span><span class="sxs-lookup"><span data-stu-id="b9b92-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="b9b92-110">Par exemple, ne redirigez pas l’assembly version 6.0.0.0 vers 7.0.0.0 ou 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="b9b92-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="b9b92-111">Les fichiers de configuration du serveur de publication doivent être émis uniquement par le serveur de publication de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="b9b92-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="b9b92-112">Les développeurs d’assemblys doivent signer les assemblys côte à côte partagés et les fichiers de configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b9b92-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="b9b92-113">Utilisez la même clé pour signer l’assembly et les fichiers de configuration du serveur de publication associés.</span><span class="sxs-lookup"><span data-stu-id="b9b92-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="b9b92-114">Les fichiers de configuration du serveur de publication doivent être signés à l’aide des mêmes outils que ceux utilisés pour les assemblys. consultez [exemple de signature d’assembly](assembly-signing-example.md) et [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="b9b92-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="b9b92-115">En règle générale, la nouvelle version d’un assembly et le fichier de configuration du serveur de publication associé seront installés dans une mise à jour Service Pack.</span><span class="sxs-lookup"><span data-stu-id="b9b92-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="b9b92-116">Les fichiers de configuration du serveur de publication ne doivent jamais être fournis avec des applications comme un package redistribuable, car l’installation d’un fichier de configuration d’éditeur redirige globalement les assemblys sur le système.</span><span class="sxs-lookup"><span data-stu-id="b9b92-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="b9b92-117">Si l’assembly en cours de mise à jour est fourni en tant que redistribuable, le serveur de publication doit fournir les deux éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="b9b92-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="b9b92-118">Un package Windows Installer (fichier. msi) qui comprend la nouvelle version de l’assembly avec la configuration du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="b9b92-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="b9b92-119">Cela peut être installé en tant que Service Pack ou QFE, car dans ce cas, le client a choisi de mettre à jour le système de manière globale.</span><span class="sxs-lookup"><span data-stu-id="b9b92-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="b9b92-120">Cette version du package ne doit jamais être installée par les applications.</span><span class="sxs-lookup"><span data-stu-id="b9b92-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="b9b92-121">Un module de fusion Windows Installer (fichier. msm) qui n’intègre que la nouvelle version de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="b9b92-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="b9b92-122">Cette version peut être incluse avec les applications.</span><span class="sxs-lookup"><span data-stu-id="b9b92-122">This version may be included with applications.</span></span>

<span data-ttu-id="b9b92-123">Les applications nécessitant une version minimale de l’assembly doivent indiquer leur dépendance sur la version minimale, si la version minimale n’est pas disponible sur un système, l’application ne démarrera pas.</span><span class="sxs-lookup"><span data-stu-id="b9b92-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="b9b92-124">S’il est disponible en tant que redistribuable, il doit être inclus dans la configuration de l’application.</span><span class="sxs-lookup"><span data-stu-id="b9b92-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="b9b92-125">Par exemple, l’installation du [fichier de configuration](publisher-configuration-files.md) du serveur de publication suivant redirige la liaison de la version 2.0.0.0 de Microsoft. Windows. SampleAssembly vers la version 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="b9b92-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="b9b92-126">Cela ajoute une nouvelle stratégie nommée 1.1.0.0. Policy, sous% systemDrive% \\ Windows \\ WinSxS \\ stratégies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="b9b92-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="b9b92-127">L’installation du fichier de configuration du serveur de publication suivant pour le même assembly redirige la liaison de la version 2.0.0.0 de Microsoft. Windows. SampleAssembly vers la version 2.0.3.0.</span><span class="sxs-lookup"><span data-stu-id="b9b92-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="b9b92-128">Cela ajoute une autre stratégie, nommée 2.1.0.0. Policy, sous% systemDrive% \\ Windows \\ WinSxS \\ Policies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="b9b92-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



