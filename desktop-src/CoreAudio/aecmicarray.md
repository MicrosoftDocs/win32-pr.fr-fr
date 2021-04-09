---
description: Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité. L’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’AEC DMO, également appelé DSP de capture vocale, fourni par Microsoft.
ms.assetid: 932d3442-1beb-4938-9382-031c61cd9b05
title: AECMicArray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe72351b9f8f61d939a9f73eaf85022d7f487bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111562"
---
# <a name="aecmicarray"></a><span data-ttu-id="92ab7-104">AECMicArray</span><span class="sxs-lookup"><span data-stu-id="92ab7-104">AECMicArray</span></span>

<span data-ttu-id="92ab7-105">Cet exemple utilise les API audio de base pour capturer un flux vocal de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="92ab7-105">This sample uses the Core Audio APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="92ab7-106">L’exemple prend en charge l’annulation de l’écho acoustique et le traitement du tableau de microphone à l’aide de l’AEC DMO, également appelé DSP de capture vocale, fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="92ab7-106">The sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO, also called the Voice capture DSP, provided by Microsoft .</span></span>

<span data-ttu-id="92ab7-107">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="92ab7-107">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="92ab7-108">Description</span><span class="sxs-lookup"><span data-stu-id="92ab7-108">Description</span></span>](#description)
-   [<span data-ttu-id="92ab7-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92ab7-109">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="92ab7-110">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-110">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="92ab7-111">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-111">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="92ab7-112">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-112">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="92ab7-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92ab7-113">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="92ab7-114">Description</span><span class="sxs-lookup"><span data-stu-id="92ab7-114">Description</span></span>

<span data-ttu-id="92ab7-115">Cet exemple illustre les fonctionnalités suivantes.</span><span class="sxs-lookup"><span data-stu-id="92ab7-115">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="92ab7-116">[MMDevice](mmdevice-api.md) pour l’énumération et la sélection des appareils multimédias.</span><span class="sxs-lookup"><span data-stu-id="92ab7-116">[MMDevice](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="92ab7-117">[WASAPI](wasapi.md) pour les opérations de gestion de flux, telles que le démarrage et l’arrêt du flux, le basculement de flux.</span><span class="sxs-lookup"><span data-stu-id="92ab7-117">[WASAPI](wasapi.md) for stream management operations such as starting and stopping the stream, stream switching.</span></span>
-   <span data-ttu-id="92ab7-118">[DeviceTopology](devicetopology-api.md) pour l’énumération des adaptateurs audio.</span><span class="sxs-lookup"><span data-stu-id="92ab7-118">[DeviceTopology](devicetopology-api.md) for enumerating audio adapters.</span></span>
-   <span data-ttu-id="92ab7-119">[EndpointVolume](endpointvolume-api.md) contrôle des niveaux de volume des [sessions audio](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="92ab7-119">[EndpointVolume](endpointvolume-api.md) control the volume levels of [audio sessions](audio-sessions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92ab7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92ab7-120">Requirements</span></span>



| <span data-ttu-id="92ab7-121">Produit</span><span class="sxs-lookup"><span data-stu-id="92ab7-121">Product</span></span>                                                        | <span data-ttu-id="92ab7-122">Version</span><span class="sxs-lookup"><span data-stu-id="92ab7-122">Version</span></span>                     |
|----------------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="92ab7-123">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="92ab7-123">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="92ab7-124">Windows Vista ou version ultérieure ;</span><span class="sxs-lookup"><span data-stu-id="92ab7-124">Windows Vista or later</span></span>      |
| <span data-ttu-id="92ab7-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92ab7-125">Visual Studio</span></span>                                                  | <span data-ttu-id="92ab7-126">2005 (éditions non-Express)</span><span class="sxs-lookup"><span data-stu-id="92ab7-126">2005 (non-express editions)</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="92ab7-127">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-127">Downloading the Sample</span></span>

<span data-ttu-id="92ab7-128">Cet exemple est disponible aux emplacements suivants.</span><span class="sxs-lookup"><span data-stu-id="92ab7-128">This sample is available in the following locations.</span></span>



| <span data-ttu-id="92ab7-129">Emplacement</span><span class="sxs-lookup"><span data-stu-id="92ab7-129">Location</span></span>    | <span data-ttu-id="92ab7-130">Chemin d’accès/URL</span><span class="sxs-lookup"><span data-stu-id="92ab7-130">Path/URL</span></span>                                                                                     |
|-------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ab7-131">Kit de développement logiciel (SDK) Windows</span><span class="sxs-lookup"><span data-stu-id="92ab7-131">Windows SDK</span></span> | <span data-ttu-id="92ab7-132">\\Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ audio \\ AECMicArray \\ ...</span><span class="sxs-lookup"><span data-stu-id="92ab7-132">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\AECMicArray\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="92ab7-133">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-133">Building the Sample</span></span>

<span data-ttu-id="92ab7-134">Pour générer l’exemple AecSDKDemo, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="92ab7-134">To build the AecSDKDemo sample, use the following steps:</span></span>

1.  <span data-ttu-id="92ab7-135">Ouvrez une fenêtre de commande du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="92ab7-135">Open an SDK command window.</span></span>
2.  <span data-ttu-id="92ab7-136">Tapez **CD% MSSDK% \\ Setup**.</span><span class="sxs-lookup"><span data-stu-id="92ab7-136">Type **cd %MSSDK%\\Setup**.</span></span>
3.  <span data-ttu-id="92ab7-137">Exécutez VCIntegrate.exe.</span><span class="sxs-lookup"><span data-stu-id="92ab7-137">Run VCIntegrate.exe.</span></span>

    <span data-ttu-id="92ab7-138">À partir de ce point, les fenêtres de commande auront les paramètres d’environnement appropriés pour créer une application qui tire parti du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="92ab7-138">From this point forward, command windows will have the proper environment settings to build an application that takes advantage of the SDK.</span></span>

4.  <span data-ttu-id="92ab7-139">Générez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="92ab7-139">Build the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="92ab7-140">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="92ab7-140">Running the Sample</span></span>

<span data-ttu-id="92ab7-141">Si vous générez l’application de démonstration avec succès, un fichier exécutable, AecSDKDemo.exe est généré.</span><span class="sxs-lookup"><span data-stu-id="92ab7-141">If you build the demo application successfully, an executable file, AecSDKDemo.exe is generated.</span></span> <span data-ttu-id="92ab7-142">Pour l’exécuter, tapez `AecSDKDemo` dans une fenêtre de commande suivie d’arguments obligatoires ou facultatifs, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="92ab7-142">To run it, type `AecSDKDemo` in a command window followed by required or optional arguments as described below.</span></span>

`AecSDKDemo -out mic_out.pcm -mod system_mode [-option value] `

<span data-ttu-id="92ab7-143">Le tableau suivant indique les arguments.</span><span class="sxs-lookup"><span data-stu-id="92ab7-143">The following table shows the arguments.</span></span>

| <span data-ttu-id="92ab7-144">Argument</span><span class="sxs-lookup"><span data-stu-id="92ab7-144">Argument</span></span>  | <span data-ttu-id="92ab7-145">Description</span><span class="sxs-lookup"><span data-stu-id="92ab7-145">Description</span></span>                                                                                                                           |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ab7-146">-out</span><span class="sxs-lookup"><span data-stu-id="92ab7-146">-out</span></span>      | <span data-ttu-id="92ab7-147">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="92ab7-147">Required.</span></span> <span data-ttu-id="92ab7-148">Spécifie le nom du fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="92ab7-148">Specifies output file name.</span></span>                                                                                                 |
| <span data-ttu-id="92ab7-149">-mod</span><span class="sxs-lookup"><span data-stu-id="92ab7-149">-mod</span></span>      | <span data-ttu-id="92ab7-150">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="92ab7-150">Required.</span></span> <span data-ttu-id="92ab7-151">Spécifie le mode système de capture vocale.</span><span class="sxs-lookup"><span data-stu-id="92ab7-151">Specifies voice capture system mode.</span></span> <span data-ttu-id="92ab7-152">Pour plus d’informations, reportez-vous à la section « Configuration de la capture de la voix DMO » dans l’exemple de fichier Readme.</span><span class="sxs-lookup"><span data-stu-id="92ab7-152">Refer to "Configuring the voice capture DMO" section in the sample readme for details.</span></span> |
| <span data-ttu-id="92ab7-153">-Feature</span><span class="sxs-lookup"><span data-stu-id="92ab7-153">-feat</span></span>     | <span data-ttu-id="92ab7-154">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-154">Optional.</span></span> <span data-ttu-id="92ab7-155">Active le mode de fonctionnalité sur (1) ou sur OFF (0).</span><span class="sxs-lookup"><span data-stu-id="92ab7-155">Turns feature mode on (1) or off (0).</span></span>                                                                                       |
| <span data-ttu-id="92ab7-156">-NS</span><span class="sxs-lookup"><span data-stu-id="92ab7-156">-ns</span></span>       | <span data-ttu-id="92ab7-157">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-157">Optional.</span></span> <span data-ttu-id="92ab7-158">Désactive la suppression du bruit sur (1) ou sur OFF (0).</span><span class="sxs-lookup"><span data-stu-id="92ab7-158">Turns noise suppression on (1) or off (0).</span></span> <span data-ttu-id="92ab7-159">Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.</span><span class="sxs-lookup"><span data-stu-id="92ab7-159">Feature mode must be on for specifying this.</span></span>                                     |
| <span data-ttu-id="92ab7-160">-AGC</span><span class="sxs-lookup"><span data-stu-id="92ab7-160">-agc</span></span>      | <span data-ttu-id="92ab7-161">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-161">Optional.</span></span> <span data-ttu-id="92ab7-162">Active Digital AGC sur (1) ou sur OFF (0).</span><span class="sxs-lookup"><span data-stu-id="92ab7-162">Turns digital AGC on (1) or off (0).</span></span> <span data-ttu-id="92ab7-163">Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.</span><span class="sxs-lookup"><span data-stu-id="92ab7-163">Feature mode must be on for specifying this.</span></span>                                           |
| <span data-ttu-id="92ab7-164">-cntrclip</span><span class="sxs-lookup"><span data-stu-id="92ab7-164">-cntrclip</span></span> | <span data-ttu-id="92ab7-165">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-165">Optional.</span></span> <span data-ttu-id="92ab7-166">Active ou désactive le découpage du Centre (0).</span><span class="sxs-lookup"><span data-stu-id="92ab7-166">Turns center clipping on (1) or off (0).</span></span> <span data-ttu-id="92ab7-167">Le mode de fonctionnalité doit être activé pour pouvoir être spécifié.</span><span class="sxs-lookup"><span data-stu-id="92ab7-167">Feature mode must be on for specifying this.</span></span>                                       |
| <span data-ttu-id="92ab7-168">-spkdev</span><span class="sxs-lookup"><span data-stu-id="92ab7-168">-spkdev</span></span>   | <span data-ttu-id="92ab7-169">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-169">Optional.</span></span> <span data-ttu-id="92ab7-170">Spécifie l’index de l’appareil de l’intervenant.</span><span class="sxs-lookup"><span data-stu-id="92ab7-170">Specifies speaker device index.</span></span> <span data-ttu-id="92ab7-171">S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="92ab7-171">If not specified, the user will be asked to select.</span></span>                                         |
| <span data-ttu-id="92ab7-172">-micdev</span><span class="sxs-lookup"><span data-stu-id="92ab7-172">-micdev</span></span>   | <span data-ttu-id="92ab7-173">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-173">Optional.</span></span> <span data-ttu-id="92ab7-174">Spécifie l’index du périphérique microphone.</span><span class="sxs-lookup"><span data-stu-id="92ab7-174">Specifies microphone device index.</span></span> <span data-ttu-id="92ab7-175">S’il n’est pas spécifié, l’utilisateur est invité à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="92ab7-175">If not specified, the user will be asked to select.</span></span>                                      |
| <span data-ttu-id="92ab7-176">-Duration</span><span class="sxs-lookup"><span data-stu-id="92ab7-176">-duration</span></span> | <span data-ttu-id="92ab7-177">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-177">Optional.</span></span> <span data-ttu-id="92ab7-178">Spécifie la durée d’exécution de l’application.</span><span class="sxs-lookup"><span data-stu-id="92ab7-178">Specifies how long the application runs.</span></span>                                                                                    |



 

<span data-ttu-id="92ab7-179">Cet exemple d’application ne joue aucun signal.</span><span class="sxs-lookup"><span data-stu-id="92ab7-179">This sample application does not play any signals.</span></span> <span data-ttu-id="92ab7-180">Pour exécuter la démonstration correctement pour les modes activés AEC (mode 0 et 4), les utilisateurs doivent lire certains signaux audio via le même appareil d’orateur spécifié pour la solution DMO (c’est-à-dire l’appareil spécifié par l’option « -spkdev »), ce qui simule la voix de bout en bout dans un scénario de conversation bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="92ab7-180">To run the demo properly for AEC enabled modes (mode 0 and 4), users must play some audio signals through the same speaker device specified for the DMO (that is, the device specified by the "-spkdev" option), which simulates the far-end voice in a two-way chatting scenario.</span></span> <span data-ttu-id="92ab7-181">Les utilisateurs peuvent utiliser n’importe quel joueur pour lire des signaux audio.</span><span class="sxs-lookup"><span data-stu-id="92ab7-181">Users can use any player to play any audio signals.</span></span> <span data-ttu-id="92ab7-182">S’il n’y a aucun flux de rendu actif sur le périphérique de l’orateur sélectionné, le traitement de DMO échoue.</span><span class="sxs-lookup"><span data-stu-id="92ab7-182">If there is no active render stream on the selected speaker device, the DMO will fail to process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="92ab7-183">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="92ab7-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92ab7-184">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="92ab7-184">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



