---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748549"
---
# <a name="endpointvolume-api"></a><span data-ttu-id="fd61c-103">API EndpointVolume</span><span class="sxs-lookup"><span data-stu-id="fd61c-103">EndpointVolume API</span></span>

<span data-ttu-id="fd61c-104">L’API EndpointVolume permet aux clients spécialisés de contrôler et de surveiller les niveaux de volume des [appareils de point de terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="fd61c-104">The EndpointVolume API enables specialized clients to control and monitor the volume levels of [audio endpoint devices](audio-endpoint-devices.md).</span></span> <span data-ttu-id="fd61c-105">Un client obtient des références aux interfaces dans l’API EndpointVolume en obtenant l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) d’un périphérique de point de terminaison audio et en appelant la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .</span><span class="sxs-lookup"><span data-stu-id="fd61c-105">A client obtains references to the interfaces in the EndpointVolume API by obtaining the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of an audio endpoint device and calling the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method.</span></span>

<span data-ttu-id="fd61c-106">Le fichier d’en-tête Endpointvolume. h définit les interfaces dans l’API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="fd61c-106">Header file Endpointvolume.h defines the interfaces in the EndpointVolume API.</span></span>

<span data-ttu-id="fd61c-107">Les applications audio qui utilisent l' [API MMDevice](mmdevice-api.md) et [WASAPI](wasapi.md) utilisent généralement l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) pour contrôler les niveaux de volume pour chaque session.</span><span class="sxs-lookup"><span data-stu-id="fd61c-107">Audio applications that use the [MMDevice API](mmdevice-api.md) and [WASAPI](wasapi.md) typically use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) interface to control volume levels on a per-session basis.</span></span> <span data-ttu-id="fd61c-108">Seuls deux types d’applications audio requièrent l’utilisation de l’API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="fd61c-108">Only two types of audio applications require the use of the EndpointVolume API.</span></span> <span data-ttu-id="fd61c-109">Ces types d’applications sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="fd61c-109">These application types are:</span></span>

-   <span data-ttu-id="fd61c-110">Les applications qui gèrent les niveaux de volume principal des appareils de point de terminaison audio, comme le programme de contrôle de volume de Windows, Sndvol.exe.</span><span class="sxs-lookup"><span data-stu-id="fd61c-110">Applications that manage the master volume levels of audio endpoint devices, similar to the Windows volume-control program, Sndvol.exe.</span></span>
-   <span data-ttu-id="fd61c-111">Applications audio professionnelles (« Pro Audio ») qui requièrent un accès en mode exclusif aux appareils de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="fd61c-111">Professional audio ("pro audio") applications that require exclusive-mode access to audio endpoint devices.</span></span>

<span data-ttu-id="fd61c-112">L’utilisation inappropriée de l’API EndpointVolume peut interférer avec la stratégie audio Windows et perturber les paramètres de volume système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fd61c-112">Inappropriate use of the EndpointVolume API can interfere with Windows audio policy and disrupt the user's system volume settings.</span></span>

<span data-ttu-id="fd61c-113">Si un périphérique de point de terminaison audio implémente des contrôles de volume matériel et de sourdine, l’API EndpointVolume utilise ces contrôles pour gérer le volume de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="fd61c-113">If an audio endpoint device implements hardware volume and mute controls, the EndpointVolume API uses those controls to manage the device volume.</span></span> <span data-ttu-id="fd61c-114">Dans le cas contraire, l’API EndpointVolume implémente les contrôles dans le logiciel, de manière transparente pour le client.</span><span class="sxs-lookup"><span data-stu-id="fd61c-114">Otherwise, the EndpointVolume API implements the controls in software, transparently to the client.</span></span>

