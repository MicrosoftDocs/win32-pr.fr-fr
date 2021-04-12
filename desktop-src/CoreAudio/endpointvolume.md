---
description: Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, comme spécifié par l’utilisateur.
ms.assetid: 2597f3b1-5339-4fd4-9938-39ff917626b4
title: EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e89efe89035ec272c68c6a9289672a249616e23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483489"
---
# <a name="endpointvolume"></a><span data-ttu-id="b9559-103">EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="b9559-103">EndpointVolume</span></span>

<span data-ttu-id="b9559-104">Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, comme spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9559-104">This sample application uses the Core Audio APIs to change the volume of the device, as specified by the user.</span></span>

<span data-ttu-id="b9559-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9559-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b9559-106">Description</span><span class="sxs-lookup"><span data-stu-id="b9559-106">Description</span></span>](#description)
-   [<span data-ttu-id="b9559-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9559-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b9559-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b9559-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b9559-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="b9559-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9559-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="b9559-112">Description</span><span class="sxs-lookup"><span data-stu-id="b9559-112">Description</span></span>

<span data-ttu-id="b9559-113">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="b9559-113">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="b9559-114">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="b9559-114">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="b9559-115">[API EndpointVolume](endpointvolume-api.md) pour contrôler les niveaux de volume du point de terminaison de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b9559-115">[EndpointVolume API](endpointvolume-api.md) to control volume levels of the device endpoint.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9559-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9559-116">Requirements</span></span>



| <span data-ttu-id="b9559-117">Produit</span><span class="sxs-lookup"><span data-stu-id="b9559-117">Product</span></span>                                                        | <span data-ttu-id="b9559-118">Version</span><span class="sxs-lookup"><span data-stu-id="b9559-118">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="b9559-119">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="b9559-119">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="b9559-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b9559-120">Windows 7</span></span> |
| <span data-ttu-id="b9559-121">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b9559-121">Visual Studio</span></span>                                                  | <span data-ttu-id="b9559-122">2008</span><span class="sxs-lookup"><span data-stu-id="b9559-122">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b9559-123">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-123">Downloading the Sample</span></span>

<span data-ttu-id="b9559-124">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="b9559-124">This sample is available in the following locations.</span></span>



| <span data-ttu-id="b9559-125">Emplacement</span><span class="sxs-lookup"><span data-stu-id="b9559-125">Location</span></span>    | <span data-ttu-id="b9559-126">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="b9559-126">Path/URL</span></span>                                                                                        |
|-------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9559-127">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="b9559-127">Windows SDK</span></span> | <span data-ttu-id="b9559-128">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ EndpointVolume \\ ...</span><span class="sxs-lookup"><span data-stu-id="b9559-128">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\EndpointVolume\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="b9559-129">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-129">Building the Sample</span></span>

<span data-ttu-id="b9559-130">Pour générer l’exemple x, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9559-130">To build the x sample, use the following steps:</span></span>

<span data-ttu-id="b9559-131">Pour générer l’exemple EndpointVolumeChanger, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b9559-131">To build the EndpointVolumeChanger sample, use the following steps:</span></span>

1.  <span data-ttu-id="b9559-132">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="b9559-132">Open the CMD shell for the Windows SDK and change to the EndpointVolume sample directory.</span></span>
2.  <span data-ttu-id="b9559-133">Exécutez la commande `start EndpointVolumeChanger.sln` dans le répertoire EndpointVolume pour ouvrir le projet EndpointVolumeChanger dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b9559-133">Run the command `start EndpointVolumeChanger.sln` in the EndpointVolume directory to open the EndpointVolumeChanger project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="b9559-134">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="b9559-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="b9559-135">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="b9559-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="b9559-136">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIEndpointVolume. vcproj.</span><span class="sxs-lookup"><span data-stu-id="b9559-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIEndpointVolume.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b9559-137">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="b9559-137">Running the Sample</span></span>

<span data-ttu-id="b9559-138">Si vous générez l’application de démonstration avec succès, un fichier exécutable, EndpointVolumeChanger.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="b9559-138">If you build the demo application successfully, an executable file, EndpointVolumeChanger.exe, is generated.</span></span> <span data-ttu-id="b9559-139">Pour l’exécuter, tapez `EndpointVolumeChanger` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="b9559-139">To run it, type `EndpointVolumeChanger` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="b9559-140">L’exemple suivant montre comment basculer le paramètre muet sur l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9559-140">The following example shows how to toggle the mute setting on the default console device.</span></span>

`EndpointVolumeChanger.exe -console -m`

<span data-ttu-id="b9559-141">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="b9559-141">The following table shows the arguments.</span></span>

| <span data-ttu-id="b9559-142">Argument</span><span class="sxs-lookup"><span data-stu-id="b9559-142">Argument</span></span>        | <span data-ttu-id="b9559-143">Description</span><span class="sxs-lookup"><span data-stu-id="b9559-143">Description</span></span>                                                         |
|-----------------|---------------------------------------------------------------------|
| <span data-ttu-id="b9559-144">-?</span><span class="sxs-lookup"><span data-stu-id="b9559-144">-?</span></span>              | <span data-ttu-id="b9559-145">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="b9559-145">Shows help.</span></span>                                                         |
| <span data-ttu-id="b9559-146">-H</span><span class="sxs-lookup"><span data-stu-id="b9559-146">-h</span></span>              | <span data-ttu-id="b9559-147">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="b9559-147">Shows help.</span></span>                                                         |
| -+              | <span data-ttu-id="b9559-148">Incrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.</span><span class="sxs-lookup"><span data-stu-id="b9559-148">Increments the volume level on audio endpoint device by one step.</span></span> <span data-ttu-id="b9559-149">.</span><span class="sxs-lookup"><span data-stu-id="b9559-149">.</span></span> |
| <span data-ttu-id="b9559-150">vers le haut</span><span class="sxs-lookup"><span data-stu-id="b9559-150">-up</span></span>             | <span data-ttu-id="b9559-151">Incrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.</span><span class="sxs-lookup"><span data-stu-id="b9559-151">Increments the volume level on audio endpoint device by one step.</span></span>   |
| --              | <span data-ttu-id="b9559-152">Décrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.</span><span class="sxs-lookup"><span data-stu-id="b9559-152">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="b9559-153">-vers le</span><span class="sxs-lookup"><span data-stu-id="b9559-153">-down</span></span>           | <span data-ttu-id="b9559-154">Décrémente le niveau de volume sur l’appareil de point de terminaison audio d’une étape.</span><span class="sxs-lookup"><span data-stu-id="b9559-154">Decrements the volume level on audio endpoint device by one step.</span></span>   |
| <span data-ttu-id="b9559-155">-v</span><span class="sxs-lookup"><span data-stu-id="b9559-155">-v</span></span>              | <span data-ttu-id="b9559-156">Définit le niveau de volume maître sur l’appareil de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="b9559-156">Sets the master volume level on the audio endpoint device.</span></span>          |
| <span data-ttu-id="b9559-157">-Console</span><span class="sxs-lookup"><span data-stu-id="b9559-157">-console</span></span>        | <span data-ttu-id="b9559-158">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9559-158">Use the default console device.</span></span>                                     |
| <span data-ttu-id="b9559-159">-Communications</span><span class="sxs-lookup"><span data-stu-id="b9559-159">-communications</span></span> | <span data-ttu-id="b9559-160">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9559-160">Use the default communication device.</span></span>                               |
| <span data-ttu-id="b9559-161">-multimédia</span><span class="sxs-lookup"><span data-stu-id="b9559-161">-multimedia</span></span>     | <span data-ttu-id="b9559-162">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="b9559-162">Use the default multimedia device.</span></span>                                  |
| <span data-ttu-id="b9559-163">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b9559-163">-endpoint</span></span>       | <span data-ttu-id="b9559-164">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="b9559-164">Use the endpoint identifier specified in the switch value.</span></span>          |



 

<span data-ttu-id="b9559-165">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil.</span><span class="sxs-lookup"><span data-stu-id="b9559-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device.</span></span> <span data-ttu-id="b9559-166">Une fois que l’utilisateur spécifie l’appareil, l’application affiche les paramètres actuels du volume pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="b9559-166">After the user specifies the device, the application displays the current volume settings for the endpoint.</span></span> <span data-ttu-id="b9559-167">Le volume peut être contrôlé à l’aide des commutateurs décrits dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="b9559-167">The volume can be controlled by using the switches described in the preceding table.</span></span>

<span data-ttu-id="b9559-168">Pour plus d’informations sur le contrôle des niveaux de volume des appareils de point de terminaison audio, consultez [API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="b9559-168">For more information about controlling the volume levels of audio endpoint devices, see [EndpointVolume API](endpointvolume-api.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9559-169">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9559-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9559-170">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="b9559-170">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



