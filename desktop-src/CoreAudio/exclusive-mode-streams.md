---
description: Flux de Exclusive-Mode
ms.assetid: 196cc6fe-91bf-46fa-acc9-38a7a4005875
title: Flux de Exclusive-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 677efa83d099bd32ddb0674414e25a9af219bd1a
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068585"
---
# <a name="exclusive-mode-streams"></a><span data-ttu-id="406d8-103">Flux de Exclusive-Mode</span><span class="sxs-lookup"><span data-stu-id="406d8-103">Exclusive-Mode Streams</span></span>

<span data-ttu-id="406d8-104">Comme expliqué précédemment, si une application ouvre un flux en mode exclusif, l’application utilise exclusivement l’appareil de point de terminaison audio qui lit ou enregistre le flux.</span><span class="sxs-lookup"><span data-stu-id="406d8-104">As explained previously, if an application opens a stream in exclusive mode, the application has exclusive use of the audio endpoint device that plays or records the stream.</span></span> <span data-ttu-id="406d8-105">En revanche, plusieurs applications peuvent partager un périphérique de point de terminaison audio en ouvrant des flux en mode partagé sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="406d8-105">In contrast, several applications can share an audio endpoint device by opening shared-mode streams on the device.</span></span>

<span data-ttu-id="406d8-106">L’accès en mode exclusif à un périphérique audio peut bloquer les sons importants du système, empêcher l’interopérabilité avec d’autres applications et dégrader l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="406d8-106">Exclusive-mode access to an audio device can block crucial system sounds, prevent interoperability with other applications, and otherwise degrade the user experience.</span></span> <span data-ttu-id="406d8-107">Pour atténuer ces problèmes, une application avec un flux en mode exclusif abandonne généralement le contrôle du périphérique audio lorsque l’application n’est pas le processus de premier plan ou n’est pas active en continu.</span><span class="sxs-lookup"><span data-stu-id="406d8-107">To mitigate these problems, an application with an exclusive-mode stream typically relinquishes control of the audio device when the application is not the foreground process or is not actively streaming.</span></span>

<span data-ttu-id="406d8-108">La latence du flux est le délai inhérent au chemin de données qui connecte la mémoire tampon de point de terminaison d’une application à un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-108">Stream latency is the delay that is inherent in the data path that connects an application's endpoint buffer with an audio endpoint device.</span></span> <span data-ttu-id="406d8-109">Pour un flux de rendu, la latence est le délai maximal entre le moment où une application écrit un échantillon dans une mémoire tampon de point de terminaison et le moment où l’échantillon est audible à travers les intervenants.</span><span class="sxs-lookup"><span data-stu-id="406d8-109">For a rendering stream, the latency is the maximum delay from the time that an application writes a sample to an endpoint buffer to the time that the sample is heard through the speakers.</span></span> <span data-ttu-id="406d8-110">Pour un flux de capture, la latence est le délai maximal entre le moment où un son entre dans le microphone et le moment où une application peut lire l’exemple pour ce son à partir du tampon de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="406d8-110">For a capture stream, the latency is the maximum delay from the time that a sound enters the microphone to the time that an application can read the sample for that sound from the endpoint buffer.</span></span>

<span data-ttu-id="406d8-111">Les applications qui utilisent des flux en mode exclusif le font souvent, car elles nécessitent des latences faibles dans les chemins d’accès aux données entre les périphériques de point de terminaison audio et les threads d’application qui accèdent aux mémoires tampons de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="406d8-111">Applications that use exclusive-mode streams often do so because they require low latencies in the data paths between the audio endpoint devices and the application threads that access the endpoint buffers.</span></span> <span data-ttu-id="406d8-112">En règle générale, ces threads s’exécutent en priorité relativement élevée et se planifient pour s’exécuter à intervalles réguliers qui sont proches ou identiques à l’intervalle périodique qui sépare les passages successifs de traitement par le matériel audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-112">Typically, these threads run at relatively high priority and schedule themselves to run at periodic intervals that are close to or the same as the periodic interval that separates successive processing passes by the audio hardware.</span></span> <span data-ttu-id="406d8-113">Pendant chaque passe, le matériel audio traite les nouvelles données dans les mémoires tampons de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="406d8-113">During each pass, the audio hardware processes the new data in the endpoint buffers.</span></span>

