---
description: Un fichier de configuration d’éditeur redirige globalement les applications et les assemblys qui dépendent d’une version d’un assembly côte à côte pour utiliser une autre version du même assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Publisher Configuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011336"
---
# <a name="publisher-configuration"></a>Publisher Configuré

Un [fichier de configuration d’éditeur](publisher-configuration-files.md) redirige globalement les applications et les assemblys qui dépendent d’une version d’un assembly côte à côte pour utiliser une autre version du même assembly. Cela permet aux applications et aux assemblys d’utiliser l’assembly mis à jour sans avoir à recréer toutes les applications affectées.

[Publisher fichiers de configuration](publisher-configuration-files.md) peuvent être fournis par le serveur de publication d’un assembly lors de l’émission d’une nouvelle version de l’assembly avec des correctifs de bogues compatibles ou des mises à jour de sécurité. La version mise à jour doit être entièrement à compatibilité descendante. Un fichier de configuration d’éditeur ne doit jamais être utilisé pour ajouter de nouvelles fonctionnalités, sauf si la mise à jour est entièrement rétrocompatible. Publisher fichiers de configuration ne doivent jamais être utilisés pour incrémenter la version majeure ou mineure d’un assembly. Par exemple, ne redirigez pas l’assembly version 6.0.0.0 vers 7.0.0.0 ou 6.1.0.0.

Publisher fichiers de configuration ne doivent être émis que par l’éditeur de l’assembly. Les développeurs d’assemblys doivent signer les assemblys côte à côte partagés et les fichiers de configuration du serveur de publication. Utilisez la même clé pour signer l’assembly et les fichiers de configuration du serveur de publication associés. Publisher fichiers de configuration doivent être signés à l’aide des mêmes outils que ceux utilisés pour les assemblys, consultez [exemple de signature d’assembly](assembly-signing-example.md) et [création de fichiers et catalogues signés](creating-signed-files-and-catalogs.md).

En règle générale, la nouvelle version d’un assembly et le fichier de configuration du serveur de publication associé seront installés dans une mise à jour Service Pack. Publisher fichiers de configuration ne doivent jamais être fournis avec des applications comme un package redistribuable, car l’installation d’un fichier de configuration d’éditeur redirige globalement les assemblys sur le système. Si l’assembly en cours de mise à jour est fourni en tant que redistribuable, le serveur de publication doit fournir les deux éléments suivants.

-   un package de Windows Installer (fichier .msi) qui comprend la nouvelle version de l’assembly avec la configuration du serveur de publication. Cela peut être installé en tant que Service Pack ou QFE, car dans ce cas, le client a choisi de mettre à jour le système de manière globale. Cette version du package ne doit jamais être installée par les applications.
-   un module de fusion Windows Installer (fichier. msm) qui n’intègre que la nouvelle version de l’assembly. Cette version peut être incluse avec les applications.

Les applications nécessitant une version minimale de l’assembly doivent indiquer leur dépendance sur la version minimale, si la version minimale n’est pas disponible sur un système, l’application ne démarrera pas. S’il est disponible en tant que redistribuable, il doit être inclus dans la configuration de l’application.

Par exemple, l’installation du [fichier de configuration](publisher-configuration-files.md) du serveur de publication suivant redirige la liaison à partir de la version 2.0.0.0 de Microsoft. Windows. SampleAssembly vers la version 2.0.1.0. Cela ajoute une nouvelle stratégie nommée 1.1.0.0. Policy, sous% systemDrive% \\ Windows \\ WinSxS \\ stratégies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.

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

L’installation du fichier de configuration du serveur de publication suivant pour le même assembly redirige la liaison à partir de la version 2.0.0.0 de Microsoft. Windows. SampleAssembly vers la version 2.0.3.0. Cela ajoute une autre stratégie, nommée 2.1.0.0. Policy, sous% systemDrive% \\ Windows \\ WinSxS \\ stratégies \\ x86 \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.

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

 

 



