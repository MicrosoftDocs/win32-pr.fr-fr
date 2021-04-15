---
title: Développement d’applications pour les versions antérieures de Windows
description: Explique ce que vous devez faire pour développer des applications qui s’exécutent sur des versions antérieures de Windows et tirer parti de l’API prise en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.
ms.assetid: 9c46f894-e5cd-46a1-81c8-f63b09504735
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d4c61b0e2b931c3833934c843bf964fc3fa7c
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104393891"
---
# <a name="developing-applications-for-previous-versions-of-windows"></a><span data-ttu-id="38aab-103">Développement d’applications pour les versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="38aab-103">Developing Applications for Previous Versions of Windows</span></span>

<span data-ttu-id="38aab-104">Explique ce que vous devez faire pour développer des applications qui s’exécutent sur des versions antérieures de Windows et tirer parti de l’API prise en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="38aab-104">Explains what to do to develop applications that run on previous versions of Windows and take advantage of the API that are supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

## <a name="required-downloads"></a><span data-ttu-id="38aab-105">Téléchargements requis</span><span class="sxs-lookup"><span data-stu-id="38aab-105">Required Downloads</span></span>

<span data-ttu-id="38aab-106">Le téléchargement et l’installation des packages décrits dans les sections suivantes sont nécessaires si vous souhaitez développer des applications qui utilisent des API introduites avec le kit de développement logiciel (SDK) Microsoft Windows pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38aab-106">Download and installation of the packages described in the following sections is required if you want to develop applications that use API that are introduced with the Microsoft Windows Software Development Kit (SDK) for Windows 7.</span></span>

### <a name="microsoft-windows-sdk"></a><span data-ttu-id="38aab-107">Microsoft Windows SDK</span><span class="sxs-lookup"><span data-stu-id="38aab-107">Microsoft Windows SDK</span></span>

