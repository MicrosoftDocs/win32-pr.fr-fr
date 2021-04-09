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
# <a name="using-winhttp-as-a-side-by-side-assembly"></a>Utilisation de WinHTTP comme assembly côte à côte

Sur Windows Server 2003, WinHTTP est implémenté en tant qu’assembly côte à côte et doit être lié en tant que tel. Notez que cela ne s’applique pas à Windows Vista et versions ultérieures.

## <a name="side-by-side-assemblies"></a>Assemblys côte à côte

À compter de Microsoft Windows XP, un mécanisme d’assemblys côte à côte était fourni pour contrôler la liaison au moment de l’exécution afin d’éviter les conflits de contrôle de version de la bibliothèque de liens dynamiques (DLL). Pour plus d’informations sur les assemblys côte à côte, consultez [à propos des applications isolées et des assemblys côte à côte](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).

Pour utiliser ce mécanisme afin de créer un lien vers la version 5,1 de WinHTTP sur Windows Server 2003, une application doit incorporer un manifeste qui spécifie WinHTTP comme assembly dépendant. Pour plus d’informations sur la façon de procéder, consultez [utilisation d’assemblys côte à côte](/windows/desktop/SbsCs/using-side-by-side-assemblies) .

## <a name="a-sample-winhttp-application-manifest"></a>Exemple de manifeste d’application WinHTTP

L’exemple de manifeste ci-dessous illustre un manifeste d’application qui peut être utilisé pour la liaison à WinHTTP.

Tous les attributs, à l’exception de « type » du « <assembly> <assemblyIdentity> », doivent être modifiés en fonction de votre application. Il en va de même pour le contenu de &lt; l' &gt; élément « Description ».

En outre, assurez-vous que l’attribut « processorArchitecture » de « <dependentAssembly> <assemblyIdentity> » correspond à l’attribut « processorArchitecture » du « <assembly> <assemblyIdentity> ». Ci-dessous, par exemple, les deux ont la valeur « x86 ».

Toutes les valeurs qui ne sont pas spécifiques à votre application doivent prendre les formes indiquées ci-dessous.

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

 

 
