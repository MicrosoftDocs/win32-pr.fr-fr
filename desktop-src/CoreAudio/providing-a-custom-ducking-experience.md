---
description: Une application peut refuser l’expérience de l’utilisation des canards par défaut gérée par le système et la remplacer par une implémentation personnalisée.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fournir un comportement de canard personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111310"
---
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="9d852-103">Fournir un comportement de canard personnalisé</span><span class="sxs-lookup"><span data-stu-id="9d852-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="9d852-104">Une application peut refuser l’expérience de l' [utilisation des canards par défaut](stream-attenuation.md) gérée par le système et la remplacer par une implémentation personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9d852-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="9d852-105">Une application peut fournir une expérience de canard personnalisée.</span><span class="sxs-lookup"><span data-stu-id="9d852-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="9d852-106">Par exemple, le lecteur Windows Media offre sa propre expérience en matière de mise en suspens en suspendant le flux multimédia actuel pendant une session de communication et en reprenant la lecture lorsque la session est fermée.</span><span class="sxs-lookup"><span data-stu-id="9d852-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="9d852-107">Un exemple d’application multimédia qui implémente un canard est inclus dans SDK Windows exemples ; Pour plus d’informations, consultez [DuckingMediaPlayer](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="9d852-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="9d852-108">Pour simuler l’expérience de l’ouverture et de la fermeture des flux de communication et la génération d’événements de canard, consultez [DuckingCaptureSample](duckingcapturesample.md), qui est également inclus avec SDK Windows exemples.</span><span class="sxs-lookup"><span data-stu-id="9d852-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="9d852-109">Une application multimédia qui lit des sons à atténuer doit être consciente des flux de communication, lorsqu’ils sont ouverts et fermés dans le système.</span><span class="sxs-lookup"><span data-stu-id="9d852-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="9d852-110">L’implémentation personnalisée peut être fournie à l’aide de MediaFoundation, DirectShow ou DirectSound, qui utilisent les API audio de base.</span><span class="sxs-lookup"><span data-stu-id="9d852-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="9d852-111">Un client direct WASAPI peut également remplacer la gestion par défaut s’il sait à quel moment la session de communication démarre et se termine.</span><span class="sxs-lookup"><span data-stu-id="9d852-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="9d852-112">**Pour fournir une expérience de canard personnalisée, un client WASAPI doit effectuer les tâches suivantes :**</span><span class="sxs-lookup"><span data-stu-id="9d852-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="9d852-113">Inscrivez-vous pour recevoir des événements de notification du *Gestionnaire de canards*, un composant du système audio qui gère les notifications relatives aux modifications du flux de communication.</span><span class="sxs-lookup"><span data-stu-id="9d852-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="9d852-114">Pour plus d’informations, vous [obtenez des événements de canard](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="9d852-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="9d852-115">Si le client est inscrit pour recevoir des notifications d’inversion, le gestionnaire de canards désactive le comportement par défaut fourni par le système.</span><span class="sxs-lookup"><span data-stu-id="9d852-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="9d852-116">Si le comportement par défaut est désactivé de manière explicitement (voir [désactivation de l’expérience de l’utilisation de l’environnement par défaut](disabling-the-ducking-experience.md)) et que le client ne fournit pas de comportement de remplacement, l’application ne rencontre pas de comportement d’inversion.</span><span class="sxs-lookup"><span data-stu-id="9d852-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="9d852-117">Écoutez les notifications d’événement Duck envoyées par le gestionnaire de canards et effectuez le comportement de l’encadrement souhaité.</span><span class="sxs-lookup"><span data-stu-id="9d852-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="9d852-118">Pour plus d’informations sur l’implémentation d’un comportement de mise en œuvre, consultez [considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="9d852-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d852-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d852-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d852-120">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="9d852-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="9d852-121">Expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="9d852-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="9d852-122">Désactivation de l’expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="9d852-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="9d852-123">Considérations relatives à l’implémentation pour l’installation de notifications</span><span class="sxs-lookup"><span data-stu-id="9d852-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="9d852-124">Obtention d’événements de canard</span><span class="sxs-lookup"><span data-stu-id="9d852-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



