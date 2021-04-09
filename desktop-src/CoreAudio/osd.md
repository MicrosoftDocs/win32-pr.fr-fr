---
description: Cet exemple utilise les API audio de base pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent via l’appareil de point de terminaison de rendu audio par défaut.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: DÉPLOIEMENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033712"
---
# <a name="osd"></a><span data-ttu-id="5c8a9-103">DÉPLOIEMENT</span><span class="sxs-lookup"><span data-stu-id="5c8a9-103">OSD</span></span>

<span data-ttu-id="5c8a9-104">Cet exemple utilise les API audio de base pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent via l’appareil de point de terminaison de rendu audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="5c8a9-105">L’affichage à l’écran s’affiche lorsque l’utilisateur ajuste le niveau de volume dans le programme de contrôle de volume Windows, Sndvol.exe, et disparaît une fois que le volume reste inchangé pendant une brève période.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="5c8a9-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="5c8a9-107">Description</span><span class="sxs-lookup"><span data-stu-id="5c8a9-107">Description</span></span>](#description)
-   [<span data-ttu-id="5c8a9-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c8a9-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5c8a9-109">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5c8a9-110">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5c8a9-111">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="5c8a9-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c8a9-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="5c8a9-113">Description</span><span class="sxs-lookup"><span data-stu-id="5c8a9-113">Description</span></span>

<span data-ttu-id="5c8a9-114">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="5c8a9-115">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="5c8a9-116">[API EndpointVolume](endpointvolume-api.md) audio</span><span class="sxs-lookup"><span data-stu-id="5c8a9-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="5c8a9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c8a9-117">Requirements</span></span>



| <span data-ttu-id="5c8a9-118">Produit</span><span class="sxs-lookup"><span data-stu-id="5c8a9-118">Product</span></span>                                                        | <span data-ttu-id="5c8a9-119">Version</span><span class="sxs-lookup"><span data-stu-id="5c8a9-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="5c8a9-120">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="5c8a9-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="5c8a9-121">Windows Vista ou version ultérieure ;</span><span class="sxs-lookup"><span data-stu-id="5c8a9-121">Windows Vista or later</span></span> |
| <span data-ttu-id="5c8a9-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5c8a9-122">Visual Studio</span></span>                                                  | <span data-ttu-id="5c8a9-123">2005 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="5c8a9-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5c8a9-124">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-124">Downloading the Sample</span></span>

<span data-ttu-id="5c8a9-125">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="5c8a9-126">Emplacement</span><span class="sxs-lookup"><span data-stu-id="5c8a9-126">Location</span></span>    | <span data-ttu-id="5c8a9-127">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="5c8a9-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c8a9-128">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="5c8a9-128">Windows SDK</span></span> | <span data-ttu-id="5c8a9-129">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ d' \\ OSD audio multimédia \\ \\ ...</span><span class="sxs-lookup"><span data-stu-id="5c8a9-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="5c8a9-130">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-130">Building the Sample</span></span>

1.  <span data-ttu-id="5c8a9-131">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire de l’exemple OSD.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="5c8a9-132">Exécutez la commande « Start OSD. sln » dans le répertoire OSD pour ouvrir le projet OSD dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="5c8a9-133">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="5c8a9-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="5c8a9-134">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="5c8a9-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="5c8a9-135">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, OSD. vcproj.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="5c8a9-136">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="5c8a9-136">Running the Sample</span></span>

1.  <span data-ttu-id="5c8a9-137">Exécutez le fichier exécutable OSD, OSD.exe, dans Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="5c8a9-138">Notez que vous ne verrez pas une icône de barre d’état système ou une fenêtre pour l’application, mais vous pouvez voir le processus en cours d’exécution à l’aide de TaskMgr.exe.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="5c8a9-139">Exécutez sndvol.exe pour modifier le volume ou le sourdine, ou modifiez le volume à l’aide de contrôles de clavier ou d’un contrôle HID.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="5c8a9-140">L’interface utilisateur OSD s’affiche.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="5c8a9-141">Pour quitter l’application, exécutez TaskMgr.exe, mettez en surbrillance le processus OSD.exe et cliquez sur **terminer le processus**.</span><span class="sxs-lookup"><span data-stu-id="5c8a9-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8a9-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5c8a9-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8a9-143">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="5c8a9-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