<span data-ttu-id="406d8-114">Pour obtenir les plus petites latences de flux, une application peut nécessiter un matériel audio spécial et un système informatique légèrement chargé.</span><span class="sxs-lookup"><span data-stu-id="406d8-114">To achieve the smallest stream latencies, an application might require both special audio hardware, and a computer system that is lightly loaded.</span></span> <span data-ttu-id="406d8-115">La conduite du matériel audio au-delà de ses limites de synchronisation ou du chargement du système avec des tâches haute priorité concurrentes peut provoquer un problème dans un flux audio à faible latence.</span><span class="sxs-lookup"><span data-stu-id="406d8-115">Driving the audio hardware beyond its timing limits or loading the system with competing high-priority tasks might cause a glitch in a low-latency audio stream.</span></span> <span data-ttu-id="406d8-116">Par exemple, pour un flux de rendu, un problème peut se produire si l’écriture de l’application échoue dans une mémoire tampon de point de terminaison avant que le matériel audio ne lise la mémoire tampon, ou si le matériel ne parvient pas à lire le tampon avant que la mémoire tampon ne soit planifiée.</span><span class="sxs-lookup"><span data-stu-id="406d8-116">For example, for a rendering stream, a glitch can occur if the application fails to write to an endpoint buffer before the audio hardware reads the buffer, or if the hardware fails to read the buffer before the time that the buffer is scheduled to play.</span></span> <span data-ttu-id="406d8-117">En règle générale, une application destinée à être exécutée sur une grande variété de matériel audio et dans un large éventail de systèmes doit être suffisamment longue pour éviter des problèmes dans tous les environnements cibles.</span><span class="sxs-lookup"><span data-stu-id="406d8-117">Typically, an application that is intended to run on a wide variety of audio hardware and in a broad range of systems should relax its timing requirements enough to avoid glitches in all target environments.</span></span>

<span data-ttu-id="406d8-118">Windows Vista offre plusieurs fonctionnalités pour prendre en charge les applications qui nécessitent des flux audio à faible latence.</span><span class="sxs-lookup"><span data-stu-id="406d8-118">Windows Vista has several features to support applications that require low-latency audio streams.</span></span> <span data-ttu-id="406d8-119">Comme indiqué dans les [composants audio en mode utilisateur](user-mode-audio-components.md), les applications qui effectuent des opérations critiques peuvent appeler les fonctions du service Planificateur de classes multimédias (MMCSS) pour augmenter la priorité des threads sans refuser les ressources du processeur aux applications de faible priorité.</span><span class="sxs-lookup"><span data-stu-id="406d8-119">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), applications that perform time-critical operations can call the Multimedia Class Scheduler Service (MMCSS) functions to increase thread priority without denying CPU resources to lower-priority applications.</span></span> <span data-ttu-id="406d8-120">En outre, la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) prend en charge un \_ indicateur de EventCallback suivante STREAMFLAGS AUDCLNT \_ qui permet au thread de maintenance de mémoire tampon d’une application de planifier son exécution lorsqu’une nouvelle mémoire tampon est disponible à partir du périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-120">In addition, the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method supports an AUDCLNT\_STREAMFLAGS\_EVENTCALLBACK flag that enables an application's buffer-servicing thread to schedule its execution to occur when a new buffer becomes available from the audio device.</span></span> <span data-ttu-id="406d8-121">En utilisant ces fonctionnalités, un thread d’application peut réduire l’incertitude quant au moment de son exécution, ce qui réduit le risque de problèmes dans un flux audio à faible latence.</span><span class="sxs-lookup"><span data-stu-id="406d8-121">By using these features, an application thread can reduce uncertainty about when it will execute, thereby decreasing the risk of glitches in a low-latency audio stream.</span></span>

