---
title: Vérification de la version de Windows
description: La version du système d’exploitation a été incrémentée avec la version du système d’exploitation Windows 10.
ms.assetid: 55BB7B44-1AFD-456D-9380-38B4D26E5EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea1e65ed97859486bdd0a18fe53ee44a653faf
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104102492"
---
# <a name="windows-version-check"></a><span data-ttu-id="6e948-103">Vérification de la version de Windows</span><span class="sxs-lookup"><span data-stu-id="6e948-103">Windows version check</span></span>

<span data-ttu-id="6e948-104">La version du système d’exploitation a été incrémentée avec la version du système d’exploitation Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6e948-104">The OS version has been incremented with the Windows 10 OS release.</span></span> <span data-ttu-id="6e948-105">Cela signifie que le numéro de version interne de Windows 10 a également été remplacé par 10,0.</span><span class="sxs-lookup"><span data-stu-id="6e948-105">This means that the internal version number for Windows 10 has also been changed to 10.0.</span></span> <span data-ttu-id="6e948-106">Comme précédemment, nous faisons le maximum pour maintenir la compatibilité entre les applications et les appareils après un changement de version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6e948-106">As in the past, we go to great lengths to maintain application and device compatibility after an OS version change.</span></span> <span data-ttu-id="6e948-107">Pour la plupart des catégories d’applications (sans dépendances de noyau), la modification n’aura pas d’impact négatif sur les fonctionnalités de l’application, et les applications existantes continueront à fonctionner correctement sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6e948-107">For most app categories (without any kernel dependencies) the change will not negatively impact app functionality, and existing apps will continue to work fine on Windows 10.</span></span>

## <a name="manifestations"></a><span data-ttu-id="6e948-108">Manifestations</span><span class="sxs-lookup"><span data-stu-id="6e948-108">Manifestations</span></span>

<span data-ttu-id="6e948-109">La manifestation de cette modification est propre à l’application.</span><span class="sxs-lookup"><span data-stu-id="6e948-109">The manifestation of this change is app-specific.</span></span> <span data-ttu-id="6e948-110">En d’autres termes, une application qui vérifie spécifiquement la version du système d’exploitation obtient un numéro de version supérieur, ce qui peut conduire aux situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e948-110">This means any app that specifically checks for the OS version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="6e948-111">Les programmes d’installation des applications peuvent ne pas être en mesure d’installer les applications, ou les applications peuvent être dans l’impossibilité de démarrer.</span><span class="sxs-lookup"><span data-stu-id="6e948-111">App installers might not be able to install the app, and apps might not be able to start.</span></span>
-   <span data-ttu-id="6e948-112">Les applications peuvent devenir instables ou se planter.</span><span class="sxs-lookup"><span data-stu-id="6e948-112">Apps might become unstable or crash.</span></span>
-   <span data-ttu-id="6e948-113">Les applications peuvent générer des messages d’erreur, tout en continuant de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="6e948-113">Apps might generate error messages, but continue to function properly.</span></span>

<span data-ttu-id="6e948-114">Certaines applications effectuent une vérification de version et transmettent simplement un avertissement aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="6e948-114">Some apps perform a version check and simply pass a warning to users.</span></span> <span data-ttu-id="6e948-115">Cependant, certaines d’entre elles sont liées très étroitement à une vérification de la version (dans les pilotes ou en mode noyau pour éviter la détection).</span><span class="sxs-lookup"><span data-stu-id="6e948-115">However, there are apps that are bound very tightly to a version check (in the drivers, or in kernel mode to avoid detection).</span></span> <span data-ttu-id="6e948-116">Dans ce cas, les applications échouent si une version incorrecte est détectée.</span><span class="sxs-lookup"><span data-stu-id="6e948-116">In these cases, the app will fail if an incorrect version is found.</span></span> <span data-ttu-id="6e948-117">Au lieu d’une vérification de la version, nous vous recommandons une des approches suivantes :</span><span class="sxs-lookup"><span data-stu-id="6e948-117">Rather than a version check, we recommend one of the following approaches:</span></span>

