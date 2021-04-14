---
title: Modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2
description: Modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2
ms.assetid: 3040262A-85EB-4F26-BE34-D2BBD5886E9E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0078ba918c675bbc8b9b9bbaf76660388f05bda9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382703"
---
# <a name="operating-system-version-changes-in-windows-81-and-windows-server-2012-r2"></a><span data-ttu-id="7f7fc-103">Modifications de version du système d’exploitation dans Windows 8.1 et Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7f7fc-103">Operating system version changes in Windows 8.1 and Windows Server 2012 R2</span></span>

## <a name="platforms"></a><span data-ttu-id="7f7fc-104">Plateformes</span><span class="sxs-lookup"><span data-stu-id="7f7fc-104">Platforms</span></span>

<span data-ttu-id="7f7fc-105">**Clients-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="7f7fc-105">**Clients -** Windows 8.1</span></span>

<span data-ttu-id="7f7fc-106">**Serveurs-** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="7f7fc-106">**Servers -** Windows Server 2012 R2</span></span>

## <a name="description"></a><span data-ttu-id="7f7fc-107">Description</span><span class="sxs-lookup"><span data-stu-id="7f7fc-107">Description</span></span>

<span data-ttu-id="7f7fc-108">Nous avons apporté des changements significatifs dans la façon dont les API GetVersion (ex) fonctionnent dans Windows 8.1 en raison de comportements de client indésirables résultant de la façon dont les API GetVersion (ex) ont été utilisées par le passé.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-108">We have made some significant changes in how the GetVersion(Ex) APIs work in Windows 8.1 due to undesirable customer behaviors resulting from how the GetVersion(Ex) APIs have been used in the past.</span></span>

<span data-ttu-id="7f7fc-109">Dans les versions précédentes de Windows, l’appel des API GetVersion (ex) retournerait la version du système d’exploitation (se), à moins que le processus n’ait été atténué par un shim de compatibilité des applications pour lui donner une version différente.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-109">In previous versions of Windows, calling the GetVersion(Ex) APIs would return the actual version of the operating system (OS), unless the process had been mitigated by an app compat shim to give it a different version.</span></span> <span data-ttu-id="7f7fc-110">Cette opération a été effectuée sur une base provisoire et était relativement incomplète en termes de nombre de processus que Microsoft pourrait raisonnablement déchiffrer dans une version.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-110">This was done on a provisional basis and was relatively incomplete in terms of the number of processes that Microsoft could reasonably shim in a release.</span></span> <span data-ttu-id="7f7fc-111">De nombreuses applications sont tombées en raison de fissures, car elles n’ont pas été corrigées en raison de vérifications de version mal conçues.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-111">Many applications fell through the cracks because they didn’t get shimmed due to poorly designed version checks.</span></span>

<span data-ttu-id="7f7fc-112">La vérification de la version permet d’avertir l’utilisateur que l’application doit s’exécuter sur une version plus récente du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-112">The number one reason to do a version check is to warn the user that the application needs to run on a newer version of the OS.</span></span> <span data-ttu-id="7f7fc-113">Toutefois, en raison de mauvaises vérifications, les applications signalent souvent de manière incorrecte qu’elles devaient être exécutées sur Windows XP ou version ultérieure, ce qui, bien sûr, est le système d’exploitation le plus récent.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-113">However due to poor checks, apps would often incorrectly warn that they needed to be run on Windows XP or later, which of course the newest OS is.</span></span> <span data-ttu-id="7f7fc-114">Plus souvent, le système d’exploitation le plus récent exécute l’application sans aucun problème, si ce n’est pas le cas pour ces vérifications.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-114">More often than not, the newest OS would run the application without any issues if not for these checks.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7f7fc-115">Manifestation</span><span class="sxs-lookup"><span data-stu-id="7f7fc-115">Manifestation</span></span>

<span data-ttu-id="7f7fc-116">Dans Windows 8.1, les API GetVersion (ex) sont dépréciées.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-116">In Windows 8.1, the GetVersion(Ex) APIs have been deprecated.</span></span> <span data-ttu-id="7f7fc-117">Cela signifie que même si vous pouvez toujours appeler ces fonctions API, si votre application ne cible pas spécifiquement Windows 8.1, les fonctions retournent la version de Windows 8 (6,2).</span><span class="sxs-lookup"><span data-stu-id="7f7fc-117">That means that while you can still call these API functions, if your app does not specifically target Windows 8.1, the functions will return the Windows 8 version (6.2).</span></span>