<span data-ttu-id="406d8-122">Les pilotes pour les cartes audio plus anciennes sont susceptibles d’utiliser l’interface DDI WaveCyclic ou WavePci, tandis que les pilotes pour les cartes audio plus récentes sont plus susceptibles de prendre en charge l’interface DDI WaveRT.</span><span class="sxs-lookup"><span data-stu-id="406d8-122">The drivers for older audio adapters are likely to use the WaveCyclic or WavePci device driver interface (DDI), whereas the drivers for newer audio adapters are more likely to support the WaveRT DDI.</span></span> <span data-ttu-id="406d8-123">Pour les applications en mode exclusif, les pilotes WaveRT peuvent offrir de meilleures performances que les pilotes WaveCyclic ou WavePci, mais les pilotes WaveRT requièrent des capacités matérielles supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="406d8-123">For exclusive-mode applications, WaveRT drivers can provide better performance than WaveCyclic or WavePci drivers, but WaveRT drivers require additional hardware capabilities.</span></span> <span data-ttu-id="406d8-124">Ces fonctionnalités incluent la possibilité de partager des mémoires tampons matérielles directement avec les applications.</span><span class="sxs-lookup"><span data-stu-id="406d8-124">These capabilities include the ability to share hardware buffers directly with applications.</span></span> <span data-ttu-id="406d8-125">Avec le partage direct, aucune intervention du système n’est requise pour transférer des données entre une application en mode exclusif et le matériel audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-125">With direct sharing, no system intervention is required to transfer data between an exclusive-mode application and the audio hardware.</span></span> <span data-ttu-id="406d8-126">En revanche, les pilotes WaveCyclic et WavePci conviennent aux cartes audio plus anciennes et moins compatibles.</span><span class="sxs-lookup"><span data-stu-id="406d8-126">In contrast, WaveCyclic and WavePci drivers are suitable for older, less capable audio adapters.</span></span> <span data-ttu-id="406d8-127">Ces adaptateurs s’appuient sur des logiciels système pour transporter des blocs de données (attachés à des paquets de demande d’e/s système ou des IRP) entre les mémoires tampons d’application et les mémoires tampons matérielles.</span><span class="sxs-lookup"><span data-stu-id="406d8-127">These adapters rely on system software to transport blocks of data (attached to system I/O request packets, or IRPs) between application buffers and hardware buffers.</span></span> <span data-ttu-id="406d8-128">En outre, les périphériques audio USB s’appuient sur des logiciels système pour transporter des données entre les mémoires tampons d’application et les mémoires tampons matérielles.</span><span class="sxs-lookup"><span data-stu-id="406d8-128">In addition, USB audio devices rely on system software to transport data between application buffers and hardware buffers.</span></span> <span data-ttu-id="406d8-129">Pour améliorer les performances des applications en mode exclusif qui se connectent aux périphériques audio qui reposent sur le système pour le transport de données, WASAPI augmente automatiquement la priorité des threads système qui transfèrent les données entre les applications et le matériel.</span><span class="sxs-lookup"><span data-stu-id="406d8-129">To improve the performance of exclusive-mode applications that connect to audio devices that rely on the system for data transport, WASAPI automatically increases the priority of the system threads that transfer data between the applications and the hardware.</span></span> <span data-ttu-id="406d8-130">WASAPI utilise MMCSS pour augmenter la priorité des threads.</span><span class="sxs-lookup"><span data-stu-id="406d8-130">WASAPI uses MMCSS to increase the thread priority.</span></span> <span data-ttu-id="406d8-131">Dans Windows Vista, si un thread système gère le transport de données pour un flux de lecture audio en mode exclusif avec un format PCM et une période d’appareil inférieure à 10 millisecondes, WASAPI affecte le nom de tâche MMCSS « Pro audio » au thread.</span><span class="sxs-lookup"><span data-stu-id="406d8-131">In Windows Vista, if a system thread manages data transport for an exclusive-mode audio playback stream with a PCM format and a device period of less than 10 milliseconds, WASAPI assigns the MMCSS task name "Pro Audio" to the thread.</span></span> <span data-ttu-id="406d8-132">Si la période d’appareil du flux est supérieure ou égale à 10 millisecondes, WASAPI assigne le nom de tâche MMCSS « audio » au thread.</span><span class="sxs-lookup"><span data-stu-id="406d8-132">If the device period of the stream is greater than or equal to 10 milliseconds, WASAPI assigns the MMCSS task name "Audio" to the thread.</span></span> <span data-ttu-id="406d8-133">Pour plus d’informations sur les DDIs WaveCyclic, WavePci et WaveRT, consultez la documentation de Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="406d8-133">For more information about the WaveCyclic, WavePci, and WaveRT DDIs, see the Windows DDK documentation.</span></span> <span data-ttu-id="406d8-134">Pour plus d’informations sur la sélection d’une période d’appareil appropriée, consultez [**IAudioClient :: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span><span class="sxs-lookup"><span data-stu-id="406d8-134">For information about selecting an appropriate device period, see [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod).</span></span>

<span data-ttu-id="406d8-135">Comme décrit dans la section [contrôles de volume de session](session-volume-controls.md), [WASAPI](wasapi.md) fournit les interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)et [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) pour contrôler les niveaux de volume des flux audio en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="406d8-135">As described in [Session Volume Controls](session-volume-controls.md), [WASAPI](wasapi.md) provides the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces for controlling the volume levels of shared-mode audio streams.</span></span> <span data-ttu-id="406d8-136">Toutefois, les contrôles dans ces interfaces n’ont aucun effet sur les flux en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="406d8-136">However, the controls in these interfaces have no effect on exclusive-mode streams.</span></span> <span data-ttu-id="406d8-137">Au lieu de cela, les applications qui gèrent des flux en mode exclusif utilisent généralement l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) dans l' [API EndpointVolume](endpointvolume-api.md) pour contrôler les niveaux de volume de ces flux.</span><span class="sxs-lookup"><span data-stu-id="406d8-137">Instead, applications that manage exclusive-mode streams typically use the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface in the [EndpointVolume API](endpointvolume-api.md) to control the volume levels of those streams.</span></span> <span data-ttu-id="406d8-138">Pour plus d’informations sur cette interface, consultez [contrôles du volume du point de terminaison](endpoint-volume-controls.md).</span><span class="sxs-lookup"><span data-stu-id="406d8-138">For information about this interface, see [Endpoint Volume Controls](endpoint-volume-controls.md).</span></span>

<span data-ttu-id="406d8-139">Pour chaque périphérique de lecture et périphérique de capture dans le système, l’utilisateur peut contrôler si l’appareil peut être utilisé en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="406d8-139">For each playback device and capture device in the system, the user can control whether the device can be used in exclusive mode.</span></span> <span data-ttu-id="406d8-140">Si l’utilisateur désactive l’utilisation en mode exclusif de l’appareil, l’appareil peut être utilisé pour lire ou enregistrer uniquement des flux en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="406d8-140">If the user disables exclusive-mode use of the device, the device can be used to play or record only shared-mode streams.</span></span>

