---
description: Exemples de SDK qui utilisent les API audio principales
ms.assetid: 4460df28-a77d-4bf5-9dee-5fb69ba2ded6
title: Exemples de SDK qui utilisent les API audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15eb05da5fefc22eaa0987d9996f0ddb48702158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950674"
---
# <a name="sdk-samples-that-use-the-core-audio-apis"></a><span data-ttu-id="845ce-103">Exemples de SDK qui utilisent les API audio principales</span><span class="sxs-lookup"><span data-stu-id="845ce-103">SDK Samples That Use the Core Audio APIs</span></span>

<span data-ttu-id="845ce-104">Le SDK Windows comprend les exemples de code suivants qui illustrent l’utilisation des API audio de base.</span><span class="sxs-lookup"><span data-stu-id="845ce-104">The Windows SDK includes the following code samples that demonstrate the use of the Core Audio APIs.</span></span> <span data-ttu-id="845ce-105">Les exemples suivants se trouvent dans le répertoire% MSSdk% \\ Samples \\ Multimedia \\ audio, où% MSSdk% est le répertoire racine de l’installation SDK Windows sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-105">The following samples are located in the directory %MSSdk%\\samples\\multimedia\\audio, where %MSSdk% is the root directory of the Windows SDK installation on your computer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="845ce-106">Exemple</span><span class="sxs-lookup"><span data-stu-id="845ce-106">Sample</span></span></th>
<th><span data-ttu-id="845ce-107">Deascription</span><span class="sxs-lookup"><span data-stu-id="845ce-107">Deascription</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="845ce-108"><a href="aecmicarray.md">AECMicArray</a></span><span class="sxs-lookup"><span data-stu-id="845ce-108"><a href="aecmicarray.md">AECMicArray</a></span></span></td>
<td><span data-ttu-id="845ce-109">Cet exemple utilise les API MMDevice, WASAPI, DeviceTopology et EndpointVolume pour capturer un flux vocal de haute qualité.</span><span class="sxs-lookup"><span data-stu-id="845ce-109">This sample uses the MMDevice, WASAPI, DeviceTopology, and EndpointVolume APIs to capture a high-quality voice stream.</span></span> <span data-ttu-id="845ce-110">L’exemple prend en charge l’annulation de l’écho acoustique (AEC) et le traitement du tableau de microphone à l’aide de l’AEC DMO également appelé le DSP de capture vocale fourni par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="845ce-110">TThe sample supports acoustic echo cancellation (AEC) and microphone array processing by using the AEC DMO also called the Voice capture DSP provided by Microsoft .</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="845ce-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-111"><a href="capturesharedeventdriven.md">CaptureSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="845ce-112">Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="845ce-112">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="845ce-113">Cet exemple illustre la mise en mémoire tampon pilotée par les événements.</span><span class="sxs-lookup"><span data-stu-id="845ce-113">This sample demonstrates event-driven buffering.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="845ce-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-114"><a href="capturesharedtimerdriven.md">CaptureSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="845ce-115">Cet exemple d’application utilise les API audio de base pour capturer des données audio à partir d’un périphérique d’entrée, spécifié par l’utilisateur et les écrit dans un nom unique. Fichier WAV dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="845ce-115">This sample application uses the Core Audio APIs to capture audio data from an input device, specified by the user and writes it to a uniquely named .WAV file in the current directory.</span></span> <span data-ttu-id="845ce-116">Cet exemple illustre la mise en mémoire tampon pilotée par une minuterie.</span><span class="sxs-lookup"><span data-stu-id="845ce-116">This sample demonstrates timer-driven buffering.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="845ce-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span><span class="sxs-lookup"><span data-stu-id="845ce-117"><a href="duckingcapturesample.md">DuckingCaptureSample</a></span></span></td>
<td><span data-ttu-id="845ce-118">Cet exemple d’application montre l’ouverture et la fermeture de flux de communication et la mise en place d’événements de canard qu’une application peut atteindre pour implémenter l’atténuation du flux.</span><span class="sxs-lookup"><span data-stu-id="845ce-118">This sample application demonstrates opening and closing communication streams and causing ducking events that an application can get to implement stream attenuation.</span></span> <span data-ttu-id="845ce-119">Cette application implémente un client de conversation qui utilise des API audio de base pour lire les données audio à partir d’un périphérique de communication et les lire sur le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="845ce-119">This application implements a chat client that uses Core Audio APIs to read audio data from a communication device and to play it on the output device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="845ce-120"><a href="endpointvolume.md">EndpointVolume</a></span><span class="sxs-lookup"><span data-stu-id="845ce-120"><a href="endpointvolume.md">EndpointVolume</a></span></span></td>
<td><span data-ttu-id="845ce-121">Cet exemple d’application utilise les API audio de base pour modifier le volume de l’appareil, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-121">This sample application uses the Core Audio APIs to change the volume of the device, specified by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="845ce-122"><a href="osd.md">DÉPLOIEMENT</a></span><span class="sxs-lookup"><span data-stu-id="845ce-122"><a href="osd.md">OSD</a></span></span></td>
<td><span data-ttu-id="845ce-123">Cet exemple utilise les API MMDevice et EndpointVolume pour implémenter un affichage à l’écran qui affiche les modifications de volume du flux de sortie qui s’exécutent par le biais du périphérique de point de terminaison de rendu audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="845ce-123">This sample uses the MMDevice and EndpointVolume APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="845ce-124">L’affichage à l’écran s’affiche lorsque l’utilisateur ajuste le niveau de volume dans le programme de contrôle de volume Windows, Sndvol.exe, et disparaît une fois que le volume reste inchangé pendant une brève période.</span><span class="sxs-lookup"><span data-stu-id="845ce-124">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="845ce-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-125"><a href="renderexclusiveeventdriven.md">RenderExclusiveEventDriven</a></span></span></td>
<td><span data-ttu-id="845ce-126">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-126">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="845ce-127">Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="845ce-127">This sample demonstrates event-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="845ce-128">Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="845ce-128">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="845ce-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-129"><a href="renderexclusivetimerdriven.md">RenderExclusiveTimerDriven</a></span></span></td>
<td><span data-ttu-id="845ce-130">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-130">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="845ce-131">Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="845ce-131">This sample demonstrates timer-driven buffering for a rendering client in exclusive mode.</span></span> <span data-ttu-id="845ce-132">Pour un flux en mode exclusif, le client partage la mémoire tampon du point de terminaison avec le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="845ce-132">For an exclusive-mode stream, the client shares the endpoint buffer with the audio device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="845ce-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-133"><a href="rendersharedeventdriven.md">RenderSharedEventDriven</a></span></span></td>
<td><span data-ttu-id="845ce-134">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-134">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="845ce-135">Cet exemple illustre la mise en mémoire tampon pilotée par les événements pour un client de rendu en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="845ce-135">This sample demonstrates event-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="845ce-136">Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="845ce-136">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="845ce-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span><span class="sxs-lookup"><span data-stu-id="845ce-137"><a href="rendersharedtimerdriven.md">RenderSharedTimerDriven</a></span></span></td>
<td><span data-ttu-id="845ce-138">Cet exemple d’application utilise les API audio de base pour afficher les données audio sur un périphérique de sortie, spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="845ce-138">This sample application uses the Core Audio APIs to render audio data to an output device, specified by the user.</span></span> <span data-ttu-id="845ce-139">Cet exemple illustre la mise en mémoire tampon pilotée par minuterie pour un client de rendu en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="845ce-139">This sample demonstrates timer-driven buffering for a rendering client in shared mode.</span></span> <span data-ttu-id="845ce-140">Pour un flux en mode partagé, le client partage la mémoire tampon du point de terminaison avec le moteur audio.</span><span class="sxs-lookup"><span data-stu-id="845ce-140">For a shared-mode stream, the client shares the endpoint buffer with the audio engine.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="845ce-141">WinAudio</span><span class="sxs-lookup"><span data-stu-id="845ce-141">WinAudio</span></span></td>
<td><span data-ttu-id="845ce-142">Cet exemple utilise l’API MMDevice et WASAPI pour lire et capturer des flux audio.</span><span class="sxs-lookup"><span data-stu-id="845ce-142">This sample uses the MMDevice API and WASAPI to play and capture audio streams.</span></span> <span data-ttu-id="845ce-143">L’interface utilisateur de cet exemple d’application permet aux utilisateurs de sélectionner des appareils de point de terminaison audio, de modifier le niveau de volume de la session audio locale et de lire les fichiers. wav et l’entrée du microphone.</span><span class="sxs-lookup"><span data-stu-id="845ce-143">The user interface of this sample application enables users to select audio endpoint devices, to change the volume level of the local audio session, and to play .wav files and microphone input.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="845ce-144">Cet exemple est déconseillé dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="845ce-144">This sample has been deprecated in Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="845ce-145">Vous pouvez télécharger le SDK Windows à partir du site Web du [Centre de téléchargement Microsoft Windows SDK](https://developer.microsoft.com/windows/downloads/sdk-archive/) .</span><span class="sxs-lookup"><span data-stu-id="845ce-145">You can download the Windows SDK from the [Microsoft Windows SDK Download Center](https://developer.microsoft.com/windows/downloads/sdk-archive/) website.</span></span>

## <a name="related-topics"></a><span data-ttu-id="845ce-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="845ce-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="845ce-147">À propos des API audio Windows Core</span><span class="sxs-lookup"><span data-stu-id="845ce-147">About the Windows Core Audio APIs</span></span>](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




