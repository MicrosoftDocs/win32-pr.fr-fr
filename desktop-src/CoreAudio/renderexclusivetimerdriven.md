---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur. Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif.
ms.assetid: 9dcfccd2-a709-4b4e-bbb3-4c68a15cce03
title: RenderExclusiveTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb6145f65de3de9425f7ba2f023a669ec0b57a3c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483481"
---
# <a name="renderexclusivetimerdriven"></a><span data-ttu-id="28281-104">RenderExclusiveTimerDriven</span><span class="sxs-lookup"><span data-stu-id="28281-104">RenderExclusiveTimerDriven</span></span>

<span data-ttu-id="28281-105">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28281-105">This sample application uses the Core Audio APIs to render audio data to an output device specified by the user.</span></span> <span data-ttu-id="28281-106">Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="28281-106">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="28281-107">Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="28281-107">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span>

<span data-ttu-id="28281-108">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="28281-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28281-109">Description</span><span class="sxs-lookup"><span data-stu-id="28281-109">Description</span></span>](#description)
-   [<span data-ttu-id="28281-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28281-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="28281-111">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="28281-111">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="28281-112">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="28281-112">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="28281-113">Afficher les fichiers d’exemple</span><span class="sxs-lookup"><span data-stu-id="28281-113">View the Sample Files</span></span>](#view-the-sample-files)
-   [<span data-ttu-id="28281-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28281-114">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="28281-115">Description</span><span class="sxs-lookup"><span data-stu-id="28281-115">Description</span></span>

<span data-ttu-id="28281-116">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="28281-116">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="28281-117">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="28281-117">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="28281-118">WASAPI pour les opérations de gestion de flux.</span><span class="sxs-lookup"><span data-stu-id="28281-118">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="28281-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28281-119">Requirements</span></span>



| <span data-ttu-id="28281-120">Produit</span><span class="sxs-lookup"><span data-stu-id="28281-120">Product</span></span>                                                        | <span data-ttu-id="28281-121">Version</span><span class="sxs-lookup"><span data-stu-id="28281-121">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="28281-122">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="28281-122">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="28281-123">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28281-123">Windows 7</span></span> |
| <span data-ttu-id="28281-124">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28281-124">Visual Studio</span></span>                                                  | <span data-ttu-id="28281-125">2008</span><span class="sxs-lookup"><span data-stu-id="28281-125">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="28281-126">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="28281-126">Downloading the Sample</span></span>

<span data-ttu-id="28281-127">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="28281-127">This sample is available in the following locations.</span></span>



| <span data-ttu-id="28281-128">Emplacement</span><span class="sxs-lookup"><span data-stu-id="28281-128">Location</span></span>    | <span data-ttu-id="28281-129">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="28281-129">Path/URL</span></span>                                                                                                    |
|-------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28281-130">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="28281-130">Windows SDK</span></span> | <span data-ttu-id="28281-131">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ RenderExclusiveTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="28281-131">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderExclusiveTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="28281-132">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="28281-132">Building the Sample</span></span>

<span data-ttu-id="28281-133">Pour générer l’exemple RenderExclusiveTimerDriven, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="28281-133">To build the RenderExclusiveTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="28281-134">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="28281-134">Open the CMD shell for the Windows SDK and change to the RenderExclusiveTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="28281-135">Exécutez la commande `start WASAPIRenderExclusiveTimerDriven.sln` dans le répertoire RenderExclusiveTimerDriven pour ouvrir le projet WASAPIRenderExclusiveTimerDriven dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="28281-135">Run the command `start WASAPIRenderExclusiveTimerDriven.sln` in the RenderExclusiveTimerDriven directory to open the WASAPIRenderExclusiveTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="28281-136">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="28281-136">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="28281-137">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="28281-137">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="28281-138">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderExclusiveTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="28281-138">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderExclusiveTimerDriven.vcproj.</span></span>

## <a name="view-the-sample-files"></a><span data-ttu-id="28281-139">Afficher les fichiers d’exemple</span><span class="sxs-lookup"><span data-stu-id="28281-139">View the Sample Files</span></span>

<span data-ttu-id="28281-140">Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderExclusiveTimerDriven.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="28281-140">If you build the demo application successfully, an executable file, WASAPIRenderExclusiveTimerDriven.exe, is generated.</span></span> <span data-ttu-id="28281-141">Pour l’exécuter, tapez `WASAPIRenderExclusiveTimerDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="28281-141">To run it, type `WASAPIRenderExclusiveTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="28281-142">L’exemple suivant montre comment exécuter l’exemple en spécifiant une durée de lecture sur l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="28281-142">The following example shows how to run the sample by a specifying playback duration on the default console device.</span></span>

`WASAPIRenderExclusiveTimerDriven.exe -d 20 -console`

<span data-ttu-id="28281-143">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="28281-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="28281-144">Argument</span><span class="sxs-lookup"><span data-stu-id="28281-144">Argument</span></span>        | <span data-ttu-id="28281-145">Description</span><span class="sxs-lookup"><span data-stu-id="28281-145">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="28281-146">-?</span><span class="sxs-lookup"><span data-stu-id="28281-146">-?</span></span>              | <span data-ttu-id="28281-147">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="28281-147">Shows help.</span></span>                                                |
| <span data-ttu-id="28281-148">-H</span><span class="sxs-lookup"><span data-stu-id="28281-148">-h</span></span>              | <span data-ttu-id="28281-149">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="28281-149">Shows help.</span></span>                                                |
| <span data-ttu-id="28281-150">-f</span><span class="sxs-lookup"><span data-stu-id="28281-150">-f</span></span>              | <span data-ttu-id="28281-151">Fréquence des vagues sinusoïdales en Hz.</span><span class="sxs-lookup"><span data-stu-id="28281-151">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="28281-152">-l</span><span class="sxs-lookup"><span data-stu-id="28281-152">-l</span></span>              | <span data-ttu-id="28281-153">Latence du rendu audio en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="28281-153">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="28281-154">-d</span><span class="sxs-lookup"><span data-stu-id="28281-154">-d</span></span>              | <span data-ttu-id="28281-155">Durée de l’onde sinusoïdale en secondes.</span><span class="sxs-lookup"><span data-stu-id="28281-155">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="28281-156">-M</span><span class="sxs-lookup"><span data-stu-id="28281-156">-m</span></span>              | <span data-ttu-id="28281-157">Désactive l’utilisation de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="28281-157">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="28281-158">-Console</span><span class="sxs-lookup"><span data-stu-id="28281-158">-console</span></span>        | <span data-ttu-id="28281-159">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="28281-159">Use the default console device.</span></span>                            |
| <span data-ttu-id="28281-160">-Communications</span><span class="sxs-lookup"><span data-stu-id="28281-160">-communications</span></span> | <span data-ttu-id="28281-161">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="28281-161">Use the default communication device.</span></span>                      |
| <span data-ttu-id="28281-162">-multimédia</span><span class="sxs-lookup"><span data-stu-id="28281-162">-multimedia</span></span>     | <span data-ttu-id="28281-163">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="28281-163">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="28281-164">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="28281-164">-endpoint</span></span>       | <span data-ttu-id="28281-165">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="28281-165">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="28281-166">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de rendu.</span><span class="sxs-lookup"><span data-stu-id="28281-166">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="28281-167">Une fois que l’utilisateur a spécifié un appareil, l’application affiche une vague sinusoïdale à 440 Hz pendant 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="28281-167">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="28281-168">Ces valeurs peuvent être modifiées en spécifiant des valeurs de commutateur-f et-d.</span><span class="sxs-lookup"><span data-stu-id="28281-168">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="28281-169">RenderExclusiveTimerDriven illustre la mise en mémoire tampon pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="28281-169">RenderExclusiveTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="28281-170">Dans ce mode, le client doit attendre pendant une période donnée (la moitié de la latence, spécifiée par la valeur du commutateur-d, en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="28281-170">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="28281-171">Lorsque le client sort de la période de traitement, il extrait le jeu d’exemples suivant du moteur.</span><span class="sxs-lookup"><span data-stu-id="28281-171">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="28281-172">Avant chaque passage de traitement dans la boucle de mise en mémoire tampon, le client doit déterminer la quantité de données à afficher afin que les données ne saturent pas la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="28281-172">Before each processing pass in the buffering loop, the client must find out the amount of data to render so that the data does not overrun the buffer.</span></span>

<span data-ttu-id="28281-173">Les données audio à lire sur l’appareil spécifié peuvent être traitées en activant la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="28281-173">Audio data to be played on the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="28281-174">Ce mode est illustré dans l’exemple RenderExclusiveTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="28281-174">This mode is demonstrated in the RenderExclusiveTimerDriven sample.</span></span>

<span data-ttu-id="28281-175">Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="28281-175">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28281-176">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28281-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28281-177">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="28281-177">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