<span data-ttu-id="406d8-141">Si l’utilisateur active l’utilisation en mode exclusif de l’appareil, l’utilisateur peut également contrôler si une demande d’utilisation de l’appareil en mode exclusif par une application est préoccupée par l’utilisation de l’appareil par des applications qui peuvent actuellement exécuter ou enregistrer des flux en mode partagé via l’appareil.</span><span class="sxs-lookup"><span data-stu-id="406d8-141">If the user enables exclusive-mode use of the device, the user can also control whether a request by an application to use the device in exclusive mode will preempt the use of the device by applications that might currently be playing or recording shared-mode streams through the device.</span></span> <span data-ttu-id="406d8-142">Si la préemption est activée, une demande par une application pour prendre le contrôle exclusif de l’appareil réussit si l’appareil n’est pas en cours d’utilisation ou si l’appareil est utilisé en mode partagé, mais la demande échoue si une autre application a déjà le contrôle exclusif de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="406d8-142">If preemption is enabled, a request by an application to take exclusive control of the device succeeds if the device is currently not in use, or if the device is being used in shared mode, but the request fails if another application already has exclusive control of the device.</span></span> <span data-ttu-id="406d8-143">Si la préemption est désactivée, une demande d’une application qui prend le contrôle exclusif de l’appareil réussit si l’appareil n’est pas en cours d’utilisation, mais la demande échoue si l’appareil est déjà utilisé en mode partagé ou en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="406d8-143">If preemption is disabled, a request by an application to take exclusive control of the device succeeds if the device is not currently in use, but the request fails if the device is already being used either in shared mode or in exclusive mode.</span></span>

<span data-ttu-id="406d8-144">Dans Windows Vista, les paramètres par défaut pour un périphérique de point de terminaison audio sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="406d8-144">In Windows Vista, the default settings for an audio endpoint device are the following:</span></span>

-   <span data-ttu-id="406d8-145">L’appareil peut être utilisé pour lire ou enregistrer des flux en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="406d8-145">The device can be used to play or record exclusive-mode streams.</span></span>
-   <span data-ttu-id="406d8-146">Une demande d’utilisation d’un appareil pour lire ou enregistrer un flux en mode exclusif prévaut sur tout flux en mode partagé en cours de lecture ou d’enregistrement via l’appareil.</span><span class="sxs-lookup"><span data-stu-id="406d8-146">A request to use a device to play or record an exclusive-mode stream preempts any shared-mode stream that is currently being played or recorded through the device.</span></span>

<span data-ttu-id="406d8-147">**Pour modifier les paramètres du mode exclusif d’un appareil de lecture ou d’enregistrement**</span><span class="sxs-lookup"><span data-stu-id="406d8-147">**To change the exclusive-mode settings of a playback or recording device**</span></span>

1.  <span data-ttu-id="406d8-148">Cliquez avec le bouton droit sur l’icône de haut-parleur dans la zone de notification, située sur le côté droit de la barre des tâches, puis sélectionnez **périphériques de lecture** ou **périphériques d’enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="406d8-148">Right-click the speaker icon in the notification area, which is located on the right side of the taskbar, and select **Playback Devices** or **Recording Devices**.</span></span> <span data-ttu-id="406d8-149">(Vous pouvez également exécuter le panneau de configuration Windows multimédia, Mmsys.cpl, à partir d’une fenêtre d’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="406d8-149">(As an alternative, run the Windows multimedia control panel, Mmsys.cpl, from a Command Prompt window.</span></span> <span data-ttu-id="406d8-150">Pour plus d’informations, consultez la section Notes dans les [ \_ \_ constantes](device-state-xxx-constants.md)de l’état de l’appareil xxx.)</span><span class="sxs-lookup"><span data-stu-id="406d8-150">For more information, see Remarks in [DEVICE\_STATE\_XXX Constants](device-state-xxx-constants.md).)</span></span>
2.  <span data-ttu-id="406d8-151">Une fois la fenêtre **audio** affichée, sélectionnez **lecture** ou **enregistrement**.</span><span class="sxs-lookup"><span data-stu-id="406d8-151">After the **Sound** window appears, select **Playback** or **Recording**.</span></span> <span data-ttu-id="406d8-152">Sélectionnez ensuite une entrée dans la liste des noms d’appareils, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="406d8-152">Next, select an entry in the list of device names, and click **Properties**.</span></span>
3.  <span data-ttu-id="406d8-153">Une fois que la fenêtre **Propriétés** s’affiche, cliquez sur **avancé**.</span><span class="sxs-lookup"><span data-stu-id="406d8-153">After the **Properties** window appears, click **Advanced**.</span></span>
4.  <span data-ttu-id="406d8-154">Pour permettre aux applications d’utiliser l’appareil en mode exclusif, cochez la case **autoriser les applications à prendre le contrôle exclusif de cet appareil**.</span><span class="sxs-lookup"><span data-stu-id="406d8-154">To enable applications to use the device in exclusive mode, check the box labeled **Allow applications to take exclusive control of this device**.</span></span> <span data-ttu-id="406d8-155">Pour désactiver l’utilisation en mode exclusif de l’appareil, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="406d8-155">To disable exclusive-mode use of the device, clear the check box.</span></span>
5.  <span data-ttu-id="406d8-156">Si l’utilisation du mode exclusif de l’appareil est activée, vous pouvez spécifier si une demande de contrôle exclusif de l’appareil est réussie si l’appareil est en train de visionner ou d’enregistrer des flux en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="406d8-156">If exclusive-mode use of the device is enabled, you can specify whether a request for exclusive control of the device will succeed if the device is currently playing or recording shared-mode streams.</span></span> <span data-ttu-id="406d8-157">Pour attribuer la priorité aux applications en mode exclusif sur les applications en mode partagé, cochez la case **nommer les applications en mode exclusif priorité**.</span><span class="sxs-lookup"><span data-stu-id="406d8-157">To give exclusive-mode applications priority over shared-mode applications, check the box labeled **Give exclusive mode applications priority**.</span></span> <span data-ttu-id="406d8-158">Pour refuser la priorité des applications en mode exclusif sur les applications en mode partagé, désactivez la case à cocher.</span><span class="sxs-lookup"><span data-stu-id="406d8-158">To deny exclusive-mode applications priority over shared-mode applications, clear the check box.</span></span>

