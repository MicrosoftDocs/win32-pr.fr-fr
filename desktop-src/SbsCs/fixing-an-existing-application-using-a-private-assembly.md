---
description: à partir de Windows XP, vous pouvez créer un assembly privé et le mettre à la disposition d’une application spécifique.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corriger une application existante à l’aide d’un assembly privé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d1f46ee2f1d80938f3178e03579b2357a26d77727e1490c861cdddff88342a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885269"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a>Résolution d’une application existante à l’aide d’un assembly privé

à partir de Windows XP, vous pouvez créer un assembly privé et le mettre à la disposition d’une application spécifique. Cette fonctionnalité peut être utilisée pour corriger une application qui devient incompatible avec une mise à jour. Il peut s’agir, par exemple, d’une application qui devient incompatible avec la dernière version de MSVCRT.DLL après la mise à niveau du système d’exploitation. dans ce cas, vous n’avez pas la possibilité de remplacer la version du système, car MSVCRT.DLL est un Windows fichier protégé. Plutôt que d’avoir à réécrire l’application pour utiliser la nouvelle version de MSVCRT, vous pouvez créer un assembly privé pour MSVCRT et l’installer dans votre dossier d’application. Notez que tous les composants partagés ne sont pas un candidat approprié pour un assembly côte à côte privé, et que certains composants ont des restrictions de licence concernant l’emplacement d’installation de leurs composants. Le composant doit répondre aux critères d’un composant côte à côte. Demandez à l’éditeur du composant s’il peut fournir un assembly approprié.

Le manifeste de l’assembly privé et le manifeste de l’application doivent tous deux être installés dans le même dossier que l’exécutable de l’application. Lorsque l’application s’exécute, elle consulte le manifeste de l’application et charge la version de MSVCRT qui est privée pour l’application.

Pour cet exemple, l’assembly privé inclut à la fois MSVCRT.DLL et MSVCIRT.DLL comme dans le manifeste d’assembly suivant :

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

Voici un exemple de manifeste d’application possible.

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

 

 



