---
title: modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2
description: modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e1fe0972a915d0f13ca3c3f8f52e5dd0559ad9c24e1afd2dd005f4a733373c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882689"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a>modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2

## <a name="platforms"></a>Plateformes

**Clients-** Windows 8.1

**serveurs-** Windows Server 2012 R2

## <a name="description"></a>Description

nous avons apporté des changements significatifs dans la façon dont les api getversion (ex) fonctionnent dans Windows 8.1 en raison de comportements de client indésirables résultant de la façon dont les api getversion (ex) ont été utilisées par le passé.

dans les versions précédentes de Windows, l’appel des api GetVersion (Ex) retournerait la version réelle du système d’exploitation, à moins que le processus n’ait été atténué par un shim de compatibilité des applications pour lui donner une version différente. Cette opération a été effectuée sur une base provisoire et était relativement incomplète en termes de nombre de processus que Microsoft pourrait raisonnablement déchiffrer dans une version. De nombreuses applications sont tombées en raison de fissures, car elles n’ont pas été corrigées en raison de vérifications de version mal conçues.

La vérification de la version permet d’avertir l’utilisateur que l’application doit s’exécuter sur une version plus récente du système d’exploitation. toutefois, en raison de mauvaises vérifications, les applications signalent souvent de manière incorrecte qu’elles devaient être exécutées sur Windows XP ou version ultérieure, ce qui, bien sûr, est le système d’exploitation le plus récent. Plus souvent, le système d’exploitation le plus récent exécute l’application sans aucun problème, si ce n’est pas le cas pour ces vérifications.

## <a name="manifestation"></a>Manifestation

dans Windows 8.1, les api GetVersion (Ex) sont dépréciées. cela signifie que même si vous pouvez toujours appeler ces fonctions API, si votre application ne cible pas spécifiquement Windows 8.1, les fonctions retournent la version Windows 8 (6,2).

## <a name="solution"></a>Solution

### <a name="adding-an-app-manifest"></a>Ajout d’un manifeste d’application

pour que votre application cible Windows 8.1, vous devez inclure un [manifeste d’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application. ensuite, dans la [section **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste, vous devez ajouter un élémentos **&lt; pris en charge &gt;** pour chaque version de Windows que vous souhaitez déclarer prise en charge par votre application.

l’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista à Windows 8.1 :

```XML
<!-- example.exe.manifest -->
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
    <assemblyIdentity
        type="win32"
        name="Contoso.ExampleApplication.ExampleBinary"
        version="1.2.3.4"
        processorArchitecture="x86"
    />
    <description>Contoso Example Application</description>
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/> <!-- * ADD THIS LINE * -->
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
</assembly>
```

La ligne ci-dessus indiquée `* ADD THIS LINE *` indique comment cibler avec précision votre application pour Windows 8.1.

la déclaration de la prise en charge des Windows 8.1 dans le manifeste de votre application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.

### <a name="using-versionhelpers-instead-of-getversionex"></a>Utilisation de VersionHelpers au lieu de GetVersion (ex)

Windows 8.1 introduit de nouvelles fonctions API de remplacement pour GetVersion (Ex), connu sous le nom de VersionHelpers. Ils sont extrêmement faciles à utiliser ; tout ce que vous avez à faire est `#include <VersionHelpers.h>` . les fonctions inline disponibles dans le fichier d’en-tête VersionHelpers. h permettent à votre code de demander si le système d’exploitation est une version donnée de Windows ou version ultérieure.

**Exemple** par exemple, si votre application nécessite Windows 8 ou version ultérieure, utilisez le test suivant :

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

Les fonctions de l’API VersionHelper disponibles sont les suivantes :

```c
#define VERSIONHELPERAPI FORCEINLINE BOOL
VERSIONHELPERAPI IsWindowsXPOrGreater();
VERSIONHELPERAPI IsWindowsXPSP1OrGreater();
VERSIONHELPERAPI IsWindowsXPSP2OrGreater();
VERSIONHELPERAPI IsWindowsXPSP3OrGreater();
VERSIONHELPERAPI IsWindowsVistaOrGreater();
VERSIONHELPERAPI IsWindowsVistaSP1OrGreater();
VERSIONHELPERAPI IsWindowsVistaSP2OrGreater();
VERSIONHELPERAPI IsWindows7OrGreater();
VERSIONHELPERAPI IsWindows7SP1OrGreater();
VERSIONHELPERAPI IsWindows8OrGreater();
VERSIONHELPERAPI IsWindows8Point1OrGreater();
VERSIONHELPERAPI IsWindowsServer();
```

Ils retournent la valeur TRUE ou FALSe en fonction de la question que vous demandez, et vous devez uniquement définir le système d’exploitation de niveau minimal que vous prenez en charge.

## <a name="resources"></a>Ressources

-   [compatibilité des applications Shared Computer Toolkit téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   [Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))
-   [API VersionHelpers](../sysinfo/version-helper-apis.md)