<span data-ttu-id="406d8-159">L’exemple de code suivant montre comment lire un flux audio à faible latence sur un périphérique de rendu audio configuré pour une utilisation en mode exclusif :</span><span class="sxs-lookup"><span data-stu-id="406d8-159">The following code example shows how to play a low-latency audio stream on an audio-rendering device that is configured for use in exclusive mode:</span></span>


```C++
//-----------------------------------------------------------
// Play an exclusive-mode stream on the default audio
// rendering device. The PlayExclusiveStream function uses
// event-driven buffering and MMCSS to play the stream at
// the minimum latency supported by the device.
//-----------------------------------------------------------

// REFERENCE_TIME time units per second and per millisecond
#define REFTIMES_PER_SEC  10000000
#define REFTIMES_PER_MILLISEC  10000

#define EXIT_ON_ERROR(hres)  \
              if (FAILED(hres)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
const IID IID_IAudioClient = __uuidof(IAudioClient);
const IID IID_IAudioRenderClient = __uuidof(IAudioRenderClient);

HRESULT PlayExclusiveStream(MyAudioSource *pMySource)
{
    HRESULT hr;
    REFERENCE_TIME hnsRequestedDuration = 0;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioClient *pAudioClient = NULL;
    IAudioRenderClient *pRenderClient = NULL;
    WAVEFORMATEX *pwfx = NULL;
    HANDLE hEvent = NULL;
    HANDLE hTask = NULL;
    UINT32 bufferFrameCount;
    BYTE *pData;
    DWORD flags = 0;
    DWORD taskIndex = 0;
    
    hr = CoCreateInstance(
           CLSID_MMDeviceEnumerator, NULL,
           CLSCTX_ALL, IID_IMMDeviceEnumerator,
           (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    hr = pEnumerator->GetDefaultAudioEndpoint(
                        eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(
                    IID_IAudioClient, CLSCTX_ALL,
                    NULL, (void**)&pAudioClient);
    EXIT_ON_ERROR(hr)

    // Call a helper function to negotiate with the audio
    // device for an exclusive-mode stream format.
    hr = GetStreamFormat(pAudioClient, &pwfx);
    EXIT_ON_ERROR(hr)

    // Initialize the stream to play at the minimum latency.
    hr = pAudioClient->GetDevicePeriod(NULL, &hnsRequestedDuration);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->Initialize(
                         AUDCLNT_SHAREMODE_EXCLUSIVE,
                         AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
                         hnsRequestedDuration,
                         hnsRequestedDuration,
                         pwfx,
                         NULL);
    if (hr == AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED) {
        // Align the buffer if needed, see IAudioClient::Initialize() documentation
        UINT32 nFrames = 0;
        hr = pAudioClient->GetBufferSize(&nFrames);
        EXIT_ON_ERROR(hr)
        hnsRequestedDuration = (REFERENCE_TIME)((double)REFTIMES_PER_SEC / pwfx->nSamplesPerSec * nFrames + 0.5);
        hr = pAudioClient->Initialize(
            AUDCLNT_SHAREMODE_EXCLUSIVE,
            AUDCLNT_STREAMFLAGS_EVENTCALLBACK,
            hnsRequestedDuration,
            hnsRequestedDuration,
            pwfx,
            NULL);
    }
    EXIT_ON_ERROR(hr)

    // Tell the audio source which format to use.
    hr = pMySource->SetFormat(pwfx);
    EXIT_ON_ERROR(hr)

    // Create an event handle and register it for
    // buffer-event notifications.
    hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (hEvent == NULL)
    {
        hr = E_FAIL;
        goto Exit;
    }

    hr = pAudioClient->SetEventHandle(hEvent);
    EXIT_ON_ERROR(hr);

    // Get the actual size of the two allocated buffers.
    hr = pAudioClient->GetBufferSize(&bufferFrameCount);
    EXIT_ON_ERROR(hr)

    hr = pAudioClient->GetService(
                         IID_IAudioRenderClient,
                         (void**)&pRenderClient);
    EXIT_ON_ERROR(hr)

    // To reduce latency, load the first buffer with data
    // from the audio source before starting the stream.
    hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
    EXIT_ON_ERROR(hr)

    hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
    EXIT_ON_ERROR(hr)

    hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
    EXIT_ON_ERROR(hr)

    // Ask MMCSS to temporarily boost the thread priority
    // to reduce glitches while the low-latency stream plays.
    hTask = AvSetMmThreadCharacteristics(TEXT("Pro Audio"), &taskIndex);
    if (hTask == NULL)
    {
        hr = E_FAIL;
        EXIT_ON_ERROR(hr)
    }

    hr = pAudioClient->Start();  // Start playing.
    EXIT_ON_ERROR(hr)

    // Each loop fills one of the two buffers.
    while (flags != AUDCLNT_BUFFERFLAGS_SILENT)
    {
        // Wait for next buffer event to be signaled.
        DWORD retval = WaitForSingleObject(hEvent, 2000);
        if (retval != WAIT_OBJECT_0)
        {
            // Event handle timed out after a 2-second wait.
            pAudioClient->Stop();
            hr = ERROR_TIMEOUT;
            goto Exit;
        }

        // Grab the next empty buffer from the audio device.
        hr = pRenderClient->GetBuffer(bufferFrameCount, &pData);
        EXIT_ON_ERROR(hr)

        // Load the buffer with data from the audio source.
        hr = pMySource->LoadData(bufferFrameCount, pData, &flags);
        EXIT_ON_ERROR(hr)

        hr = pRenderClient->ReleaseBuffer(bufferFrameCount, flags);
        EXIT_ON_ERROR(hr)
    }

    // Wait for the last buffer to play before stopping.
    Sleep((DWORD)(hnsRequestedDuration/REFTIMES_PER_MILLISEC));

    hr = pAudioClient->Stop();  // Stop playing.
    EXIT_ON_ERROR(hr)

Exit:
    if (hEvent != NULL)
    {
        CloseHandle(hEvent);
    }
    if (hTask != NULL)
    {
        AvRevertMmThreadCharacteristics(hTask);
    }
    CoTaskMemFree(pwfx);
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pAudioClient)
    SAFE_RELEASE(pRenderClient)

    return hr;
}
```



