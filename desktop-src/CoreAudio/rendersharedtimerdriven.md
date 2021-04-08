---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur.
ms.assetid: eae7d896-77ef-4340-bd77-1f3333166987
title: RenderSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4ce441a12d65b8bebb843c7b9a168443b34592
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748540"
---
# <a name="rendersharedtimerdriven"></a><span data-ttu-id="96828-103">RenderSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="96828-103">RenderSharedTimerDriven</span></span>

<span data-ttu-id="96828-104">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96828-104">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="96828-105">Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="96828-105">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="96828-106">Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="96828-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="96828-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="96828-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="96828-108">Description</span><span class="sxs-lookup"><span data-stu-id="96828-108">Description</span></span>](#description)
-   [<span data-ttu-id="96828-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96828-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="96828-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="96828-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="96828-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="96828-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="96828-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="96828-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="96828-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96828-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="96828-114">Description</span><span class="sxs-lookup"><span data-stu-id="96828-114">Description</span></span>

<span data-ttu-id="96828-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="96828-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="96828-116">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="96828-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="96828-117">WASAPI pour les opérations de gestion de flux.</span><span class="sxs-lookup"><span data-stu-id="96828-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="96828-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96828-118">Requirements</span></span>



| <span data-ttu-id="96828-119">Produit</span><span class="sxs-lookup"><span data-stu-id="96828-119">Product</span></span>                                                        | <span data-ttu-id="96828-120">Version</span><span class="sxs-lookup"><span data-stu-id="96828-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="96828-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="96828-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="96828-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="96828-122">Windows 7</span></span> |
| <span data-ttu-id="96828-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="96828-123">Visual Studio</span></span>                                                  | <span data-ttu-id="96828-124">2008</span><span class="sxs-lookup"><span data-stu-id="96828-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="96828-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="96828-125">Downloading the Sample</span></span>

<span data-ttu-id="96828-126">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="96828-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="96828-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="96828-127">Location</span></span>    | <span data-ttu-id="96828-128">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="96828-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96828-129">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="96828-129">Windows SDK</span></span> | <span data-ttu-id="96828-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ RenderSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="96828-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="96828-131">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="96828-131">Building the Sample</span></span>

<span data-ttu-id="96828-132">Pour générer l’exemple RenderSharedTimerDriven, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="96828-132">To build the RenderSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="96828-133">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="96828-133">Open the CMD shell for the Windows SDK and change to the RenderSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="96828-134">Exécutez la commande `start WASAPIRenderSharedTimerDriven.sln` dans le répertoire RenderSharedTimerDriven pour ouvrir le projet WASAPIRenderSharedTimerDriven dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="96828-134">Run the command `start WASAPIRenderSharedTimerDriven.sln` in the RenderSharedTimerDriven directory to open the WASAPIRenderSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="96828-135">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="96828-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="96828-136">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="96828-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="96828-137">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="96828-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="96828-138">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="96828-138">Running the Sample</span></span>

<span data-ttu-id="96828-139">Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderSharedTimerDriven.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="96828-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="96828-140">Pour l’exécuter, tapez `WASAPIRenderSharedTimerDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="96828-140">To run it, type `WASAPIRenderSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="96828-141">L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de lecture sur le périphérique multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="96828-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="96828-142">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="96828-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="96828-143">Argument</span><span class="sxs-lookup"><span data-stu-id="96828-143">Argument</span></span>        | <span data-ttu-id="96828-144">Description</span><span class="sxs-lookup"><span data-stu-id="96828-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="96828-145">-?</span><span class="sxs-lookup"><span data-stu-id="96828-145">-?</span></span>              | <span data-ttu-id="96828-146">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="96828-146">Shows help.</span></span>                                                |
| <span data-ttu-id="96828-147">-H</span><span class="sxs-lookup"><span data-stu-id="96828-147">-h</span></span>              | <span data-ttu-id="96828-148">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="96828-148">Shows help.</span></span>                                                |
| <span data-ttu-id="96828-149">-f</span><span class="sxs-lookup"><span data-stu-id="96828-149">-f</span></span>              | <span data-ttu-id="96828-150">Fréquence des vagues sinusoïdales en Hz.</span><span class="sxs-lookup"><span data-stu-id="96828-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="96828-151">-l</span><span class="sxs-lookup"><span data-stu-id="96828-151">-l</span></span>              | <span data-ttu-id="96828-152">Latence du rendu audio en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="96828-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="96828-153">-d</span><span class="sxs-lookup"><span data-stu-id="96828-153">-d</span></span>              | <span data-ttu-id="96828-154">Durée de l’onde sinusoïdale en secondes.</span><span class="sxs-lookup"><span data-stu-id="96828-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="96828-155">-M</span><span class="sxs-lookup"><span data-stu-id="96828-155">-m</span></span>              | <span data-ttu-id="96828-156">Désactive l’utilisation de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="96828-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="96828-157">-Console</span><span class="sxs-lookup"><span data-stu-id="96828-157">-console</span></span>        | <span data-ttu-id="96828-158">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="96828-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="96828-159">-Communications</span><span class="sxs-lookup"><span data-stu-id="96828-159">-communications</span></span> | <span data-ttu-id="96828-160">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="96828-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="96828-161">-multimédia</span><span class="sxs-lookup"><span data-stu-id="96828-161">-multimedia</span></span>     | <span data-ttu-id="96828-162">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="96828-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="96828-163">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="96828-163">-endpoint</span></span>       | <span data-ttu-id="96828-164">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="96828-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="96828-165">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de rendu.</span><span class="sxs-lookup"><span data-stu-id="96828-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="96828-166">Une fois que l’utilisateur a spécifié un appareil, l’application affiche une vague sinusoïdale à 440 Hz pendant 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="96828-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="96828-167">Ces valeurs peuvent être modifiées en spécifiant des valeurs de commutateur-f et-d.</span><span class="sxs-lookup"><span data-stu-id="96828-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="96828-168">RenderSharedTimerDriven illustre la mise en mémoire tampon pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="96828-168">RenderSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="96828-169">Dans ce mode, le client doit attendre pendant une période donnée (la moitié de la latence, spécifiée par la valeur du commutateur-d, en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="96828-169">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="96828-170">Lorsque le client sort de la période de traitement, il extrait le jeu d’exemples suivant du moteur.</span><span class="sxs-lookup"><span data-stu-id="96828-170">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="96828-171">Avant chaque passage de traitement dans la boucle de mise en mémoire tampon, le client doit déterminer la quantité de données à afficher afin que les données ne saturent pas la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="96828-171">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="96828-172">Les données audio à lire sur l’appareil spécifié peuvent être traitées en activant la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="96828-172">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="96828-173">Ce mode est illustré dans l’exemple [RenderSharedEventDriven](rendersharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="96828-173">This mode is demonstrated in the [RenderSharedEventDriven](rendersharedeventdriven.md) sample.</span></span>

<span data-ttu-id="96828-174">Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="96828-174">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96828-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="96828-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96828-176">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="96828-176">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