-   <span data-ttu-id="6e948-118">Si l’application dépend de fonctionnalités d’API spécifiques, veillez à cibler la version d’API correcte.</span><span class="sxs-lookup"><span data-stu-id="6e948-118">If the app is dependent on specific API functionality, ensure you target the correct API version.</span></span>
-   <span data-ttu-id="6e948-119">Le numéro de version de NTDDI (interface de pilote de périphérique NT) est incrémenté uniquement si la fonctionnalité cible de l’API change.</span><span class="sxs-lookup"><span data-stu-id="6e948-119">NTDDI (NT device driver interface) version number will increment only if target functionality in the API changes.</span></span> <span data-ttu-id="6e948-120">Veillez à détecter la modification via APISet ou une autre API exposée telle qu’elle a été créée par l’équipe des fonctionnalités, et n’utilisez pas la version en tant que proxy pour une fonctionnalité ou un correctif.</span><span class="sxs-lookup"><span data-stu-id="6e948-120">Ensure you detect the change via APISet or other exposed API as created by the feature team, and do not use the version as a proxy for some feature or fix.</span></span> <span data-ttu-id="6e948-121">En cas de changements cassants, et si une vérification correcte n’est pas exposée, il s’agit d’un bogue.</span><span class="sxs-lookup"><span data-stu-id="6e948-121">If there are breaking changes and a proper check is not exposed, then that is a bug.</span></span>
-   <span data-ttu-id="6e948-122">Assurez-vous que l’application ne vérifie pas la version de manière étrange, par exemple par le biais du Registre, des versions de fichiers, des décalages, du mode noyau, des pilotes ou d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="6e948-122">Ensure the app does NOT check for version in odd ways, such as via the registry, file versions, offsets, kernel mode, drivers or other means.</span></span> <span data-ttu-id="6e948-123">Si l’application doit absolument vérifier la version, utilisez les API GetVersion, qui doivent retourner le numéro principal, le numéro secondaire et le numéro de Build.</span><span class="sxs-lookup"><span data-stu-id="6e948-123">If the app absolutely needs to check the version, use the GetVersion APIs, which should return the major, minor and build number.</span></span>
-   <span data-ttu-id="6e948-124">Si vous utilisez l’API GetVersion ou d’autres fonctions d’assistance de version, telles que [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), n’oubliez pas que le comportement de cette API a été modifié à partir de Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="6e948-124">If you are using the GetVersion API or other Version Helper functions such as [VerifyVersionInfo](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa), remember that the behavior of this API has changed starting with Windows 8.1.</span></span> <span data-ttu-id="6e948-125">Pour plus d’informations, reportez-vous à [la documentation de l’API](../SysInfo/version-helper-apis.md) .</span><span class="sxs-lookup"><span data-stu-id="6e948-125">Please refer to [the API documentation](../SysInfo/version-helper-apis.md) for more details.</span></span>
-   <span data-ttu-id="6e948-126">Si vous possédez des applications telles qu’un logiciel anti-programme malveillant ou un pare-feu, vous devez passer par vos canaux de commentaires habituels et par le biais du programme Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="6e948-126">If you own apps such as antimalware or firewall, you should work through your usual feedback channels and via the Windows Insider program.</span></span>

## <a name="declaring-windows-10-compatibility-with-an-app-manifest"></a><span data-ttu-id="6e948-127">Déclaration de compatibilité Windows 10 avec un manifeste d’application</span><span class="sxs-lookup"><span data-stu-id="6e948-127">Declaring Windows 10 Compatibility With An App Manifest</span></span>

<span data-ttu-id="6e948-128">Si votre application est compatible avec Windows 10, elle peut déclarer ce fait dans le [manifeste de l’application (exécutable)](/windows/compatibility/application-executable-manifest) pour l’exécutable de l’application.</span><span class="sxs-lookup"><span data-stu-id="6e948-128">If your app is compatible with Windows 10, it can declare this fact in the [app (executable) manifest](/windows/compatibility/application-executable-manifest) for the app's executable.</span></span> <span data-ttu-id="6e948-129">Cela indique au système que votre application comprend le numéro de version du système 10,0 de Windows 10 (par conséquent, l’API GetVersion ne retourne pas de version antérieure) et laisse le système désactiver d’autres comportements de compatibilité appliqués aux applications qui ne déclarent pas la compatibilité avec Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6e948-129">This tells the system that your app understands Windows 10's system version number of 10.0 (so the GetVersion API does not return an earlier version), and also lets the system turn off other compatibility behaviors applied to apps that don't declare Windows 10 compatibility.</span></span>

<span data-ttu-id="6e948-130">Pour déclarer la compatibilité Windows 10 dans un manifeste d’application, vous devez ajouter une [section de **&lt; &gt; compatibilité**](../SbsCs/application-manifests.md#compatibility) du manifeste si aucune n’existe déjà, puis ajouter des éléments **&lt; pris en &gt; charge** pour Windows 10 et toutes les autres versions de Windows que vous souhaitez déclarer que votre application prend en charge.</span><span class="sxs-lookup"><span data-stu-id="6e948-130">To declare Windows 10 compatibility in an app manifest, you'll need to add a [**&lt;compatibility&gt;** section](../SbsCs/application-manifests.md#compatibility) of the manifest if one does not already exist, and then add **&lt;supportedOS&gt;** elements for Windows 10 and every other Windows version you want to declare that your app supports.</span></span>

<span data-ttu-id="6e948-131">L’exemple suivant montre un fichier manifeste d’application pour une application qui prend en charge toutes les versions de Windows de Windows Vista vers Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="6e948-131">The following example shows an app manifest file for an app that supports all versions of Windows from Windows Vista to Windows 10:</span></span>

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
            <supportedOS Id="{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}"/> <!-- * ADD THIS LINE * -->
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
</assembly>
```

<span data-ttu-id="6e948-132">La ligne ci-dessus indiquée `* ADD THIS LINE *` indique comment cibler avec précision votre application pour Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6e948-132">The line above marked `* ADD THIS LINE *` shows how to accurately target your application for Windows 10.</span></span>

<span data-ttu-id="6e948-133">La déclaration de la prise en charge de Windows 10 dans votre manifeste d’application n’aura aucun effet lors de l’exécution de votre application sur les systèmes d’exploitation précédents.</span><span class="sxs-lookup"><span data-stu-id="6e948-133">Declaring support for Windows 10 in your app manifest will not have any effect when running your app on previous operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="6e948-134">Ressources</span><span class="sxs-lookup"><span data-stu-id="6e948-134">Resources</span></span>

-   [<span data-ttu-id="6e948-135">Application Compatibility Toolkit Download : Téléchargez Windows ADK pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="6e948-135">Application Compatibility Toolkit Download: Download the Windows ADK for Windows 10</span></span>](https://download.microsoft.com/download/9/A/E/9AE69DD5-BA93-44E0-864E-180F5E700AB4/adk/adksetup.exe)
-   <span data-ttu-id="6e948-136">[Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6e948-136">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>
-   [<span data-ttu-id="6e948-137">API d’assistance de version</span><span class="sxs-lookup"><span data-stu-id="6e948-137">Version Helpers API</span></span>](../sysinfo/version-helper-apis.md)