<span data-ttu-id="406d8-160">Dans l’exemple de code précédent, la fonction PlayExclusiveStream s’exécute dans le thread d’application qui sert les tampons de point de terminaison pendant la diffusion d’un flux de rendu.</span><span class="sxs-lookup"><span data-stu-id="406d8-160">In the preceding code example, the PlayExclusiveStream function runs in the application thread that services the endpoint buffers while a rendering stream is playing.</span></span> <span data-ttu-id="406d8-161">La fonction accepte un seul paramètre, pMySource, qui est un pointeur vers un objet qui appartient à une classe définie par le client, MyAudioSource.</span><span class="sxs-lookup"><span data-stu-id="406d8-161">The function takes a single parameter, pMySource, which is a pointer to an object that belongs to a client-defined class, MyAudioSource.</span></span> <span data-ttu-id="406d8-162">Cette classe a deux fonctions membres, LoadData et SetFormat, qui sont appelées dans l’exemple de code.</span><span class="sxs-lookup"><span data-stu-id="406d8-162">This class has two member functions, LoadData and SetFormat, that are called in the code example.</span></span> <span data-ttu-id="406d8-163">MyAudioSource est décrit dans [rendu d’un flux](rendering-a-stream.md).</span><span class="sxs-lookup"><span data-stu-id="406d8-163">MyAudioSource is described in [Rendering a Stream](rendering-a-stream.md).</span></span>

