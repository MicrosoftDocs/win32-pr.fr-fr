---
description: Si votre application héberge une DLL, une extension, un plug-in ou un panneau de configuration tiers, vous souhaiterez peut-être activer un assembly dans votre application&\# 8212 ; sans activer également cet assembly pour les composants hébergés.
ms.assetid: 832957ca-82fc-4600-b469-512621dde921
title: Activation d’un assembly dans une application hébergeant une DLL, une extension ou un panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ac528c10d7ca0de903c6b132e0349c16061d63f121c390483458b4ef422d66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885539"
---
# <a name="enabling-an-assembly-in-an-application-hosting-a-dll-extension-or-control-panel"></a>Activation d’un assembly dans une application hébergeant une DLL, une extension ou un panneau de configuration

Si votre application héberge une DLL tierce, une extension, un plug-in ou un panneau de configuration, vous pouvez activer un assembly dans votre application, sans activer également cet assembly pour les composants hébergés. Cela peut être le cas lorsqu’un composant hébergé nécessite des modifications de code pour utiliser l’assembly. En tant que développeur d’applications, vous ne pourrez peut-être pas modifier ces composants tiers. Dans ce cas, vous devez suivre la procédure décrite dans cette section afin que votre application puisse utiliser l’assembly sans affecter les composants hébergés.

-   Pour activer un assembly dans une application sans affecter les dll, extensions, plug-ins et panneaux de contrôle hébergés, un manifeste qui décrit la dépendance de l’application sur l’assembly doit être inclus dans l’application en tant que ressource. Les composants hébergés qui ne sont pas activés avec l’assembly ne doivent pas inclure de manifestes décrivant cette dépendance.
-   Pour activer un assembly dans une application et ses dll, extensions, plug-ins ou panneaux de contrôle hébergés, incluez les manifestes en tant que ressources dans l’application et ses composants hébergés. Les manifestes inclus dans l’application et dans les composants hébergés doivent chacun décrire une dépendance sur l’assembly. En général, le développeur d’applications ajoute un manifeste à l’application et le développeur de composants hébergés ajoute un manifeste à la DLL, à l’extension, au plug-in ou au panneau de configuration.

La méthode suivante peut être utilisée pour ajouter un manifeste à une application ou à un composant hébergé qui est une DLL, une extension, un plug-in ou un panneau de configuration.

**Pour activer un assembly dans une application ou un composant hébergé.**

1.  Créez un manifeste qui décrit la dépendance de l’application ou de l’extension sur l’assembly.

    Par exemple, le manifeste pour « YourApplication » peut être créé en copiant l’exemple de manifeste suivant et en remplaçant les valeurs appropriées pour **assemblyIdentity**, **ProcessorArchitecture** et **Description**. Définissez la valeur de **ProcessorArchitecture** sur x86 si vous générez sur une plateforme 32 bits et sur ia64 si vous générez sur une plateforme 64 bits. L’élément **Description** contient une description d’option de l’application. Pour plus d’informations sur le format du manifeste, consultez [manifestes d’application](application-manifests.md).

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

2.  Créez une ressource dans l’application ou l’extension de type RT \_ ID de manifeste 2.

    Par exemple, si le nom de l’application est VotreApplication, l’application doit contenir les éléments suivants :

    ``` syntax
    #define MANIFEST_RESOURCE_ID 2
    MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.manifest"
    ```

3.  compilez l’application avec l’indicateur compatible-DISOLATION \_ \_ , ou insérez cette instruction avant l' \# instruction include « Windows. h ». Dans le cas d’une application avec plusieurs modules, l’indicateur de prise en charge de DISOLATION \_ \_ est requis sur tous les modules.

    ``` syntax
    #define ISOLATION_AWARE_ENABLED 1
    ```

4.  Effectuez un test pour vérifier que les assemblys utilisés par l’application fonctionnent correctement dans l’application et le composant hébergé.

Pour plus d’informations sur l’ajout d’un assembly aux applications sans extensions, consultez [activation d’un assembly dans une application sans extensions](enabling-an-assembly-in-an-application-without-extensions.md).

 

 