<span data-ttu-id="fd61c-115">Si un appareil a des contrôles volume matériel et muet, les modifications apportées aux paramètres volume et muet de l’appareil via l’API EndpointVolume affectent le niveau de volume en mode partagé et en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="fd61c-115">If a device has hardware volume and mute controls, changes made to the device's volume and mute settings through the EndpointVolume API affect the volume level in both shared mode and exclusive mode.</span></span> <span data-ttu-id="fd61c-116">Si un appareil ne dispose pas de contrôles de volume matériel et de contrôle muet, les modifications apportées au volume logiciel et les contrôles muet via l’API EndpointVolume affectent le niveau de volume en mode partagé, mais pas en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="fd61c-116">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through the EndpointVolume API affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="fd61c-117">En mode exclusif, le client et l’appareil échangent directement des données audio, en ignorant les contrôles logiciels.</span><span class="sxs-lookup"><span data-stu-id="fd61c-117">In exclusive mode, the client and the device exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="fd61c-118">Pour les applications qui doivent gérer le volume matériel et les contrôles de sourdine, l’API EndpointVolume offre deux avantages potentiels par rapport à l' [API DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="fd61c-118">For applications that must manage hardware volume and mute controls, the EndpointVolume API offers two potential advantages over the [DeviceTopology API](devicetopology-api.md).</span></span>

<span data-ttu-id="fd61c-119">Tout d’abord, un certain nombre de périphériques de carte audio n’ont pas de contrôle de volume matériel.</span><span class="sxs-lookup"><span data-stu-id="fd61c-119">First, a number of audio adapter devices lack hardware volume controls.</span></span> <span data-ttu-id="fd61c-120">Si un appareil ne dispose pas d’un contrôle de volume matériel, l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de l’API EndpointVolume implémente automatiquement un contrôle de volume logiciel sur le flux de ce périphérique.</span><span class="sxs-lookup"><span data-stu-id="fd61c-120">If a device lacks a hardware volume control, the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the EndpointVolume API automatically implements a software volume control on the stream to or from that device.</span></span> <span data-ttu-id="fd61c-121">Pour un client de l’API EndpointVolume, le résultat est le même que le contrôle du volume soit implémenté dans le matériel par l’appareil ou dans le logiciel par l’interface de l’API EndpointVolume.</span><span class="sxs-lookup"><span data-stu-id="fd61c-121">For a client of the EndpointVolume API, the result is the same whether the volume control is implemented in hardware by the device or in software by the EndpointVolume API interface.</span></span>

<span data-ttu-id="fd61c-122">Deuxièmement, même si l’appareil de l’adaptateur implémente des contrôles de volume matériel, une application qui utilise l’API DeviceTopology pour implémenter un algorithme de parcours topologique peut ne pas trouver le contrôle qu’elle recherche.</span><span class="sxs-lookup"><span data-stu-id="fd61c-122">Second, even if the adapter device does implement hardware volume controls, an application that uses the DeviceTopology API to implement a topology-traversal algorithm might fail to find the control that it is looking for.</span></span> <span data-ttu-id="fd61c-123">En règle générale, une telle application est conçue pour traverser la topologie matérielle d’un périphérique particulier ou un ensemble d’appareils associés.</span><span class="sxs-lookup"><span data-stu-id="fd61c-123">Typically, such an application is designed to traverse the hardware topology of a particular device or set of related devices.</span></span> <span data-ttu-id="fd61c-124">L’application risque d’échouer si elle tente de traverser la topologie d’un appareil pour laquelle elle n’a pas été spécifiquement conçue ou testée.</span><span class="sxs-lookup"><span data-stu-id="fd61c-124">The application risks failing if it attempts to traverse the topology of a device that it has not been specifically designed for or tested with.</span></span>

<span data-ttu-id="fd61c-125">Seules les applications spécialisées qui doivent accéder à des fonctions matérielles autres que les contrôles volume et muet requièrent l’utilisation de l’API DeviceTopology.</span><span class="sxs-lookup"><span data-stu-id="fd61c-125">Only specialized applications that must access hardware functions other than volume and mute controls require the use of the DeviceTopology API.</span></span> <span data-ttu-id="fd61c-126">Pour les applications qui requièrent uniquement le contrôle du niveau de volume d’un flux en mode exclusif, l’API EndpointVolume est plus simple à utiliser et fonctionne de manière fiable avec un plus grand nombre de périphériques matériels audio.</span><span class="sxs-lookup"><span data-stu-id="fd61c-126">For applications that require control only of the volume level of an exclusive-mode stream, the EndpointVolume API is simpler to use and works reliably with a wider range of audio hardware devices.</span></span>

<span data-ttu-id="fd61c-127">Pour obtenir des exemples de code qui utilisent les interfaces dans l’API EndpointVolume, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fd61c-127">For code examples that use the interfaces in the EndpointVolume API, see the following topics:</span></span>

-   [<span data-ttu-id="fd61c-128">Contrôles du volume du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="fd61c-128">Endpoint Volume Controls</span></span>](endpoint-volume-controls.md)
-   [<span data-ttu-id="fd61c-129">Compteurs de pic</span><span class="sxs-lookup"><span data-stu-id="fd61c-129">Peak Meters</span></span>](peak-meters.md)

<span data-ttu-id="fd61c-130">Pour voir un exemple qui utilise l’API EndpointVolume, consultez [EndpointVolume](endpointvolume.md) dans la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fd61c-130">To see a sample that uses the EndpointVolume API, see [EndpointVolume](endpointvolume.md) in the Windows SDK.</span></span>

<span data-ttu-id="fd61c-131">L’API EndpointVolume implémente les interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="fd61c-131">The EndpointVolume API implements the following interfaces.</span></span>



| <span data-ttu-id="fd61c-132">Interface</span><span class="sxs-lookup"><span data-stu-id="fd61c-132">Interface</span></span>                                                | <span data-ttu-id="fd61c-133">Description</span><span class="sxs-lookup"><span data-stu-id="fd61c-133">Description</span></span>                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd61c-134">**IAudioEndpointVolume**</span><span class="sxs-lookup"><span data-stu-id="fd61c-134">**IAudioEndpointVolume**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | <span data-ttu-id="fd61c-135">Représente les contrôles de volume du flux audio vers ou à partir d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="fd61c-135">Represents the volume controls on the audio stream to or from an audio endpoint device.</span></span> |
| [<span data-ttu-id="fd61c-136">**IAudioMeterInformation**</span><span class="sxs-lookup"><span data-stu-id="fd61c-136">**IAudioMeterInformation**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | <span data-ttu-id="fd61c-137">Représente un compteur de pic sur le flux audio vers ou à partir d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="fd61c-137">Represents a peak meter on the audio stream to or from an audio endpoint device.</span></span>        |



 

<span data-ttu-id="fd61c-138">En outre, les clients de l’API EndpointVolume qui requièrent la notification du volume et les modifications en sourdine des appareils de point de terminaison audio doivent implémenter l’interface suivante.</span><span class="sxs-lookup"><span data-stu-id="fd61c-138">In addition, clients of the EndpointVolume API that require notification of volume and muting changes in audio endpoint devices should implement the following interface.</span></span>



| <span data-ttu-id="fd61c-139">Interface</span><span class="sxs-lookup"><span data-stu-id="fd61c-139">Interface</span></span>                                                            | <span data-ttu-id="fd61c-140">Description</span><span class="sxs-lookup"><span data-stu-id="fd61c-140">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd61c-141">**IAudioEndpointVolumeCallback**</span><span class="sxs-lookup"><span data-stu-id="fd61c-141">**IAudioEndpointVolumeCallback**</span></span>](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | <span data-ttu-id="fd61c-142">Fournit des notifications lorsque le niveau de volume ou l’État muet d’un périphérique de point de terminaison audio change.</span><span class="sxs-lookup"><span data-stu-id="fd61c-142">Provides notifications when the volume level or muting state of an audio endpoint device changes.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fd61c-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fd61c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd61c-144">Contrôles de volume</span><span class="sxs-lookup"><span data-stu-id="fd61c-144">Volume Controls</span></span>](volume-controls.md)
</dt> <dt>

[<span data-ttu-id="fd61c-145">**Interface IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="fd61c-145">**IMMDevice Interface**</span></span>](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[<span data-ttu-id="fd61c-146">**IMMDevice :: Activate**</span><span class="sxs-lookup"><span data-stu-id="fd61c-146">**IMMDevice::Activate**</span></span>](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[<span data-ttu-id="fd61c-147">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="fd61c-147">**ISimpleAudioVolume**</span></span>](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[<span data-ttu-id="fd61c-148">**Guide de référence de programmation**</span><span class="sxs-lookup"><span data-stu-id="fd61c-148">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



