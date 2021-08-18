---
description: Utilisez la procédure suivante pour développer une nouvelle application, ou mettre à jour une application existante, pour utiliser les assemblys côte à côte disponibles à partir de Microsoft ou d’autres éditeurs d’assembly côte à côte.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Utilisation d’assemblys côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60170dc4873f03dfc17769f91106e02b591e0b1db81695d773a35b392a2c7dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141712"
---
# <a name="using-side-by-side-assemblies"></a>Utilisation d’assemblys côte à côte

Utilisez la procédure suivante pour développer une nouvelle application, ou mettre à jour une application existante, pour utiliser les [assemblys côte à côte](about-side-by-side-assemblies-.md) disponibles à partir de Microsoft ou d’autres éditeurs d’assembly côte à côte. Pour obtenir la liste des assemblys côte à côte actuellement fournis par Microsoft, consultez [assemblys côte à côte pris en charge](supported-microsoft-side-by-side-assemblies.md)par Microsoft. notez que l’application doit être exécutée sur au moins Windows XP pour installer les assemblys en tant qu’assemblys côte à côte. Pour plus d’informations, consultez [instructions relatives à la création d’assemblys côte à côte](guidelines-for-creating-side-by-side-assemblies.md).

**Pour ajouter un assembly côte à côte à une application**

1.  Identifiez les assemblys côte à côte nécessaires à votre application. à partir de Windows XP, ces assemblys côte à côte et leurs manifestes d’assembly sont installés avec le système d’exploitation, mais ils ne sont pas inscrits globalement.
2.  Utilisez un éditeur XML pour créer un [manifeste d’application](application-manifests.md). Consultez l’exemple de manifeste d’application ci-dessous. Pour plus d’informations, consultez [manifestes d’application](application-manifests.md) dans la [référence des fichiers manifeste](manifest-files-reference.md).
3.  Entrez les valeurs d’attribut dans le sous [*-élément assemblyIdentity du contexte de définition*](d-sbscs-gly.md) du manifeste d’application qui définit l’application de façon unique. Pour plus d’informations sur le **assemblyIdentity**-Context def, consultez [manifestes d’application](application-manifests.md).
4.  Si l’assembly contient des assemblys dépendants, entrez des valeurs d’attribut dans les sous [*-éléments AssemblyIdentity du contexte de référence*](r-sbscs-gly.md) correspondants du manifeste de l’application. Pour plus d’informations sur le **assemblyIdentity** du contexte de référence, consultez [manifestes d’application](application-manifests.md).

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  Vous pouvez inclure le manifeste de l’application dans le fichier d’en-tête binaire de l’application.

    Dans ce cas, ajoutez également la ligne suivante au fichier d’en-tête de l’application :

    <dl> Nom de la \_ ressource du manifeste CREATEPROCESS \_ \_ \_ « YourApp.exe. manifest »  
    </dl>

    Vous pouvez également placer un fichier manifeste distinct dans le même répertoire que le fichier exécutable de votre application. Le système d’exploitation charge d’abord le manifeste à partir du système de fichiers, puis vérifie la section de la ressource du fichier exécutable. La version du système de fichiers est prioritaire.

6.  les [assemblys partagés](/windows/desktop/Msi/shared-assemblies) doivent être installés à l’aide de la version 2,0 de [Windows Installer](../msi/windows-installer-portal.md) . créez un package Windows Installer comme décrit dans [comment installer des assemblys Win32 pour le partage côte à côte sur Windows XP ?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).
7.  les [assemblys privés](/windows/desktop/Msi/private-assemblies) peuvent être installés à l’aide de la version 2,0 de [Windows Installer](../msi/windows-installer-portal.md) . créez un package Windows Installer comme décrit dans [comment installer des assemblys Win32 pour l’utilisation privée d’une Application sur Windows XP ?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md). Vous pouvez également utiliser n’importe quel autre programme d’installation pour copier un assembly privé et son manifeste dans le même dossier que le fichier exécutable de l’application.
8.  Testez votre application pour vérifier les résultats. Notez que l’assembly côte à côte ne doit pas être inscrit sur votre ordinateur de test.
9.  déployez votre application ou mettez à jour en tant que package Windows Installer.

## <a name="example-application-manifest"></a>Exemple de manifeste d’application

Voici un exemple de manifeste d’application :

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

 

 