<span data-ttu-id="406d8-164">La fonction PlayExclusiveStream appelle une fonction d’assistance, GetStreamFormat, qui négocie avec le périphérique de rendu par défaut pour déterminer si l’appareil prend en charge un format de flux en mode exclusif pouvant être utilisé par l’application.</span><span class="sxs-lookup"><span data-stu-id="406d8-164">The PlayExclusiveStream function calls a helper function, GetStreamFormat, that negotiates with the default rendering device to determine whether the device supports an exclusive-mode stream format that is suitable for use by the application.</span></span> <span data-ttu-id="406d8-165">Le code de la fonction GetStreamFormat n’apparaît pas dans l’exemple de code ; Cela est dû au fait que les détails de son implémentation dépendent entièrement des exigences de l’application.</span><span class="sxs-lookup"><span data-stu-id="406d8-165">The code for the GetStreamFormat function does not appear in the code example; that is because the details of its implementation depend entirely on the requirements of the application.</span></span> <span data-ttu-id="406d8-166">Toutefois, le fonctionnement de la fonction GetStreamFormat peut être décrit simplement : elle appelle la méthode [**IAudioClient :: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) une ou plusieurs fois pour déterminer si l’appareil prend en charge un format approprié.</span><span class="sxs-lookup"><span data-stu-id="406d8-166">However, the operation of the GetStreamFormat function can be described simply—it calls the [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) method one or more times to determine whether the device supports a suitable format.</span></span> <span data-ttu-id="406d8-167">Les exigences de l’application déterminent les formats que GetStreamFormat présente à la méthode **IsFormatSupported** et l’ordre dans lequel elle les présente.</span><span class="sxs-lookup"><span data-stu-id="406d8-167">The requirements of the application dictate which formats GetStreamFormat presents to the **IsFormatSupported** method and the order in which it presents them.</span></span> <span data-ttu-id="406d8-168">Pour plus d’informations sur **IsFormatSupported**, consultez [formats de périphérique](device-formats.md).</span><span class="sxs-lookup"><span data-stu-id="406d8-168">For more information about **IsFormatSupported**, see [Device Formats](device-formats.md).</span></span>

<span data-ttu-id="406d8-169">Après l’appel de GetStreamFormat, la fonction PlayExclusiveStream appelle la méthode [**IAudioClient :: GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) pour obtenir la période de périphérique minimale prise en charge par le matériel audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-169">After the GetStreamFormat call, the PlayExclusiveStream function calls the [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod) method to obtain the minimum device period supported by the audio hardware.</span></span> <span data-ttu-id="406d8-170">Ensuite, la fonction appelle la méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) pour demander une durée de mémoire tampon égale à la période minimale.</span><span class="sxs-lookup"><span data-stu-id="406d8-170">Next, the function calls the [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) method to request a buffer duration equal to the minimum period.</span></span> <span data-ttu-id="406d8-171">Si l’appel est effectué, la méthode **Initialize** alloue deux tampons de point de terminaison, chacun d’entre eux ayant une durée égale à la période minimale.</span><span class="sxs-lookup"><span data-stu-id="406d8-171">If the call succeeds, the **Initialize** method allocates two endpoint buffers, each of which is equal in duration to the minimum period.</span></span> <span data-ttu-id="406d8-172">Plus tard, lorsque le flux audio commence à s’exécuter, l’application et le matériel audio partagent les deux mémoires tampons de la manière « ping-pong », c’est-à-dire que l’application écrit dans une mémoire tampon, le matériel lit à partir de l’autre mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="406d8-172">Later, when the audio stream begins running, the application and audio hardware will share the two buffers in "ping-pong" fashion—that is, while the application writes to one buffer, the hardware reads from the other buffer.</span></span>

<span data-ttu-id="406d8-173">Avant de démarrer le flux, la fonction PlayExclusiveStream effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="406d8-173">Before starting the stream, the PlayExclusiveStream function does the following:</span></span>

-   <span data-ttu-id="406d8-174">Crée et inscrit le descripteur d’événement par le biais duquel il recevra des notifications lorsque les mémoires tampons seront prêtes à être remplies.</span><span class="sxs-lookup"><span data-stu-id="406d8-174">Creates and registers the event handle through which it will receive notifications when buffers become ready to fill.</span></span>
-   <span data-ttu-id="406d8-175">Remplit la première mémoire tampon avec des données de la source audio pour réduire le délai à partir duquel le flux commence à s’exécuter lorsque le son initial est audible.</span><span class="sxs-lookup"><span data-stu-id="406d8-175">Fills the first buffer with data from the audio source to reduce the delay from when the stream starts running to when the initial sound is heard.</span></span>
-   <span data-ttu-id="406d8-176">Appelle la fonction **AvSetMmThreadCharacteristics** pour demander que MMCSS augmente la priorité du thread dans lequel PlayExclusiveStream s’exécute.</span><span class="sxs-lookup"><span data-stu-id="406d8-176">Calls the **AvSetMmThreadCharacteristics** function to request that MMCSS increase the priority of the thread in which PlayExclusiveStream executes.</span></span> <span data-ttu-id="406d8-177">(Lorsque l’exécution du flux s’arrête, l’appel de la fonction **AvRevertMmThreadCharacteristics** restaure la priorité du thread d’origine.)</span><span class="sxs-lookup"><span data-stu-id="406d8-177">(When the stream stops running, the **AvRevertMmThreadCharacteristics** function call restores the original thread priority.)</span></span>

