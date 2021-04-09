---
description: Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux.
ms.assetid: 9a2131b2-ec4a-492a-a277-bd26ec8d67e5
title: DuckingCaptureSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 636fe39e8fa27beee14ab17548f5929d1d937b20
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861690"
---
# <a name="duckingcapturesample"></a><span data-ttu-id="90b57-103">DuckingCaptureSample</span><span class="sxs-lookup"><span data-stu-id="90b57-103">DuckingCaptureSample</span></span>

<span data-ttu-id="90b57-104">Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux.</span><span class="sxs-lookup"><span data-stu-id="90b57-104">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="90b57-105">Cette application implémente un client de conversation qui utilise des API audio de base pour lire les données audio à partir d’un périphérique de communication et les lire sur le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="90b57-105">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span>

<span data-ttu-id="90b57-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="90b57-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="90b57-107">Description</span><span class="sxs-lookup"><span data-stu-id="90b57-107">Description</span></span>](#description)
-   [<span data-ttu-id="90b57-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b57-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="90b57-109">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="90b57-110">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="90b57-111">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="90b57-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90b57-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="90b57-113">Description</span><span class="sxs-lookup"><span data-stu-id="90b57-113">Description</span></span>

<span data-ttu-id="90b57-114">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="90b57-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="90b57-115">[API MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="90b57-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="90b57-116">[WASAPI](wasapi.md) permettant d’accéder à la capture de communications et à l’appareil de rendu, aux opérations de gestion de flux et à la gestion des événements de canard.</span><span class="sxs-lookup"><span data-stu-id="90b57-116">[WASAPI](wasapi.md) for accessing the communications capture and render device, stream management operations, and handling ducking events.</span></span>
-   <span data-ttu-id="90b57-117">[API Wave](/previous-versions//ms713499(v=vs.85)) permettant d’accéder au périphérique de communication et de capturer l’entrée audio.</span><span class="sxs-lookup"><span data-stu-id="90b57-117">[WAVE APIs](/previous-versions//ms713499(v=vs.85)) for accessing the communications device and capturing audio input.</span></span>

## <a name="requirements"></a><span data-ttu-id="90b57-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b57-118">Requirements</span></span>



| <span data-ttu-id="90b57-119">Produit</span><span class="sxs-lookup"><span data-stu-id="90b57-119">Product</span></span>                                                        | <span data-ttu-id="90b57-120">Version</span><span class="sxs-lookup"><span data-stu-id="90b57-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="90b57-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="90b57-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="90b57-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90b57-122">Windows 7</span></span> |
| <span data-ttu-id="90b57-123">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="90b57-123">Visual Studio 2008</span></span>                                             |           |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="90b57-124">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-124">Downloading the Sample</span></span>

<span data-ttu-id="90b57-125">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="90b57-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="90b57-126">Emplacement</span><span class="sxs-lookup"><span data-stu-id="90b57-126">Location</span></span>    | <span data-ttu-id="90b57-127">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="90b57-127">Path/URL</span></span>                                                                                              |
|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90b57-128">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="90b57-128">Windows SDK</span></span> | <span data-ttu-id="90b57-129">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ DuckingCaptureSample \\ ...</span><span class="sxs-lookup"><span data-stu-id="90b57-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingCaptureSample\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="90b57-130">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-130">Building the Sample</span></span>

<span data-ttu-id="90b57-131">Pour générer l’exemple DuckingCaptureSample, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="90b57-131">To build the DuckingCaptureSample sample, use the following steps:</span></span>

1.  <span data-ttu-id="90b57-132">Ouvrez DuckingCaptureSample. sln dans Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="90b57-132">Open the DuckingCaptureSample.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="90b57-133">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="90b57-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="90b57-134">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="90b57-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="90b57-135">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, DuckingCaptureSample. vcproj.</span><span class="sxs-lookup"><span data-stu-id="90b57-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingCaptureSample.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="90b57-136">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="90b57-136">Running the Sample</span></span>

<span data-ttu-id="90b57-137">Si vous générez l’application avec succès, un fichier exécutable, DuckingCaptureSample.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="90b57-137">If you build the application successfully, an executable file, DuckingCaptureSample.exe, is generated.</span></span> <span data-ttu-id="90b57-138">Pour l’exécuter, sélectionnez **Démarrer le débogage** ou **Démarrer sans débogage** dans le menu **Déboguer** ou tapez `DuckingCaptureSample` dans une fenêtre de commande.</span><span class="sxs-lookup"><span data-stu-id="90b57-138">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingCaptureSample` in a command window.</span></span>

<span data-ttu-id="90b57-139">DuckingCaptureSample fournit à l’utilisateur deux implémentations pour capturer l’audio de l’appareil de console par défaut : les API WASAPI et Wave.</span><span class="sxs-lookup"><span data-stu-id="90b57-139">DuckingCaptureSample provides the user with two implementations to capture audio from the default console device: WASAPI and Wave APIs.</span></span> <span data-ttu-id="90b57-140">Pour démarrer une session de capture, sélectionnez un mode, puis cliquez sur **Démarrer** dans l’interface utilisateur de l’application.</span><span class="sxs-lookup"><span data-stu-id="90b57-140">To start a capture session, select a mode and click **Start** on the application's user interface.</span></span> <span data-ttu-id="90b57-141">Pour mettre fin à la session, cliquez sur **arrêter**.</span><span class="sxs-lookup"><span data-stu-id="90b57-141">To end the session, click **Stop**.</span></span> <span data-ttu-id="90b57-142">En fonction de l’appareil spécifié par l’utilisateur (entrée ou sortie), l’application utilise l’API MMDevice pour obtenir une référence au périphérique de communication de rendu ou de capture par défaut.</span><span class="sxs-lookup"><span data-stu-id="90b57-142">Depending on the device specified by the user (input or output), the application uses MMDevice API to get a reference to the default rendering or capture communication device.</span></span> <span data-ttu-id="90b57-143">Une fois que l’utilisateur a démarré une session de conversation, l’application effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="90b57-143">After the user starts a chat session, the application performs the following tasks:</span></span>

-   <span data-ttu-id="90b57-144">Crée et initialise un client audio en mode piloté par les événements.</span><span class="sxs-lookup"><span data-stu-id="90b57-144">Creates and initializes an audio client in event-driven mode.</span></span>
-   <span data-ttu-id="90b57-145">Associe le client au handle d’événement qui signale que les exemples sont prêts pour la capture ou le rendu.</span><span class="sxs-lookup"><span data-stu-id="90b57-145">Associates the client with the event handle that signals that samples are ready for capture or rendering.</span></span>
-   <span data-ttu-id="90b57-146">Configure un client de capture et un client de rendu pour le transport.</span><span class="sxs-lookup"><span data-stu-id="90b57-146">Sets up a capture client and a rendering client for the transport.</span></span>
-   <span data-ttu-id="90b57-147">Crée le thread de conversation et démarre le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="90b57-147">Creates the chat thread and starts the audio engine.</span></span>

<span data-ttu-id="90b57-148">Pour la capture de données audio, avec chaque passe de traitement, l’exemple utilise le client de capture pour obtenir la quantité totale de données capturées disponibles dans la mémoire tampon, lire des données à partir de l’appareil d’entrée par défaut et libérer le paquet et rendre le tampon disponible pour lire le jeu suivant de données capturées.</span><span class="sxs-lookup"><span data-stu-id="90b57-148">For capturing audio data, with each processing pass, the sample uses the capture client to get the total amount of captured data that is available in the buffer, read data from the default input device, and release the packet and make the buffer available for reading the next set of captured data.</span></span>

<span data-ttu-id="90b57-149">Pour le rendu, l’application détermine la quantité de données mises en file d’attente dans la mémoire tampon du point de terminaison de capture.</span><span class="sxs-lookup"><span data-stu-id="90b57-149">For rendering, the application determines the amount of data that is queued up to play in the capture endpoint buffer.</span></span> <span data-ttu-id="90b57-150">En conséquence, il écrit dans la mémoire tampon et libère la mémoire tampon en vue de la réussite du traitement suivant, jusqu’à ce que toutes les données aient été écrites.</span><span class="sxs-lookup"><span data-stu-id="90b57-150">It accordingly writes to the buffer and releases the buffer in preparation for the next processing pass until all of the data has been written.</span></span> <span data-ttu-id="90b57-151">Pour le rendu, les trames silencieuses sont préinscrites pour empêcher le moteur audio de se lancer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="90b57-151">For rendering, silent frames are prerolled to prevent the audio engine from glitching on startup.</span></span> <span data-ttu-id="90b57-152">DuckingCaptureSample indique également comment masquer le flux de rendu à partir du mélangeur de volume.</span><span class="sxs-lookup"><span data-stu-id="90b57-152">DuckingCaptureSample also shows how to hide the render stream from the volume mixer.</span></span>

<span data-ttu-id="90b57-153">Pour plus d’informations sur la fonctionnalité d’atténuation de flux, consultez [utilisation d’un appareil de communication](using-the-communication-device.md).</span><span class="sxs-lookup"><span data-stu-id="90b57-153">For more information about the stream attenuation feature, see [Using a Communication Device](using-the-communication-device.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="90b57-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="90b57-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90b57-155">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="90b57-155">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 
