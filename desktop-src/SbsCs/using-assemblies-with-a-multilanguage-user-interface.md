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
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a>Utilisation d’assemblys avec une interface utilisateur multilingue

Si vous souhaitez que les utilisateurs de votre application ou de la DLL principale puissent modifier la langue de l’interface utilisateur, vous devez envisager de placer les ressources linguistiques dans des dll de ressource satellites distinctes. Pour plus d’informations sur l’utilisation des dll de ressource satellites, consultez [MUI (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface).

Chaque DLL satellite contient les ressources d’une langue différente. La DLL principale peut être fournie en tant qu’assembly et chacune des dll satellites peut être fournie sous la forme d’assemblys satellites distincts. Dans ce cas, chaque assembly satellite doit avoir son propre manifeste d’assembly auto-descriptif. Le manifeste de l’assembly satellite ne doit pas décrire de dépendance vis-à-vis d’autres assemblys. Toute dépendance des assemblys satellites sur d’autres assemblys doit plutôt être décrite dans le manifeste de l’assembly principal.

La version [MUI (Multilanguage User Interface)](/windows/desktop/Intl/multilingual-user-interface) de Windows permet aux utilisateurs de spécifier la langue de l’interface utilisateur en fonction de leurs préférences, à condition que la langue requise ait été ajoutée au système. Un assembly principal peut prendre en charge plusieurs langues à l’aide de plusieurs assemblys MUI. Dans ce cas, chaque assembly MUI doit avoir son propre manifeste et toutes les dépendances sur les autres assemblys doivent être décrites uniquement dans le manifeste de l’assembly principal.

Par exemple, proseware. Sample. pop peut être un assembly côte à côte fondamental qui dépend de l’assembly proseware. Research. SampleAssembly. Si proseware. Sample. pop utilise MUI pour prendre en charge plusieurs langues, des assemblys MUI distincts peuvent être fournis pour chaque langue. Chaque assembly MUI doit avoir son propre manifeste décrivant cette DLL de ressource satellite particulière. Les manifestes de l’assembly MUI ne doivent pas inclure de référence aux dépendances sur d’autres assemblys. Le manifeste décrivant l’assembly principal, proseware. Sample. pop, doit décrire la dépendance de proseware. Sample. pop sur l’assembly proseware. Research. SampleAssembly.

Les attributs de l’élément **assemblyIdentity** d’un assembly satellite sont similaires à ceux du manifeste de l’assembly de base. L’attribut **Name** doit être identique à l’assembly de base, avec l’ajout de « Resources ». Par exemple, si le nom est « proseware. Tools. orthographique. Runtime-Libraries » dans l’assembly de base, le nom dans l’assembly de ressource serait « proseware. Tools. orthographique. Runtime-Libraries. resources ». L’attribut **Language** doit identifier la langue de l’assembly de ressource. L’attribut **file** doit inclure la liste des fichiers qui sont des dll de ressource.

Voici un exemple du manifeste de l’assembly de ressources proseware. Tools. orthographique. Runtime-Libraries.

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

L’assembly de base décrit une dépendance facultative sur l’assembly de ressource. Dans cet exemple, si un utilisateur exécute Windows avec les paramètres régionaux définis en allemand, une application qui utilise l’assembly proseware. Tools. orthographique afficherait du texte en allemand.

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

 

 
