---
description: Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.
ms.assetid: 06124b99-89b3-4dfa-b989-a54746ecd697
title: CaptureSharedTimerDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b635462767f22d3e31fe6deaa79b5c00911b378b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033696"
---
# <a name="capturesharedtimerdriven"></a><span data-ttu-id="97917-104">CaptureSharedTimerDriven</span><span class="sxs-lookup"><span data-stu-id="97917-104">CaptureSharedTimerDriven</span></span>

<span data-ttu-id="97917-105">Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="97917-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="97917-106">Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="97917-106">This sample demonstrates timer-driven buffering.</span></span>

<span data-ttu-id="97917-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="97917-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="97917-108">Description</span><span class="sxs-lookup"><span data-stu-id="97917-108">Description</span></span>](#description)
-   [<span data-ttu-id="97917-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97917-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="97917-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="97917-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="97917-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="97917-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="97917-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="97917-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="97917-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97917-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="97917-114">Description</span><span class="sxs-lookup"><span data-stu-id="97917-114">Description</span></span>

<span data-ttu-id="97917-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="97917-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="97917-116">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="97917-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="97917-117">[WASAPI](wasapi.md) pour les opérations de gestion de flux.</span><span class="sxs-lookup"><span data-stu-id="97917-117">[WASAPI](wasapi.md) for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="97917-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97917-118">Requirements</span></span>



| <span data-ttu-id="97917-119">Produit</span><span class="sxs-lookup"><span data-stu-id="97917-119">Product</span></span>                                                        | <span data-ttu-id="97917-120">Version</span><span class="sxs-lookup"><span data-stu-id="97917-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="97917-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="97917-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="97917-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="97917-122">Windows 7</span></span> |
| <span data-ttu-id="97917-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="97917-123">Visual Studio</span></span>                                                  | <span data-ttu-id="97917-124">2008</span><span class="sxs-lookup"><span data-stu-id="97917-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="97917-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="97917-125">Downloading the Sample</span></span>

<span data-ttu-id="97917-126">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="97917-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="97917-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="97917-127">Location</span></span>    | <span data-ttu-id="97917-128">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="97917-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97917-129">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="97917-129">Windows SDK</span></span> | <span data-ttu-id="97917-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ CaptureSharedTimerDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="97917-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedTimerDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="97917-131">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="97917-131">Building the Sample</span></span>

<span data-ttu-id="97917-132">Pour générer l’exemple CaptureSharedTimerDriven, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="97917-132">To build the CaptureSharedTimerDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="97917-133">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple CaptureSharedTimerDriven.</span><span class="sxs-lookup"><span data-stu-id="97917-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedTimerDriven sample directory.</span></span>
2.  <span data-ttu-id="97917-134">Exécutez la commande `start WASAPICaptureSharedTimerDriven.sln` dans le répertoire CaptureSharedTimerDriven pour ouvrir le projet WASAPICaptureSharedTimerDriven dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="97917-134">Run the command `start WASAPICaptureSharedTimerDriven.sln` in the CaptureSharedTimerDriven directory to open the WASAPICaptureSharedTimerDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="97917-135">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="97917-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="97917-136">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="97917-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="97917-137">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPICaptureSharedTimerDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="97917-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedTimerDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="97917-138">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="97917-138">Running the Sample</span></span>

<span data-ttu-id="97917-139">Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPICaptureSharedTimerDriven.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="97917-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedTimerDriven.exe, is generated.</span></span> <span data-ttu-id="97917-140">Pour l’exécuter, tapez `WASAPICaptureSharedTimerDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="97917-140">To run it, type `WASAPICaptureSharedTimerDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="97917-141">L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de capture sur le périphérique multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="97917-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedTimerDriven.exe -d 20 -multimedia`

<span data-ttu-id="97917-142">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="97917-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="97917-143">Argument</span><span class="sxs-lookup"><span data-stu-id="97917-143">Argument</span></span>        | <span data-ttu-id="97917-144">Description</span><span class="sxs-lookup"><span data-stu-id="97917-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="97917-145">-?</span><span class="sxs-lookup"><span data-stu-id="97917-145">-?</span></span>              | <span data-ttu-id="97917-146">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="97917-146">Shows help.</span></span>                                                |
| <span data-ttu-id="97917-147">-H</span><span class="sxs-lookup"><span data-stu-id="97917-147">-h</span></span>              | <span data-ttu-id="97917-148">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="97917-148">Shows help.</span></span>                                                |
| <span data-ttu-id="97917-149">-l</span><span class="sxs-lookup"><span data-stu-id="97917-149">-l</span></span>              | <span data-ttu-id="97917-150">Latence de capture audio en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="97917-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="97917-151">-d</span><span class="sxs-lookup"><span data-stu-id="97917-151">-d</span></span>              | <span data-ttu-id="97917-152">Durée de capture audio en secondes.</span><span class="sxs-lookup"><span data-stu-id="97917-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="97917-153">-M</span><span class="sxs-lookup"><span data-stu-id="97917-153">-m</span></span>              | <span data-ttu-id="97917-154">Désactive l’utilisation de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="97917-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="97917-155">-Console</span><span class="sxs-lookup"><span data-stu-id="97917-155">-console</span></span>        | <span data-ttu-id="97917-156">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="97917-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="97917-157">-Communications</span><span class="sxs-lookup"><span data-stu-id="97917-157">-communications</span></span> | <span data-ttu-id="97917-158">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="97917-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="97917-159">-multimédia</span><span class="sxs-lookup"><span data-stu-id="97917-159">-multimedia</span></span>     | <span data-ttu-id="97917-160">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="97917-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="97917-161">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="97917-161">-endpoint</span></span>       | <span data-ttu-id="97917-162">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="97917-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="97917-163">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de capture.</span><span class="sxs-lookup"><span data-stu-id="97917-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="97917-164">La console, la communication et les périphériques multimédias par défaut sont répertoriés suivis des appareils et des identificateurs de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="97917-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="97917-165">Si aucune durée n’est spécifiée, le flux audio de l’appareil spécifié est capturé pendant 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="97917-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="97917-166">L’application écrit les données capturées dans un fichier. wav portant un nom unique.</span><span class="sxs-lookup"><span data-stu-id="97917-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="97917-167">CaptureSharedTimerDriven illustre la mise en mémoire tampon pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="97917-167">CaptureSharedTimerDriven demonstrates timer-driven buffering.</span></span> <span data-ttu-id="97917-168">Dans ce mode, le client doit attendre pendant une période donnée (la moitié de la latence, spécifiée par la valeur du commutateur-d, en millisecondes).</span><span class="sxs-lookup"><span data-stu-id="97917-168">In this mode, the client must wait for a period of time (half the latency, specified by the -d switch value, in milliseconds).</span></span> <span data-ttu-id="97917-169">Lorsque le client sort de la période de traitement, il extrait le jeu d’exemples suivant du moteur.</span><span class="sxs-lookup"><span data-stu-id="97917-169">When the client wakes up, half way through the processing period, it pulls the next set of samples from the engine.</span></span> <span data-ttu-id="97917-170">Avant chaque passage de traitement dans la boucle de mise en mémoire tampon, le client doit déterminer la quantité de données de capture disponibles afin que les données ne saturent pas le tampon de capture.</span><span class="sxs-lookup"><span data-stu-id="97917-170">Before each processing pass in the buffering loop, the client must find out the amount of capture data available so that the data does not overrun the capture buffer.</span></span> <span data-ttu-id="97917-171">Les données audio capturées à partir de l’appareil spécifié peuvent être traitées en activant la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="97917-171">The audio data that is captured from the specified device can be processed by enabling event-driven buffering.</span></span> <span data-ttu-id="97917-172">Ce mode est illustré dans l’exemple [CaptureSharedEventDriven](capturesharedeventdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="97917-172">This mode is demonstrated in the [CaptureSharedEventDriven](capturesharedeventdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97917-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97917-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97917-174">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="97917-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



