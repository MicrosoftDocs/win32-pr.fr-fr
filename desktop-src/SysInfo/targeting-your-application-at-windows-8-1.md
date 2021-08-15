---
description: dans Windows 8.1 et Windows 10, les fonctions GetVersion et GetVersionEx sont dépréciées.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Ciblage de votre application pour Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e045dff2f46501c4715e2ffebe484dfeadb3aa9f276d79c7e7c1afdbec6ba7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763110"
---
# <a name="targeting-your-application-for-windows"></a>Ciblage de votre application pour Windows

dans Windows 8.1 et Windows 10, les fonctions [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) et [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) sont dépréciées. dans Windows 10, la fonction [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) a également été dépréciée. bien que vous puissiez toujours appeler les fonctions déconseillées, si votre application ne cible pas spécifiquement Windows 8.1 ou Windows 10, les fonctions retournent la version Windows 8 (6,2).

> [!Note]  
> [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)et les [fonctions d’assistance de version](version-helper-apis.md) concernent uniquement les applications de bureau. les applications de Windows universelles peuvent utiliser la propriété [**AnalyticsInfo. VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) pour les journaux de diagnostic et de télémétrie.

pour que votre application cible Windows 8.1 ou Windows 10, vous devez inclure un [manifeste d’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application. ensuite, dans la [section **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste, vous devez ajouter un élémentos **&lt; pris en charge &gt;** pour chaque version de Windows que vous souhaitez déclarer prise en charge par votre application.

l’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista à Windows 10 :

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
            <!-- Windows 10 -->
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/>
            <!-- Windows 8.1 -->
            <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
            <!-- Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
            <!-- Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
            <!-- Windows Vista -->
            <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        </application>
    </compatibility>
    <trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
        <security>
            <requestedPrivileges>
                <!--
                  UAC settings:
                  - app should run at same integrity level as calling process
                  - app does not need to manipulate windows belonging to
                    higher-integrity-level processes
                  -->
                <requestedExecutionLevel
                    level="asInvoker"
                    uiAccess="false"
                />   
            </requestedPrivileges>
        </security>
    </trustInfo>
</assembly>
```

la déclaration de la prise en charge de Windows 8.1 ou Windows 10 dans le manifeste de votre application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.

Le manifeste d’application ci-dessus comprend également une [section **&lt; &gt; trustInfo**](/previous-versions/bb756929(v=msdn.10)), qui spécifie la façon dont le système doit le traiter en ce qui concerne le [contrôle de compte d’utilisateur (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works). L’ajout de **trustInfo** n’est pas essentiel, mais il est vivement recommandé, même si votre application n’a pas besoin d’un comportement spécifique au contrôle de compte d’utilisateur. en particulier, si vous n’ajoutez pas de **trustInfo** , les versions 32 bits x86 de votre application seront soumises à la [virtualisation de fichiers UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), ce qui permet aux écritures sur des dossiers privilégiés par l’administrateur comme les dossiers système Windows de réussir quand ils échouent, mais les redirige vers un dossier « VirtualStore » spécifique à l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention de la version du système](getting-the-system-version.md)
</dt> <dt>

[Fonctions d’assistance de version](version-helper-apis.md)
</dt> <dt>

[OSVERSIONINFO](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[OSVERSIONINFOEX](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
