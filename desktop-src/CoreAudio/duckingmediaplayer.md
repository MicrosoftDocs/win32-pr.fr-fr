---
description: Cet exemple d’application illustre l’atténuation du flux en implémentant un lecteur multimédia qui montre le comportement d’atténuation par défaut fourni par le système, qui ne permet pas d’encadrer des événements et implémente une gestion personnalisée lors de la réception d’événements.
ms.assetid: 667c8751-1d17-4b59-8ced-ed5f0c333ae9
title: DuckingMediaPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86952f1aa7b81c9a7dc711f0c4f36fc8531bd63
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106539380"
---
# <a name="duckingmediaplayer"></a><span data-ttu-id="1b201-103">DuckingMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1b201-103">DuckingMediaPlayer</span></span>

<span data-ttu-id="1b201-104">Cet exemple d’application illustre l’atténuation du flux en implémentant un lecteur multimédia qui montre le comportement d’atténuation par défaut fourni par le système, qui ne permet pas d’encadrer des événements et implémente une gestion personnalisée lors de la réception d’événements.</span><span class="sxs-lookup"><span data-stu-id="1b201-104">This sample application demonstrates stream attenuation by implementing a media player that shows the default attenuation behavior provided by the system, opts out of ducking events, and implements custom handling when ducking events are received.</span></span> <span data-ttu-id="1b201-105">Cet exemple doit être utilisé avec [DuckingCaptureSample](duckingcapturesample.md).</span><span class="sxs-lookup"><span data-stu-id="1b201-105">This sample must be used in conjuction with [DuckingCaptureSample](duckingcapturesample.md).</span></span> <span data-ttu-id="1b201-106">Pour plus d’informations sur l’utilisation de la canard ou de l’atténuation de flux, consultez l’expérience de l’utilisation de l' [environnement](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="1b201-106">For more information about ducking or stream attenuation, see [Default Ducking Experience](stream-attenuation.md).</span></span>

