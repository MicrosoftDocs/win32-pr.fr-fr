---
description: Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.
ms.assetid: 92e644be-df8b-415d-ac8e-c0c30c85f844
title: RenderSharedEventDriven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9901896b962717ed72fd36d022eef9510d7cb916
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861302"
---
# <a name="rendersharedeventdriven"></a><span data-ttu-id="7914d-103">RenderSharedEventDriven</span><span class="sxs-lookup"><span data-stu-id="7914d-103">RenderSharedEventDriven</span></span>

<span data-ttu-id="7914d-104">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7914d-104">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="7914d-105">Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="7914d-105">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="7914d-106">Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="7914d-106">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span>

<span data-ttu-id="7914d-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="7914d-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7914d-108">Description</span><span class="sxs-lookup"><span data-stu-id="7914d-108">Description</span></span>](#description)
-   [<span data-ttu-id="7914d-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7914d-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7914d-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="7914d-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="7914d-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="7914d-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7914d-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="7914d-114">Description</span><span class="sxs-lookup"><span data-stu-id="7914d-114">Description</span></span>

<span data-ttu-id="7914d-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="7914d-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="7914d-116">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="7914d-116">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="7914d-117">WASAPI pour les opérations de gestion de flux.</span><span class="sxs-lookup"><span data-stu-id="7914d-117">WASAPI for stream management operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7914d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7914d-118">Requirements</span></span>



| <span data-ttu-id="7914d-119">Produit</span><span class="sxs-lookup"><span data-stu-id="7914d-119">Product</span></span>                                                        | <span data-ttu-id="7914d-120">Version</span><span class="sxs-lookup"><span data-stu-id="7914d-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="7914d-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="7914d-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="7914d-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7914d-122">Windows 7</span></span> |
| <span data-ttu-id="7914d-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7914d-123">Visual Studio</span></span>                                                  | <span data-ttu-id="7914d-124">2008</span><span class="sxs-lookup"><span data-stu-id="7914d-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="7914d-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-125">Downloading the Sample</span></span>

<span data-ttu-id="7914d-126">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="7914d-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="7914d-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="7914d-127">Location</span></span>    | <span data-ttu-id="7914d-128">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="7914d-128">Path/URL</span></span>                                                                                                 |
|-------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7914d-129">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="7914d-129">Windows SDK</span></span> | <span data-ttu-id="7914d-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ RenderSharedEventDriven \\ ...</span><span class="sxs-lookup"><span data-stu-id="7914d-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\RenderSharedEventDriven\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="7914d-131">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-131">Building the Sample</span></span>

<span data-ttu-id="7914d-132">Pour générer l’exemple RenderSharedEventDriven, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7914d-132">To build the RenderSharedEventDriven sample, use the following steps:</span></span>

1.  <span data-ttu-id="7914d-133">Ouvrez l’interpréteur de commandes pour le SDK Windows et accédez au répertoire d’exemple RenderSharedEventDriven.</span><span class="sxs-lookup"><span data-stu-id="7914d-133">Open the CMD shell for the Windows SDK and change to the RenderSharedEventDriven sample directory.</span></span>
2.  <span data-ttu-id="7914d-134">Exécutez la commande `start WASAPIRenderSharedEventDriven.sln` dans le répertoire RenderSharedEventDriven pour ouvrir le projet WASAPIRenderSharedEventDriven dans la fenêtre Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7914d-134">Run the command `start WASAPIRenderSharedEventDriven.sln` in the RenderSharedEventDriven directory to open the WASAPIRenderSharedEventDriven project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="7914d-135">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="7914d-135">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="7914d-136">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7914d-136">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="7914d-137">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, WASAPIRenderSharedEventDriven. vcproj.</span><span class="sxs-lookup"><span data-stu-id="7914d-137">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, WASAPIRenderSharedEventDriven.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7914d-138">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7914d-138">Running the Sample</span></span>

<span data-ttu-id="7914d-139">Si vous générez l’application de démonstration avec succès, un fichier exécutable, WASAPIRenderSharedEventDriven.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="7914d-139">If you build the demo application successfully, an executable file, WASAPIRenderSharedEventDriven.exe, is generated.</span></span> <span data-ttu-id="7914d-140">Pour l’exécuter, tapez `WASAPIRenderSharedEventDriven` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs.</span><span class="sxs-lookup"><span data-stu-id="7914d-140">To run it, type `WASAPIRenderSharedEventDriven` in a command window followed by required or optional arguments.</span></span> <span data-ttu-id="7914d-141">L’exemple suivant montre comment exécuter l’exemple en spécifiant la durée de lecture sur le périphérique multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="7914d-141">The following example shows how to run the sample by specifying playback duration on the default multimedia device.</span></span>

`WASAPIRenderSharedEventDriven.exe -d 20 -multimedia`

<span data-ttu-id="7914d-142">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="7914d-142">The following table shows the arguments.</span></span>

| <span data-ttu-id="7914d-143">Argument</span><span class="sxs-lookup"><span data-stu-id="7914d-143">Argument</span></span>        | <span data-ttu-id="7914d-144">Description</span><span class="sxs-lookup"><span data-stu-id="7914d-144">Description</span></span>                                                |
|-----------------|------------------------------------------------------------|
| <span data-ttu-id="7914d-145">-?</span><span class="sxs-lookup"><span data-stu-id="7914d-145">-?</span></span>              | <span data-ttu-id="7914d-146">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="7914d-146">Shows help.</span></span>                                                |
| <span data-ttu-id="7914d-147">-H</span><span class="sxs-lookup"><span data-stu-id="7914d-147">-h</span></span>              | <span data-ttu-id="7914d-148">Affiche l’aide.</span><span class="sxs-lookup"><span data-stu-id="7914d-148">Shows help.</span></span>                                                |
| <span data-ttu-id="7914d-149">-f</span><span class="sxs-lookup"><span data-stu-id="7914d-149">-f</span></span>              | <span data-ttu-id="7914d-150">Fréquence des vagues sinusoïdales en Hz.</span><span class="sxs-lookup"><span data-stu-id="7914d-150">Sine wave frequency in Hz.</span></span>                                 |
| <span data-ttu-id="7914d-151">-l</span><span class="sxs-lookup"><span data-stu-id="7914d-151">-l</span></span>              | <span data-ttu-id="7914d-152">Latence du rendu audio en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="7914d-152">Audio render latency in milliseconds.</span></span>                      |
| <span data-ttu-id="7914d-153">-d</span><span class="sxs-lookup"><span data-stu-id="7914d-153">-d</span></span>              | <span data-ttu-id="7914d-154">Durée de l’onde sinusoïdale en secondes.</span><span class="sxs-lookup"><span data-stu-id="7914d-154">Sine wave duration in seconds.</span></span>                             |
| <span data-ttu-id="7914d-155">-M</span><span class="sxs-lookup"><span data-stu-id="7914d-155">-m</span></span>              | <span data-ttu-id="7914d-156">Désactive l’utilisation de MMCSS.</span><span class="sxs-lookup"><span data-stu-id="7914d-156">Disables the use of MMCSS.</span></span>                                 |
| <span data-ttu-id="7914d-157">-Console</span><span class="sxs-lookup"><span data-stu-id="7914d-157">-console</span></span>        | <span data-ttu-id="7914d-158">Utilisez l’appareil de la console par défaut.</span><span class="sxs-lookup"><span data-stu-id="7914d-158">Use the default console device.</span></span>                            |
| <span data-ttu-id="7914d-159">-Communications</span><span class="sxs-lookup"><span data-stu-id="7914d-159">-communications</span></span> | <span data-ttu-id="7914d-160">Utilisez l’appareil de communication par défaut.</span><span class="sxs-lookup"><span data-stu-id="7914d-160">Use the default communication device.</span></span>                      |
| <span data-ttu-id="7914d-161">-multimédia</span><span class="sxs-lookup"><span data-stu-id="7914d-161">-multimedia</span></span>     | <span data-ttu-id="7914d-162">Utilisez l’appareil multimédia par défaut.</span><span class="sxs-lookup"><span data-stu-id="7914d-162">Use the default multimedia device.</span></span>                         |
| <span data-ttu-id="7914d-163">-point de terminaison</span><span class="sxs-lookup"><span data-stu-id="7914d-163">-endpoint</span></span>       | <span data-ttu-id="7914d-164">Utilisez l’identificateur de point de terminaison spécifié dans la valeur de commutateur.</span><span class="sxs-lookup"><span data-stu-id="7914d-164">Use the endpoint identifier specified in the switch value.</span></span> |



 

<span data-ttu-id="7914d-165">Si l’application est exécutée sans arguments, elle énumère les périphériques disponibles et invite l’utilisateur à sélectionner un appareil pour la session de rendu.</span><span class="sxs-lookup"><span data-stu-id="7914d-165">If the application is run without arguments, it enumerates the available devices and prompts the user to select a device for the rendering session.</span></span> <span data-ttu-id="7914d-166">Une fois que l’utilisateur a spécifié un appareil, l’application affiche une vague sinusoïdale à 440 Hz pendant 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="7914d-166">After the user specifies a device, the application renders a sine wave at 440 Hz for 10 seconds.</span></span> <span data-ttu-id="7914d-167">Ces valeurs peuvent être modifiées en spécifiant des valeurs de commutateur-f et-d.</span><span class="sxs-lookup"><span data-stu-id="7914d-167">These values can be modified by specifying -f and -d switch values.</span></span>

<span data-ttu-id="7914d-168">RenderSharedEventDriven illustre la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="7914d-168">RenderSharedEventDriven demonstrates event-driven buffering.</span></span> <span data-ttu-id="7914d-169">L’exemple montre comment effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7914d-169">The sample shows how to:</span></span>

-   <span data-ttu-id="7914d-170">Instanciez un client audio, configurez-le pour qu’il s’exécute en mode exclusif et activez la mise en mémoire tampon pilotée par les événements en définissant l’indicateur **AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante** dans l’appel à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span><span class="sxs-lookup"><span data-stu-id="7914d-170">Instantiate an audio client, configure it to run in exclusive mode, and enable event-driven buffering by setting the **AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK** flag in the call to [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).</span></span>
-   <span data-ttu-id="7914d-171">Associez le client aux exemples qui sont prêts à être rendus en fournissant un handle d’événement au système en appelant la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) .</span><span class="sxs-lookup"><span data-stu-id="7914d-171">Associate the client with the samples that are ready to be rendered by providing an event handle to the system by calling the [**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) method.</span></span>
-   <span data-ttu-id="7914d-172">Créez un thread de rendu pour effectuer des exemples de traitement à partir du moteur audio.</span><span class="sxs-lookup"><span data-stu-id="7914d-172">Create a render thread to proces samples from the audio engine.</span></span>
-   <span data-ttu-id="7914d-173">Vérifiez le format Mix du point de terminaison de l’appareil pour déterminer si les exemples peuvent être rendus.</span><span class="sxs-lookup"><span data-stu-id="7914d-173">Check the mix format of the device endpoint to determine whether the samples can be rendered.</span></span> <span data-ttu-id="7914d-174">Si l’appareil ne prend pas en charge le format Mix, les données sont converties en PCM.</span><span class="sxs-lookup"><span data-stu-id="7914d-174">If the device does not support the mix format, the data is converted to PCM.</span></span>
-   <span data-ttu-id="7914d-175">Gérer le basculement de flux.</span><span class="sxs-lookup"><span data-stu-id="7914d-175">Handle stream switching.</span></span>

<span data-ttu-id="7914d-176">Après le début de la session de rendu et le démarrage du flux, le moteur audio signale le handle d’événement fourni pour notifier le client chaque fois qu’une mémoire tampon est prête pour le traitement du client.</span><span class="sxs-lookup"><span data-stu-id="7914d-176">After the rendering session begins and the stream starts, the audio engine signals the supplied event handle to notify the client each time a buffer becomes ready for the client to process.</span></span> <span data-ttu-id="7914d-177">Les données audio peuvent également être traitées dans une boucle pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="7914d-177">The audio data can also be processed in a timer-driven loop.</span></span> <span data-ttu-id="7914d-178">Ce mode est illustré dans l’exemple [RenderSharedTimerDriven](rendersharedtimerdriven.md) .</span><span class="sxs-lookup"><span data-stu-id="7914d-178">This mode is demonstrated in the [RenderSharedTimerDriven](rendersharedtimerdriven.md) sample.</span></span>

<span data-ttu-id="7914d-179">Pour plus d’informations sur le rendu d’un flux, consultez [rendu d’un flux](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="7914d-179">For more information about rendering a stream, see [Rendering a Stream](rendering-a-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7914d-180">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7914d-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7914d-181">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="7914d-181">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