<span data-ttu-id="38aab-108">La SDK Windows pour Windows 7 est nécessaire pour créer des applications qui utilisent des API prises en charge avec la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="38aab-108">The Windows SDK for Windows 7 is required for creating applications that use APIs supported with the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="38aab-109">Pour accéder à des ressources et des informations supplémentaires, telles que des téléchargements, des publications de forum et le blog de l’équipe SDK Windows, consultez le [Centre de développement SDK Windows](https://msdn.microsoft.com/bb980924.aspx) ( https://msdn.microsoft.com/bb980924.aspx) .</span><span class="sxs-lookup"><span data-stu-id="38aab-109">For access to additional resources and information, such as downloads, forum posts, and the Windows SDK team blog, see the [Windows SDK Developer Center](https://msdn.microsoft.com/bb980924.aspx) (https://msdn.microsoft.com/bb980924.aspx).</span></span>

### <a name="net-framework"></a><span data-ttu-id="38aab-110">.NET Framework</span><span class="sxs-lookup"><span data-stu-id="38aab-110">.NET Framework</span></span>

<span data-ttu-id="38aab-111">Le .NET Framework 3,5 Service Pack 1 est requis pour créer des applications qui utilisent des API prises en charge par la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="38aab-111">The .NET Framework 3.5 Service Pack 1 is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

<span data-ttu-id="38aab-112">Pour obtenir des informations et des ressources supplémentaires, consultez le [Centre de développement .NET Framework](https://msdn.microsoft.com/netframework/default.aspx) ( https://msdn.microsoft.com/netframework/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="38aab-112">For additional resources and information, see the [.NET Framework Developer Center](https://msdn.microsoft.com/netframework/default.aspx) (https://msdn.microsoft.com/netframework/default.aspx).</span></span>

### <a name="directx-sdk-required-when-using-direct3d"></a><span data-ttu-id="38aab-113">SDK DirectX requis lors de l’utilisation de Direct3D</span><span class="sxs-lookup"><span data-stu-id="38aab-113">DirectX SDK Required When Using Direct3D</span></span>

<span data-ttu-id="38aab-114">Si vous créez des applications qui utilisent Direct3D, le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) est requis pour créer des applications qui utilisent des API prises en charge par la mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="38aab-114">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required for creating applications that use APIs supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008.</span></span>

### <a name="update-your-development-computer"></a><span data-ttu-id="38aab-115">Mettre à jour votre ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="38aab-115">Update Your Development Computer</span></span>

<span data-ttu-id="38aab-116">Assurez-vous que votre ordinateur de développement dispose de toutes les mises à jour les plus récentes à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="38aab-116">Ensure that your development computer has all of the latest updates from Windows Update.</span></span>

<span data-ttu-id="38aab-117">Si vous développez des applications sur une version antérieure de Windows, vous devez obtenir la mise à jour de la plateforme pour Windows Vista ou la mise à jour de la plateforme pour Windows Server 2008 à partir de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="38aab-117">If you are developing applications on a previous version of Windows, you must obtain the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update from Windows Update.</span></span> <span data-ttu-id="38aab-118">L’installation de l’une de ces mises à jour vous permettra de tirer parti de la nouvelle API fournie par le SDK Windows pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38aab-118">Installing either of these updates will enable you to take advantage of the new API provided by the Windows SDK for Windows 7.</span></span>

<span data-ttu-id="38aab-119">Pour plus d’informations sur la façon d’obtenir des mises à jour à partir de Windows Update consultez l' [article de la base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) ( https://support.microsoft.com/kb/971644) .</span><span class="sxs-lookup"><span data-stu-id="38aab-119">For more information about how to obtain updates from Windows Update see the [Knowledge Base article about the Platform Update for Windows Vista (KB 971644)](https://support.microsoft.com/kb/971644) (https://support.microsoft.com/kb/971644).</span></span>

## <a name="development-environment"></a><span data-ttu-id="38aab-120">Environnement de développement</span><span class="sxs-lookup"><span data-stu-id="38aab-120">Development Environment</span></span>

### <a name="set-the-build-target-to-windows-7"></a><span data-ttu-id="38aab-121">Définir la cible de génération sur Windows 7</span><span class="sxs-lookup"><span data-stu-id="38aab-121">Set the Build Target to Windows 7</span></span>

<span data-ttu-id="38aab-122">Toutes les applications qui utilisent des bibliothèques dans la mise à jour de plateforme pour Windows Vista doivent être générées par rapport à la plateforme cible Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38aab-122">All applications that use libraries in the Platform Update for Windows Vista must be built against the Windows 7 target platform.</span></span>

<span data-ttu-id="38aab-123">La définition de WINVER sur la valeur de la plateforme cible Windows 7 vous permet de développer des applications qui utilisent des API prises en charge avec la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008 sur un ordinateur de développement exécutant Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="38aab-123">Setting WINVER to the Windows 7 target platform value enables you to develop applications that use APIs supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 on a development machine running Windows Vista.</span></span>

<span data-ttu-id="38aab-124">Vous pouvez définir la plateforme cible sur Windows 7 dans votre code source ou à l’aide de l’option/D avec le compilateur Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="38aab-124">You can set the target platform to Windows 7 either in your source code or by using the /D option with the Visual Studio compiler.</span></span>

<span data-ttu-id="38aab-125">L’exemple suivant montre comment définir WINVER dans votre code source.</span><span class="sxs-lookup"><span data-stu-id="38aab-125">The following example shows how to set WINVER in your source code.</span></span>


```C++
#define WINVER 0x0601
```



<span data-ttu-id="38aab-126">L’exemple suivant montre comment définir WINVER à l’aide de l’option du compilateur/D.</span><span class="sxs-lookup"><span data-stu-id="38aab-126">The following example shows how to set WINVER using the /D compiler option.</span></span>

``` syntax
/DWINVER=0x0601
```

## <a name="application-deployment"></a><span data-ttu-id="38aab-127">Déploiement d’application</span><span class="sxs-lookup"><span data-stu-id="38aab-127">Application Deployment</span></span>

<span data-ttu-id="38aab-128">Si vous générez votre application à l’aide des en-têtes et des bibliothèques fournis par le SDK Windows pour Windows 7, les API prises en charge s’exécuteront sur toutes les versions de Windows dont la mise à jour de plateforme pour Windows Vista ou la mise à jour de plateforme pour Windows Server 2008 est installée.</span><span class="sxs-lookup"><span data-stu-id="38aab-128">If you build your application using the headers and libraries provided by the Windows SDK for Windows 7, supported APIs will run on any Windows version that has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 installed.</span></span>

> [!Note]  
> <span data-ttu-id="38aab-129">Le comportement, les performances ou la configuration requise pour certaines API prises en charge avec la mise à jour de plateforme pour Windows Vista ou pour la mise à jour de plateforme pour Windows Server 2008 peuvent varier selon les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="38aab-129">The behavior, performance, or requirements for some APIs that are supported with the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 may vary across different versions of Windows.</span></span> <span data-ttu-id="38aab-130">Pour plus d’informations sur une API spécifique prise en charge par les mises à jour, consultez à [propos de la mise à jour de la plateforme pour Windows Vista](platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="38aab-130">For details about a specific API that is supported by the updates, see [About Platform Update for Windows Vista](platform-update-for-windows-vista-overview.md).</span></span>

 

### <a name="no-redistributable-components"></a><span data-ttu-id="38aab-131">Aucun composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="38aab-131">No Redistributable Components</span></span>

<span data-ttu-id="38aab-132">Votre application n’a pas besoin d’installer des composants redistribuables, tels que des dll ou d’autres fichiers d’exécution.</span><span class="sxs-lookup"><span data-stu-id="38aab-132">Your application does not need to install redistributable components, such as DLLs or other run-time files.</span></span>

### <a name="requires-updated-end-user-computer"></a><span data-ttu-id="38aab-133">Nécessite la mise à jour de End-User ordinateur</span><span class="sxs-lookup"><span data-stu-id="38aab-133">Requires Updated End-User Computer</span></span>

<span data-ttu-id="38aab-134">Étant donné que la mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 sont hébergées par Windows Update, les utilisateurs finaux avec des mises à jour automatiques activées sont très susceptibles d’avoir déjà ces mises à jour, ainsi que les service packs requis.</span><span class="sxs-lookup"><span data-stu-id="38aab-134">Because Platform Update for Windows Vista and Platform Update for Windows Server 2008 are hosted by Windows Update, end-users with automatic updates enabled are highly likely to already have these updates as well as the required service packs.</span></span>

<span data-ttu-id="38aab-135">Si l’ordinateur de l’utilisateur final ne dispose pas de la mise à jour de la plateforme pour Windows Vista ou de la mise à jour de la plateforme pour Windows Server 2008 et que votre application nécessite des API prises en charge avec ces mises à jour, il se peut que votre application ne puisse pas s’exécuter sur l’ordinateur de l’utilisateur final ou rencontre des erreurs lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="38aab-135">If the end-user's computer does not have Platform Update for Windows Vista or Platform Update for Windows Server 2008 installed and your application requires APIs that are supported with these updates, your application may not be able to run on the end-user's computer or may encounter errors during execution.</span></span>

<span data-ttu-id="38aab-136">Pour éviter les problèmes qui peuvent être causés par l’ordinateur de l’utilisateur obsolète, vous devez vérifier que l’ordinateur de l’utilisateur dispose de la mise à jour de la plateforme pour Windows Vista ou de la mise à jour de la plateforme pour Windows Server 2008 lors de l’installation de votre application.</span><span class="sxs-lookup"><span data-stu-id="38aab-136">To avoid the problems that could be caused by your user's computer being out-of-date, you want to verify that your user's computer has the Platform Update for Windows Vista or the Platform Update for Windows Server 2008 update during the installation of your application.</span></span> <span data-ttu-id="38aab-137">Vous pouvez utiliser l' [API](/windows/desktop/Wua_Sdk/portal-client) de l’Agent de Windows Update pour vérifier l’ordinateur de l’utilisateur final pour les mises à jour installées.</span><span class="sxs-lookup"><span data-stu-id="38aab-137">You can use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to check your end-user's computer for installed updates.</span></span> <span data-ttu-id="38aab-138">Vous pouvez également utiliser l’API Windows Update Agent pour télécharger et installer les mises à jour requises lors de l’installation de l’application si l’utilisateur final n’a pas déjà installé les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="38aab-138">You can also use the Windows Update Agent API to download and install required updates during application installation if the end-user has not already installed the updates.</span></span>

<span data-ttu-id="38aab-139">Pour obtenir un exemple de programme d’installation qui montre comment utiliser l’API de l' [agent de Windows Update](/windows/desktop/Wua_Sdk/portal-client), consultez [déploiement de Direct3D 11 pour les développeurs de jeux](../direct3darticles/direct3d11-deployment.md) dans le kit de [développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) .</span><span class="sxs-lookup"><span data-stu-id="38aab-139">For an example of an installer that demonstrates how to use the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client), see [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md) in the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx).</span></span>

<span data-ttu-id="38aab-140">Bien que l’exemple de programme d’installation D3D11InstallHelper abordé dans le [déploiement de Direct3D 11 pour les développeurs de jeux](../direct3darticles/direct3d11-deployment.md)ait été conçu pour les applications qui utilisent Direct3D 11, il fournit un bon exemple d’interaction avec l' [API d’agent Windows Update](/windows/desktop/Wua_Sdk/portal-client) pour lancer et suivre le téléchargement et l’installation des mises à jour qui sont hébergées par Windows Update.</span><span class="sxs-lookup"><span data-stu-id="38aab-140">Although the D3D11InstallHelper installer sample that is discussed in [Direct3D 11 Deployment for Game Developers](../direct3darticles/direct3d11-deployment.md), was written for applications that use Direct3D 11, it provides a good example of how to interact with the [Windows Update Agent API](/windows/desktop/Wua_Sdk/portal-client) to initiate and track the download and installation of updates that are hosted by Windows Update.</span></span> <span data-ttu-id="38aab-141">La compilation de cet exemple peut nécessiter l’SDK Windows pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="38aab-141">Compiling this sample may require the Windows SDK for Windows 7.</span></span> <span data-ttu-id="38aab-142">Pour plus d’informations sur l’exemple D3D11InstallHelper, y compris les problèmes connus, consultez le [Kit de développement logiciel (SDK) DirectX](/previous-versions/windows/apps/hh452744(v=win.10)) ( https://msdn.microsoft.com/directx/aa937788.aspx) notes de publication pour août 2009. mise à jour de la plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38aab-142">For additional information about the D3D11InstallHelper sample, including known issues, see the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) Release Notes for August 2009.Platform Update for Windows Vista</span></span>

## <a name="related-topics"></a><span data-ttu-id="38aab-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="38aab-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38aab-144">Mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38aab-144">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="38aab-145">**Vues d'ensemble**</span><span class="sxs-lookup"><span data-stu-id="38aab-145">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="38aab-146">À propos de la mise à jour de plateforme pour Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38aab-146">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="38aab-147">Article de la base de connaissances sur la mise à jour de plateforme pour Windows Vista (KB 971644)</span><span class="sxs-lookup"><span data-stu-id="38aab-147">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 