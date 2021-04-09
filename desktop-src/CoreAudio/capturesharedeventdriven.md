---
description: Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif. Cet exemple illustre la mise en mémoire tampon pilotée par les événements.
ms.assetid: 6ff3bc23-550e-41b7-b37c-35d552b29e20
title: CaptureSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 339bd02fcb94f65be558c2dce767747ebf4fab98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110790"
---
# <a name="capturesharedeventdriven"></a><span data-ttu-id="d4cf7-104">CaptureSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="d4cf7-104">CaptureSharedEventDriven</span></span>

<span data-ttu-id="d4cf7-105">Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée spécifié par l’utilisateur et les écrit dans un fichier. wav portant un nom unique dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-105">This sample application uses the Core Audio APIs to capture audio data from an input device specified by the user and writes it to a uniquely named .wav file in the current directory.</span></span> <span data-ttu-id="d4cf7-106">Cet exemple illustre la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-106">This sample demonstrates event-driven buffering.</span></span>

<span data-ttu-id="d4cf7-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d4cf7-108">Description</span><span class="sxs-lookup"><span data-stu-id="d4cf7-108">Description</span></span>](#description)
-   [<span data-ttu-id="d4cf7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4cf7-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d4cf7-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d4cf7-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d4cf7-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d4cf7-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4cf7-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="d4cf7-114">Description</span><span class="sxs-lookup"><span data-stu-id="d4cf7-114">Description</span></span>

<span data-ttu-id="d4cf7-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="d4cf7-116">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="d4cf7-117">[WASAPI](wasapi.md) pour les opérations de gestion de flux, telles que le démarrage et l’arrêt du flux et le basculement de flux.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, and stream switching.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4cf7-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4cf7-118">Requirements</span></span>



| <span data-ttu-id="d4cf7-119">Produit</span><span class="sxs-lookup"><span data-stu-id="d4cf7-119">Product</span></span>                                                        | <span data-ttu-id="d4cf7-120">Version</span><span class="sxs-lookup"><span data-stu-id="d4cf7-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="d4cf7-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="d4cf7-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="d4cf7-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d4cf7-122">Windows 7</span></span> |
| <span data-ttu-id="d4cf7-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4cf7-123">Visual Studio</span></span>                                                  | <span data-ttu-id="d4cf7-124">2008</span><span class="sxs-lookup"><span data-stu-id="d4cf7-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d4cf7-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-125">Downloading the Sample</span></span>

<span data-ttu-id="d4cf7-126">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="d4cf7-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="d4cf7-127">Location</span></span>    | <span data-ttu-id="d4cf7-128">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="d4cf7-128">Path/URL</span></span>                                                                                                  |
|-------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4cf7-129">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="d4cf7-129">Windows SDK</span></span> | <span data-ttu-id="d4cf7-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ CaptureSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="d4cf7-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\CaptureSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="d4cf7-131">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-131">Building the Sample</span></span>

<span data-ttu-id="d4cf7-132">Pour générer l’exemple CaptureSharedEventDriven, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d4cf7-132">To build the CaptureSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="d4cf7-133">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple CaptureSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-133">Open the CMD shell for the Windows SDK and change to the CaptureSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="d4cf7-134">Exécutez la commande `start WASAPICaptureSharedEventDriven.sln` dans le répertoire CaptureSharedEventDriven pour ouvrir le projet WASAPICaptureSharedEventDriven dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-134">Run the command `start WASAPICaptureSharedEventDriven.sln` in the CaptureSharedEventDriven directory to open the WASAPICaptureSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="d4cf7-135">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="d4cf7-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="d4cf7-136">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="d4cf7-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="d4cf7-137">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPICaptureSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPICaptureSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d4cf7-138">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="d4cf7-138">Running the Sample</span></span>

<span data-ttu-id="d4cf7-139">Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPICaptureSharedEventDriven.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-139">If you build the demo application successfully, an executable file, WASAPICaptureSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="d4cf7-140">Pour l’exécuter, tapez `WASAPICaptureSharedEventDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-140">To run it, type `WASAPICaptureSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="d4cf7-141">L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de capture sur le périphérique multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-141">The following example shows how to run the sample by specifying capture duration on the default multimedia device.</span></span>

`WASAPICaptureSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="d4cf7-142">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="d4cf7-143">Argument</span><span class="sxs-lookup"><span data-stu-id="d4cf7-143">Argument</span></span>        | <span data-ttu-id="d4cf7-144">Description</span><span class="sxs-lookup"><span data-stu-id="d4cf7-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="d4cf7-145">-?</span><span class="sxs-lookup"><span data-stu-id="d4cf7-145">-?</span></span>              | <span data-ttu-id="d4cf7-146">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-146">Shows help.</span></span>                                                |
| <span data-ttu-id="d4cf7-147">-H</span><span class="sxs-lookup"><span data-stu-id="d4cf7-147">-h</span></span>              | <span data-ttu-id="d4cf7-148">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-148">Shows help.</span></span>                                                |
| <span data-ttu-id="d4cf7-149">-l</span><span class="sxs-lookup"><span data-stu-id="d4cf7-149">-l</span></span>              | <span data-ttu-id="d4cf7-150">Latence de capture audio en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-150">Audio capture latency in milliseconds.</span></span>                     |
| <span data-ttu-id="d4cf7-151">-d</span><span class="sxs-lookup"><span data-stu-id="d4cf7-151">-d</span></span>              | <span data-ttu-id="d4cf7-152">Durée de capture audio en secondes.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-152">Audio capture duration in seconds.</span></span>                         |
| <span data-ttu-id="d4cf7-153">-M</span><span class="sxs-lookup"><span data-stu-id="d4cf7-153">-m</span></span>              | <span data-ttu-id="d4cf7-154">Désactive l’utilisation de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-154">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="d4cf7-155">-Console</span><span class="sxs-lookup"><span data-stu-id="d4cf7-155">-console</span></span>        | <span data-ttu-id="d4cf7-156">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-156">Use the default console device.</span></span>                            |
| <span data-ttu-id="d4cf7-157">-Communications</span><span class="sxs-lookup"><span data-stu-id="d4cf7-157">-communications</span></span> | <span data-ttu-id="d4cf7-158">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-158">Use the default communication device.</span></span>                      |
| <span data-ttu-id="d4cf7-159">-multimédia</span><span class="sxs-lookup"><span data-stu-id="d4cf7-159">-multimedia</span></span>     | <span data-ttu-id="d4cf7-160">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-160">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="d4cf7-161">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d4cf7-161">-endpoint</span></span>       | <span data-ttu-id="d4cf7-162">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-162">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="d4cf7-163">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de capture.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-163">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the capture session.</span></span> <span data-ttu-id="d4cf7-164">La console, la communication et les périphériques multimédias par défaut sont répertoriés suivis des appareils et des identificateurs de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-164">The default console, communication, and multimedia devices are listed followed by devices and the endpoint identifiers.</span></span> <span data-ttu-id="d4cf7-165">Si aucune durée n’est spécifiée, le flux audio de l’appareil spécifié est capturé pendant 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-165">If no duration is specified, the audio stream from the specified device is captured for 10 seconds.</span></span> <span data-ttu-id="d4cf7-166">L’application écrit les données capturées dans un fichier. wav portant un nom unique.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-166">The application writes the captured data to a uniquely named .wav file.</span></span>

<span data-ttu-id="d4cf7-167">CaptureSharedEventDriven illustre la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-167">CaptureSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="d4cf7-168">Le client audio instancié pour cet exemple est configuré pour s’exécuter en mode partagé et le traitement du client de la mémoire tampon audio est rendu déclenché par l’événement en définissant l’indicateur **AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante** dans l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="d4cf7-168">The audio client instantiated for this sample is configured to run in shared mode and the client's processing of the audio buffer is made event driven by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span> <span data-ttu-id="d4cf7-169">L’exemple montre comment le client doit fournir un handle d’événement au système en appelant la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="d4cf7-169">The sample shows how the client must provide an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span> <span data-ttu-id="d4cf7-170">Après le début de la session de capture et le démarrage du flux, le moteur audio signale le handle d’événement fourni pour notifier le client chaque fois qu’une mémoire tampon est prête à être traitée par le client.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-170">After the capture session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="d4cf7-171">Les données audio peuvent également être traitées dans une boucle pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="d4cf7-171">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="d4cf7-172">Ce mode est demostrated dans l’exemple [CaptureSharedTimerDriven](capturesharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="d4cf7-172">This mode is demostrated in the [CaptureSharedTimerDriven](capturesharedtimerdriven.md) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4cf7-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d4cf7-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4cf7-174">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="d4cf7-174">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