<span data-ttu-id="1b201-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b201-107">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1b201-108">Description</span><span class="sxs-lookup"><span data-stu-id="1b201-108">Description</span></span>](#description)
-   [<span data-ttu-id="1b201-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b201-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="1b201-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="1b201-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="1b201-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="1b201-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b201-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="1b201-114">Description</span><span class="sxs-lookup"><span data-stu-id="1b201-114">Description</span></span>

<span data-ttu-id="1b201-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="1b201-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="1b201-116">DirectShow pour lire un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="1b201-116">DirectShow to play a media file.</span></span>
-   <span data-ttu-id="1b201-117">[WASAPI](wasapi.md) pour la gestion des flux et la gestion des événements de canard.</span><span class="sxs-lookup"><span data-stu-id="1b201-117">[WASAPI](wasapi.md) for stream management and handling ducking events.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b201-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b201-118">Requirements</span></span>



| <span data-ttu-id="1b201-119">Produit</span><span class="sxs-lookup"><span data-stu-id="1b201-119">Product</span></span>                                                        | <span data-ttu-id="1b201-120">Version</span><span class="sxs-lookup"><span data-stu-id="1b201-120">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="1b201-121">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="1b201-121">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="1b201-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1b201-122">Windows 7</span></span> |
| <span data-ttu-id="1b201-123">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b201-123">Visual Studio</span></span>                                                  | <span data-ttu-id="1b201-124">2008</span><span class="sxs-lookup"><span data-stu-id="1b201-124">2008</span></span>      |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="1b201-125">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-125">Downloading the Sample</span></span>

<span data-ttu-id="1b201-126">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="1b201-126">This sample is available in the following locations.</span></span>



| <span data-ttu-id="1b201-127">Emplacement</span><span class="sxs-lookup"><span data-stu-id="1b201-127">Location</span></span>    | <span data-ttu-id="1b201-128">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="1b201-128">Path/URL</span></span>                                                                                            |
|-------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b201-129">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="1b201-129">Windows SDK</span></span> | <span data-ttu-id="1b201-130">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ DuckingMediaPlayer \\ ...</span><span class="sxs-lookup"><span data-stu-id="1b201-130">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\DuckingMediaPlayer\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="1b201-131">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-131">Building the Sample</span></span>

<span data-ttu-id="1b201-132">Pour générer l’exemple DuckingMediaPlayer, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b201-132">To build the DuckingMediaPlayer sample, use the following steps:</span></span>

1.  <span data-ttu-id="1b201-133">Ouvrez DuckingMediaPlayer. sln dans Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="1b201-133">Open the DuckingMediaPlayer.sln in Visual Studio 2008.</span></span>
2.  <span data-ttu-id="1b201-134">À partir de la fenêtre, sélectionnez la configuration de la solution **Debug** ou **Release** , sélectionnez le menu **générer** dans la barre de menus, puis sélectionnez l’option **générer** .</span><span class="sxs-lookup"><span data-stu-id="1b201-134">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="1b201-135">Si vous n’ouvrez pas Visual Studio à partir du shell CMD pour le kit de développement logiciel (SDK), Visual Studio n’aura pas accès à l’environnement de génération du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="1b201-135">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="1b201-136">Dans ce cas, l’exemple n’est pas généré, sauf si vous définissez explicitement la variable d’environnement MSSdk, qui est utilisée dans le fichier projet, DuckingMediaPlayer. vcproj.</span><span class="sxs-lookup"><span data-stu-id="1b201-136">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, DuckingMediaPlayer.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1b201-137">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="1b201-137">Running the Sample</span></span>

<span data-ttu-id="1b201-138">Si vous générez l’application avec succès, un fichier exécutable, DuckingMediaPlayer.exe, est généré.</span><span class="sxs-lookup"><span data-stu-id="1b201-138">If you build the application successfully, an executable file, DuckingMediaPlayer.exe, is generated.</span></span> <span data-ttu-id="1b201-139">Pour l’exécuter, sélectionnez **Démarrer le débogage** ou **Démarrer sans débogage** dans le menu **Déboguer** ou tapez `DuckingMediaPlayer` dans une fenêtre de commande.</span><span class="sxs-lookup"><span data-stu-id="1b201-139">To run it, select **Start Debugging** or **Start Without Debugging** from the **Debug** menu or type `DuckingMediaPlayer` in a command window.</span></span>

<span data-ttu-id="1b201-140">Pour voir une démonstration de l’un des canards, vous devez exécuter DuckingMediaPlayer et DuckingCaptureSample simultanément.</span><span class="sxs-lookup"><span data-stu-id="1b201-140">To view a demonstration of ducking, you must execute DuckingMediaPlayer and DuckingCaptureSample simultaneously.</span></span> <span data-ttu-id="1b201-141">DuckingCaptureSample ouvre un flux de communication et signale au système qu’il doit générer un événement de canard.</span><span class="sxs-lookup"><span data-stu-id="1b201-141">DuckingCaptureSample opens a communication stream and signals the system to generate a ducking event.</span></span> <span data-ttu-id="1b201-142">Le DuckingMediaPlayer est averti par le système lorsqu’un événement de canard se produit et que le lecteur multimédia effectue l’action demandée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1b201-142">The DuckingMediaPlayer is notified by the system when a ducking event occurs, and the media player performs the action requested by the user.</span></span>

<span data-ttu-id="1b201-143">Pour désactiver le comportement de l’encanardment :</span><span class="sxs-lookup"><span data-stu-id="1b201-143">To disable ducking behavior:</span></span>

1.  <span data-ttu-id="1b201-144">Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.</span><span class="sxs-lookup"><span data-stu-id="1b201-144">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="1b201-145">Sur la DuckingMediaPlayer, sélectionnez un fichier multimédia à lire, puis spécifiez l’option de l’option de l’encadrement comme **refus de** l’encadrer.</span><span class="sxs-lookup"><span data-stu-id="1b201-145">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Opt out of Ducking**.</span></span>

<span data-ttu-id="1b201-146">Notez que le fichier multimédia est lu sans interruption.</span><span class="sxs-lookup"><span data-stu-id="1b201-146">Notice that the media file is played without any interruption.</span></span> <span data-ttu-id="1b201-147">Les événements générés par le système lors de l’ouverture du flux de communication sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="1b201-147">The events generated by the system when the communication stream opened are ignored.</span></span>

<span data-ttu-id="1b201-148">Pour illustrer le comportement de l’encodeur par défaut fourni par le système, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1b201-148">To demonstrate the default ducking behavior provided by the system, do the following:</span></span>

1.  <span data-ttu-id="1b201-149">Sélectionnez l’option **sons** dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="1b201-149">Select the **Sounds** option from the control panel.</span></span> <span data-ttu-id="1b201-150">Sous l’onglet **communications** , sélectionnez **réduire le volume des autres sons de 80%**.</span><span class="sxs-lookup"><span data-stu-id="1b201-150">On the **Communications** tab, select **Reduce the volume of other sounds by 80%**.</span></span>
2.  <span data-ttu-id="1b201-151">Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.</span><span class="sxs-lookup"><span data-stu-id="1b201-151">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
3.  <span data-ttu-id="1b201-152">Sur le DuckingMediaPlayer, sélectionnez un fichier multimédia à lire, sans choisir l’une des options d’encanardment.</span><span class="sxs-lookup"><span data-stu-id="1b201-152">On the DuckingMediaPlayer, select a media file to play, without choosing any of the ducking options.</span></span>
4.  <span data-ttu-id="1b201-153">Dans la fenêtre DuckingCaptureSample, cliquez sur **arrêter** pour arrêter le flux de communication.</span><span class="sxs-lookup"><span data-stu-id="1b201-153">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="1b201-154">Notez que lorsque DuckingCaptureSample ouvre le flux de communication, le fichier multimédia joué par DuckingMediaPlayer est lu sans interruption, mais le niveau de volume est abaissé.</span><span class="sxs-lookup"><span data-stu-id="1b201-154">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer plays without interruption, but the volume level is lowered.</span></span> <span data-ttu-id="1b201-155">Lorsque la session de communication est arrêtée, le volume est réinitialisé sur le paramètre d’origine.</span><span class="sxs-lookup"><span data-stu-id="1b201-155">When the communication session is stopped, the volume is reset to the original setting.</span></span> <span data-ttu-id="1b201-156">Ce comportement d’atténuation de flux est le comportement de mise en œuvre par défaut implémenté par le système.</span><span class="sxs-lookup"><span data-stu-id="1b201-156">This stream attenuation behavior is the default ducking behavior implemented by the system.</span></span>

<span data-ttu-id="1b201-157">Pour afficher un comportement de canardment personnalisé implémenté par le lecteur multimédia :</span><span class="sxs-lookup"><span data-stu-id="1b201-157">To view a customized ducking behavior implemented by the media player:</span></span>

1.  <span data-ttu-id="1b201-158">Dans la fenêtre DuckingCaptureSample, sélectionnez **utiliser l’appareil d’entrée par défaut**, puis cliquez sur **Démarrer** pour démarrer une session de capture à partir de l’appareil de communication.</span><span class="sxs-lookup"><span data-stu-id="1b201-158">On the DuckingCaptureSample window, select **Use default input device**, and click **Start** to start a capture session from the communication device.</span></span>
2.  <span data-ttu-id="1b201-159">Sur le DuckingMediaPlayer, sélectionnez un fichier multimédia à lire et spécifiez l’option de mise en forme en tant que mise en **pause sur le canard**.</span><span class="sxs-lookup"><span data-stu-id="1b201-159">On the DuckingMediaPlayer, select a media file to play, and specify the ducking option as **Pause on Duck**.</span></span>
3.  <span data-ttu-id="1b201-160">Dans la fenêtre DuckingCaptureSample, cliquez sur **arrêter** pour arrêter le flux de communication.</span><span class="sxs-lookup"><span data-stu-id="1b201-160">On the DuckingCaptureSample window, click **Stop** to stop the communication stream.</span></span>

<span data-ttu-id="1b201-161">Notez que lorsque DuckingCaptureSample ouvre le flux de communication, le fichier multimédia lu par DuckingMediaPlayer est suspendu.</span><span class="sxs-lookup"><span data-stu-id="1b201-161">Notice that when DuckingCaptureSample opens the communication stream, the media file played by DuckingMediaPlayer is paused.</span></span> <span data-ttu-id="1b201-162">La lecture reprend lorsque la session de communication est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="1b201-162">The playback resumes when the communication session is stopped.</span></span> <span data-ttu-id="1b201-163">Ce comportement d’atténuation du flux est le comportement de l’enchaînement implémenté par le lecteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="1b201-163">This stream attenuation behavior is the ducking behavior implemented by the media player.</span></span>

<span data-ttu-id="1b201-164">DuckingMediaPlayer montre également comment intégrer le contrôle du volume pour chaque application avec le mélangeur de volume.</span><span class="sxs-lookup"><span data-stu-id="1b201-164">DuckingMediaPlayer also demonstrates how to integrate volume control for each application with the volume mixer.</span></span>

<span data-ttu-id="1b201-165">Pour plus d’informations sur la fonctionnalité d’atténuation de flux, consultez l’expérience de l’utilisation de l' [environnement par défaut](stream-attenuation.md).</span><span class="sxs-lookup"><span data-stu-id="1b201-165">For more information about the stream attenuation feature, see [Default Ducking Experience](stream-attenuation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b201-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b201-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b201-167">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="1b201-167">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



