---
description: Dans Windows 8.1 et Windows 10, les fonctions GetVersion et GetVersionEx ont été dépréciées.
ms.assetid: E7A1A16A-95B3-4B45-81AD-A19E33F15AE4
title: Ciblage de votre application pour Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0bd280451e5a1dd6a5162dd7b9ccb34495d22be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320358"
---
# <a name="targeting-your-application-for-windows"></a><span data-ttu-id="f54d0-103">Ciblage de votre application pour Windows</span><span class="sxs-lookup"><span data-stu-id="f54d0-103">Targeting your application for Windows</span></span>

<span data-ttu-id="f54d0-104">Dans Windows 8.1 et Windows 10, les fonctions [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) et [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) ont été dépréciées.</span><span class="sxs-lookup"><span data-stu-id="f54d0-104">In Windows 8.1 and Windows 10, the [**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion) and [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) functions have been deprecated.</span></span> <span data-ttu-id="f54d0-105">Dans Windows 10, la fonction [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) a également été dépréciée.</span><span class="sxs-lookup"><span data-stu-id="f54d0-105">In Windows 10, the [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa) function has also been deprecated.</span></span> <span data-ttu-id="f54d0-106">Bien que vous puissiez toujours appeler les fonctions déconseillées, si votre application ne cible pas spécifiquement Windows 8.1 ou Windows 10, les fonctions retournent la version de Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="f54d0-106">While you can still call the deprecated functions, if your application does not specifically target Windows 8.1 or Windows 10, the functions will return the Windows 8 version (6.2).</span></span>

> [!Note]  
> <span data-ttu-id="f54d0-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)et les [fonctions d’assistance de version](version-helper-apis.md) concernent uniquement les applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="f54d0-107">[**GetVersion**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversion), [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa), [**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa), and the [Version Helper functions](version-helper-apis.md) are for desktop apps only.</span></span> <span data-ttu-id="f54d0-108">Les applications Windows universelles peuvent utiliser la propriété [**AnalyticsInfo. VERSIONINFO**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) pour les journaux de diagnostic et de télémétrie.</span><span class="sxs-lookup"><span data-stu-id="f54d0-108">Universal Windows apps can use the [**AnalyticsInfo.VersionInfo**](/uwp/api/windows.system.profile.analyticsinfo.versioninfo) property for telemetry and diagnostic logs.</span></span>

<span data-ttu-id="f54d0-109">Pour que votre application cible Windows 8.1 ou Windows 10, vous devez inclure un [manifeste d’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="f54d0-109">In order for your app to target Windows 8.1 or Windows 10, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="f54d0-110">Ensuite, dans la [section **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste, vous devez ajouter un élémentos **&lt; pris en charge &gt;** pour chaque version de Windows que vous souhaitez déclarer prise en charge par votre application.</span><span class="sxs-lookup"><span data-stu-id="f54d0-110">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="f54d0-111">L’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista vers Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="f54d0-111">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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

<span data-ttu-id="f54d0-112">La déclaration de la prise en charge de Windows 8.1 ou de Windows 10 dans votre manifeste d’application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.</span><span class="sxs-lookup"><span data-stu-id="f54d0-112">Declaring support for Windows 8.1 or Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

<span data-ttu-id="f54d0-113">Le manifeste d’application ci-dessus comprend également une [section **&lt; &gt; trustInfo**](/previous-versions/bb756929(v=msdn.10)), qui spécifie la façon dont le système doit le traiter en ce qui concerne le [contrôle de compte d’utilisateur (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span><span class="sxs-lookup"><span data-stu-id="f54d0-113">The above app manifest also includes a [**&lt;trustInfo&gt;** section](/previous-versions/bb756929(v=msdn.10)), which specifies how the system should treat it with respect to [User Account Control (UAC)](/windows/security/identity-protection/user-account-control/how-user-account-control-works).</span></span> <span data-ttu-id="f54d0-114">L’ajout de **trustInfo** n’est pas essentiel, mais il est vivement recommandé, même si votre application n’a pas besoin d’un comportement spécifique au contrôle de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f54d0-114">Adding **trustInfo** isn't essential, but it is highly recommended, even when your app doesn't need any particular UAC-related behavior.</span></span> <span data-ttu-id="f54d0-115">En particulier, si vous n’ajoutez pas de **trustInfo** , les versions 32 bits x86 de votre application seront soumises à [la virtualisation de fichiers UAC](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), qui permet aux écritures sur des dossiers privilégiés par l’administrateur comme les dossiers système Windows de réussir quand ils échouent, mais les redirige vers un dossier « VirtualStore » spécifique à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f54d0-115">In particular, if you don't add **trustInfo** at all, then 32-bit x86 versions of your app will be subject to [UAC file virtualization](/windows/security/identity-protection/user-account-control/how-user-account-control-works#virtualization), which allows writes to administrator-privileged folders like the Windows system folders to succeed when they would otherwise fail, but redirects them to a user-specific "VirtualStore" folder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f54d0-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f54d0-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f54d0-117">Obtention de la version du système</span><span class="sxs-lookup"><span data-stu-id="f54d0-117">Getting the system version</span></span>](getting-the-system-version.md)
</dt> <dt>

[<span data-ttu-id="f54d0-118">Fonctions d’assistance de version</span><span class="sxs-lookup"><span data-stu-id="f54d0-118">Version Helper functions</span></span>](version-helper-apis.md)
</dt> <dt>

[<span data-ttu-id="f54d0-119">OSVERSIONINFO</span><span class="sxs-lookup"><span data-stu-id="f54d0-119">OSVERSIONINFO</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoa)
</dt> <dt>

[<span data-ttu-id="f54d0-120">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="f54d0-120">OSVERSIONINFOEX</span></span>](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa)
</dt> </dl>
