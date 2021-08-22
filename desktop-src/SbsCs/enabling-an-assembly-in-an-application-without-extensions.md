---
description: Si votre application n’héberge pas de DLL, d’extension, de plug-in ou de panneau de configuration, vous pouvez utiliser la méthode décrite dans cette section pour activer un assembly pour votre application.
ms.assetid: d043ec1b-ac31-45fb-9232-eec42aef4ac3
title: Activation d’un assembly dans une application sans extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6666d7b50775438f0d4a3edd13658e5c18127a21c37ec95e46a873682e6f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142252"
---
# <a name="enabling-an-assembly-in-an-application-without-extensions"></a>Activation d’un assembly dans une application sans extensions

Si votre application n’héberge pas de DLL, d’extension, de plug-in ou de panneau de configuration, vous pouvez utiliser la méthode décrite dans cette section pour activer un assembly pour votre application. Pour plus d’informations sur l’ajout d’un assembly aux applications avec des extensions, consultez [activation d’un assembly dans une application hébergeant une dll, une extension ou le panneau de configuration](enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel.md).

**Pour activer un assembly dans une application sans aucun composant hébergé**

1.  Créez un manifeste qui décrit la dépendance de l’application ou de l’extension sur l’assembly.

    Par exemple, le manifeste pour « YourApplication » peut être créé en copiant l’exemple de manifeste suivant et en remplaçant les valeurs appropriées pour **assemblyIdentity**, **ProcessorArchitecture** et **Description**. Définissez la valeur de **ProcessorArchitecture** sur x86 si vous générez sur une plateforme 32 bits, et sur ia64 si vous générez sur une plateforme 64 bits. L’élément **Description** contient une description d’option de l’application. Pour plus d’informations sur le format du manifeste, consultez [manifestes d’application](application-manifests.md).

    ``` syntax
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="x86"
        name="YourCompanyName.YourDivision.YourApp"
        type="win32"
    />
    <description>Your app description here</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Proseware.Research.SampleAssembly"
                version="6.0.0.0"
                processorArchitecture="X86"
                publicKeyToken="0000000000000000"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

2.  Ajoutez le manifeste à l’application en tant que ressource dans le fichier d’en-tête binaire de l’application. Il n’est pas recommandé d’ajouter le manifeste à l’application en tant que fichier manifeste externe.

    Pour ajouter le manifeste en tant que ressource, créez une ressource dans l’application de type RT \_ ID de manifeste 1. Par exemple, si le nom de l’application est VotreApplication, le fichier d’en-tête de l’application doit contenir les éléments suivants :

    ``` syntax
    #define MANIFEST_RESOURCE_ID 1
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

    Si vous ajoutez plutôt le manifeste en tant que fichier manifeste externe, assurez-vous que l’installation copie le fichier manifeste dans le dossier contenant le fichier exécutable de l’application.

3.  Testez pour vérifier que les assemblys utilisés par l’application fonctionnent correctement dans l’application.

 

 