<span data-ttu-id="406d8-178">Pour plus d’informations sur **AvSetMmThreadCharacteristics** et **AvRevertMmThreadCharacteristics**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="406d8-178">For more information about **AvSetMmThreadCharacteristics** and **AvRevertMmThreadCharacteristics**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="406d8-179">Pendant que le flux est en cours d’exécution, chaque itération de la boucle **while** dans l’exemple de code précédent remplit une mémoire tampon de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="406d8-179">While the stream is running, each iteration of the **while**-loop in the preceding code example fills one endpoint buffer.</span></span> <span data-ttu-id="406d8-180">Entre les itérations, l’appel de fonction **WaitForSingleObject** attend que le handle d’événement soit signalé.</span><span class="sxs-lookup"><span data-stu-id="406d8-180">Between iterations, the **WaitForSingleObject** function call waits for the event handle to be signaled.</span></span> <span data-ttu-id="406d8-181">Lorsque le descripteur est signalé, le corps de la boucle effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="406d8-181">When the handle is signaled, the loop body does the following:</span></span>

1.  <span data-ttu-id="406d8-182">Appelle la méthode [**IAudioRenderClient :: GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) pour accéder à la mémoire tampon suivante.</span><span class="sxs-lookup"><span data-stu-id="406d8-182">Calls the [**IAudioRenderClient::GetBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer) method to get the next buffer.</span></span>
2.  <span data-ttu-id="406d8-183">Remplit la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="406d8-183">Fills the buffer.</span></span>
3.  <span data-ttu-id="406d8-184">Appelle la méthode [**IAudioRenderClient :: ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) pour libérer la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="406d8-184">Calls the [**IAudioRenderClient::ReleaseBuffer**](/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-releasebuffer) method to release the buffer.</span></span>

<span data-ttu-id="406d8-185">Pour plus d’informations sur **WaitForSingleObject**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="406d8-185">For more information about **WaitForSingleObject**, see the Windows SDK documentation.</span></span>

<span data-ttu-id="406d8-186">Si la carte audio est contrôlée par un pilote WaveRT, la signalisation du descripteur d’événement est liée aux notifications de transfert DMA du matériel audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-186">If the audio adapter is controlled by a WaveRT driver, the signaling of the event handle is tied to the DMA-transfer notifications from the audio hardware.</span></span> <span data-ttu-id="406d8-187">Pour un périphérique audio USB ou pour un périphérique audio contrôlé par un pilote WaveCyclic ou WavePci, la signalisation du descripteur d’événement est liée à la saisie semi-automatique des IRP qui transfèrent les données de la mémoire tampon d’application vers la mémoire tampon matérielle.</span><span class="sxs-lookup"><span data-stu-id="406d8-187">For a USB audio device, or for an audio device that is controlled by a WaveCyclic or WavePci driver, the signaling of the event handle is tied to completions of the IRPs that transfer data from the application buffer to the hardware buffer.</span></span>

<span data-ttu-id="406d8-188">L’exemple de code précédent pousse le matériel audio et le système informatique à leurs limites de performances.</span><span class="sxs-lookup"><span data-stu-id="406d8-188">The preceding code example pushes the audio hardware and the computer system to their performance limits.</span></span> <span data-ttu-id="406d8-189">Tout d’abord, pour réduire la latence du flux, l’application planifie son thread de maintenance de mémoire tampon afin d’utiliser la période de périphérique minimale prise en charge par le matériel audio.</span><span class="sxs-lookup"><span data-stu-id="406d8-189">First, to reduce the stream latency, the application schedules its buffer-servicing thread to use the minimum device period that the audio hardware will support.</span></span> <span data-ttu-id="406d8-190">Deuxièmement, pour vous assurer que le thread s’exécute de manière fiable dans chaque période de l’appareil, l’appel de fonction **AvSetMmThreadCharacteristics** définit le paramètre TASKNAME sur « Pro Audio », qui est, dans Windows Vista, le nom de tâche par défaut avec la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="406d8-190">Second, to ensure that the thread reliably executes within each device period, the **AvSetMmThreadCharacteristics** function call sets the TaskName parameter to "Pro Audio", which is, in Windows Vista, the default task name with the highest priority.</span></span> <span data-ttu-id="406d8-191">Déterminez si les exigences de synchronisation de votre application peuvent être assouplies sans compromettre son utilité.</span><span class="sxs-lookup"><span data-stu-id="406d8-191">Consider whether the timing requirements of your application might be relaxed without compromising its usefulness.</span></span> <span data-ttu-id="406d8-192">Par exemple, l’application peut planifier son thread de maintenance de mémoire tampon pour utiliser une période plus longue que la valeur minimale.</span><span class="sxs-lookup"><span data-stu-id="406d8-192">For example, the application might schedule its buffer-servicing thread to use a period that is longer than the minimum.</span></span> <span data-ttu-id="406d8-193">Un délai plus long peut permettre d’utiliser en toute sécurité une priorité de thread inférieure.</span><span class="sxs-lookup"><span data-stu-id="406d8-193">A longer period might safely allow the use of a lower thread priority.</span></span>

## <a name="related-topics"></a><span data-ttu-id="406d8-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="406d8-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="406d8-195">Gestion de flux</span><span class="sxs-lookup"><span data-stu-id="406d8-195">Stream Management</span></span>](stream-management.md)
</dt> </dl>

 

 