## <a name="solution"></a><span data-ttu-id="7f7fc-118">Solution</span><span class="sxs-lookup"><span data-stu-id="7f7fc-118">Solution</span></span>

### <a name="adding-an-app-manifest"></a><span data-ttu-id="7f7fc-119">Ajout d’un manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="7f7fc-119">Adding an app manifest</span></span>

<span data-ttu-id="7f7fc-120">Pour que votre application cible Windows 8.1, vous devez inclure un [manifeste d’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-120">In order for your app to target Windows 8.1, you'll need to include an [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="7f7fc-121">Ensuite, dans la [section **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste, vous devez ajouter un élémentos **&lt; pris en charge &gt;** pour chaque version de Windows que vous souhaitez déclarer prise en charge par votre application.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-121">Then, in the [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest, you'll need to add a **&lt;supportedOS&gt;** element for each Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="7f7fc-122">L’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista pour Windows 8.1 :</span><span class="sxs-lookup"><span data-stu-id="7f7fc-122">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 8.1:</span></span>

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

<span data-ttu-id="7f7fc-123">La ligne ci-dessus indiquée `* ADD THIS LINE *` indique comment cibler avec précision votre application pour Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-123">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 8.1.</span></span>

<span data-ttu-id="7f7fc-124">La déclaration de la prise en charge des Windows 8.1 dans le manifeste de votre application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-124">Declaring support for Windows 8.1 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

### <a name="using-versionhelpers-instead-of-getversionex"></a><span data-ttu-id="7f7fc-125">Utilisation de VersionHelpers au lieu de GetVersion (ex)</span><span class="sxs-lookup"><span data-stu-id="7f7fc-125">Using VersionHelpers instead of GetVersion(Ex)</span></span>

<span data-ttu-id="7f7fc-126">Windows 8.1 introduit de nouvelles fonctions API de remplacement pour GetVersion (ex), connu sous le nom de VersionHelpers.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-126">Windows 8.1 introduces new replacement API functions for GetVersion(Ex), known as VersionHelpers.</span></span> <span data-ttu-id="7f7fc-127">Ils sont extrêmement faciles à utiliser ; tout ce que vous avez à faire est `#include <VersionHelpers.h>` .</span><span class="sxs-lookup"><span data-stu-id="7f7fc-127">They are extremely easy to use; all you have to do is `#include <VersionHelpers.h>`.</span></span> <span data-ttu-id="7f7fc-128">Les fonctions inline disponibles dans le fichier d’en-tête VersionHelpers. h permettent à votre code de demander si le système d’exploitation est une version spécifique de Windows ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-128">The inline functions available in the VersionHelpers.h header file allow your code to ask whether the operating system is a given version of Windows or later.</span></span>

<span data-ttu-id="7f7fc-129">**Exemple** Par exemple, si votre application nécessite Windows 8 ou version ultérieure, utilisez le test suivant :</span><span class="sxs-lookup"><span data-stu-id="7f7fc-129">**Example** For example, if your application requires Windows 8 or later, use the following test:</span></span>

```cpp
#include <VersionHelpers.h>
// ...
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }
```

<span data-ttu-id="7f7fc-130">Les fonctions de l’API VersionHelper disponibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f7fc-130">The available VersionHelper API functions are:</span></span>

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

<span data-ttu-id="7f7fc-131">Ils retournent la valeur TRUE ou FALSe en fonction de la question que vous demandez, et vous devez uniquement définir le système d’exploitation de niveau minimal que vous prenez en charge.</span><span class="sxs-lookup"><span data-stu-id="7f7fc-131">They will return TRUE or FALSE depending on the question you are asking, and you only need to define the minimum level operating system that you support.</span></span>

## <a name="resources"></a><span data-ttu-id="7f7fc-132">Ressources</span><span class="sxs-lookup"><span data-stu-id="7f7fc-132">Resources</span></span>

-   [<span data-ttu-id="7f7fc-133">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="7f7fc-133">Application Compatibility Toolkit Download</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyId=24DA89E9-B581-47B0-B45E-492DD6DA2971)
-   <span data-ttu-id="7f7fc-134">[Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="7f7fc-134">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="7f7fc-135">API VersionHelpers</span><span class="sxs-lookup"><span data-stu-id="7f7fc-135">VersionHelpers APIs</span></span>](../sysinfo/version-helper-apis.md)