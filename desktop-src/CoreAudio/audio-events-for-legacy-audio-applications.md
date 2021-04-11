---
description: Événements audio pour les applications audio héritées
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Événements audio pour les applications audio héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111559"
---
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="d1246-103">Événements audio pour les applications audio héritées</span><span class="sxs-lookup"><span data-stu-id="d1246-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="d1246-104">Les API audio héritées telles que DirectSound, DirectShow et les fonctions **waveOutXxx** permettent aux applications d’acquérir et de définir les niveaux de volume des flux audio.</span><span class="sxs-lookup"><span data-stu-id="d1246-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="d1246-105">Les applications peuvent utiliser les fonctionnalités de contrôle de volume de ces API pour afficher des curseurs de volume dans leurs fenêtres d’application.</span><span class="sxs-lookup"><span data-stu-id="d1246-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="d1246-106">Dans Windows Vista, le programme de contrôle de volume système, sndvol, permet aux utilisateurs de contrôler les niveaux de volume audio pour des applications individuelles.</span><span class="sxs-lookup"><span data-stu-id="d1246-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="d1246-107">Les curseurs de volume affichés par les applications doivent être liés aux curseurs de volume correspondants dans sndvol.</span><span class="sxs-lookup"><span data-stu-id="d1246-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="d1246-108">Si un utilisateur ajuste le volume d’application par le biais d’un curseur de volume dans une fenêtre d’application, le curseur de volume correspondant dans sndvol se déplace immédiatement pour indiquer le nouveau niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="d1246-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="d1246-109">À l’inverse, si l’utilisateur ajuste le volume d’application par le biais de sndvol, les curseurs de volume dans la fenêtre d’application doivent être déplacés pour indiquer le nouveau niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="d1246-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="d1246-110">Dans Windows Vista, sndvol reflète immédiatement les modifications de volume qu’une application effectue via des appels à la méthode **IDirectSoundBuffer :: setVolume** ou à la fonction **waveOutSetVolume** .</span><span class="sxs-lookup"><span data-stu-id="d1246-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="d1246-111">Toutefois, une API audio héritée telle que DirectSound ou les fonctions **waveOutXxx** ne fournit aucun moyen de notifier une application lorsque l’utilisateur modifie le volume d’application par le biais de sndvol.</span><span class="sxs-lookup"><span data-stu-id="d1246-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="d1246-112">Si une application affiche un curseur de volume, mais ne reçoit pas de notifications de modifications de volume, le curseur ne reflète pas les modifications apportées par l’utilisateur dans sndvol.</span><span class="sxs-lookup"><span data-stu-id="d1246-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="d1246-113">Pour implémenter le comportement approprié, le concepteur d’application doit compenser l’absence de notifications par l’API audio héritée.</span><span class="sxs-lookup"><span data-stu-id="d1246-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="d1246-114">L’une des solutions peut être que l’application doit définir un minuteur pour lui rappeler régulièrement de vérifier le niveau du volume pour voir s’il a changé.</span><span class="sxs-lookup"><span data-stu-id="d1246-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="d1246-115">Une solution plus élégante consiste à ce que l’application utilise les fonctionnalités de notification d’événements des API audio principales.</span><span class="sxs-lookup"><span data-stu-id="d1246-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="d1246-116">En particulier, l’application peut inscrire une interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) pour recevoir des rappels lorsque des modifications de volume ou d’autres types d’événements audio se produisent.</span><span class="sxs-lookup"><span data-stu-id="d1246-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="d1246-117">Lorsque le volume change, la routine de rappel de modification de volume peut immédiatement mettre à jour le curseur de volume de l’application pour refléter la modification.</span><span class="sxs-lookup"><span data-stu-id="d1246-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="d1246-118">L’exemple de code suivant montre comment une application peut s’inscrire pour recevoir des notifications de modifications de volume et d’autres événements audio :</span><span class="sxs-lookup"><span data-stu-id="d1246-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



<span data-ttu-id="d1246-119">L’exemple de code précédent implémente une classe nommée AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="d1246-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="d1246-120">Pendant l’initialisation du programme, l’application audio active les notifications d’événements audio en créant un objet AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="d1246-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="d1246-121">Le constructeur de cette classe accepte trois paramètres d’entrée :</span><span class="sxs-lookup"><span data-stu-id="d1246-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="d1246-122">*Flow*: sens du flux de données de l' [appareil de point de terminaison audio](audio-endpoint-devices.md) (valeur d’énumération [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).</span><span class="sxs-lookup"><span data-stu-id="d1246-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="d1246-123">*rôle*: rôle d' [appareil](device-roles.md) actuel de l’appareil de point de terminaison (valeur d’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="d1246-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="d1246-124">*pAudioEvents*: pointeur vers un objet (instance d’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) qui contient un ensemble de routines de rappel implémentées par l’application.</span><span class="sxs-lookup"><span data-stu-id="d1246-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="d1246-125">Le constructeur fournit les valeurs de workflow et de rôle en tant que paramètres d’entrée à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) .</span><span class="sxs-lookup"><span data-stu-id="d1246-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="d1246-126">La méthode crée un objet [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui encapsule l’appareil de point de terminaison audio avec la direction de flux de données et le rôle d’appareil spécifiés.</span><span class="sxs-lookup"><span data-stu-id="d1246-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="d1246-127">L’application implémente l’objet pointé par *pAudioEvents*.</span><span class="sxs-lookup"><span data-stu-id="d1246-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="d1246-128">(L’implémentation n’est pas illustrée dans l’exemple de code précédent.</span><span class="sxs-lookup"><span data-stu-id="d1246-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="d1246-129">Pour obtenir un exemple de code qui implémente une interface **IAudioSessionEvents** , consultez [événements de session audio](audio-session-events.md).) Chaque méthode de cette interface reçoit des notifications d’un type particulier d’événement audio.</span><span class="sxs-lookup"><span data-stu-id="d1246-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="d1246-130">Si l’application ne s’intéresse pas à un type d’événement particulier, la méthode pour ce type d’événement ne doit faire rien, mais retourner la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d1246-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="d1246-131">La méthode [**IAudioSessionEvents :: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) reçoit des notifications de modifications de volume.</span><span class="sxs-lookup"><span data-stu-id="d1246-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="d1246-132">En général, cette méthode met à jour le curseur de volume de l’application.</span><span class="sxs-lookup"><span data-stu-id="d1246-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="d1246-133">Dans l’exemple de code précédent, le constructeur de la classe AudioVolumeEvents s’inscrit aux notifications sur la [session audio](audio-sessions.md) spécifique au processus qui est identifiée par la valeur GUID de la valeur GUID de session \_ .</span><span class="sxs-lookup"><span data-stu-id="d1246-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="d1246-134">Par défaut, les API audio héritées telles que DirectSound, DirectShow et les fonctions **waveOutXxx** affectent leurs flux à cette session.</span><span class="sxs-lookup"><span data-stu-id="d1246-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="d1246-135">Toutefois, une application DirectSound ou DirectShow peut, en option, remplacer le comportement par défaut et assigner ses flux à une session inter-processus ou à une session qui est identifiée par une valeur GUID autre que GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="d1246-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="d1246-136">(Aucun mécanisme n’est actuellement fourni pour qu’une application **waveOutXxx** remplace le comportement par défaut de la même manière.) Pour obtenir un exemple de code d’une application DirectShow avec ce comportement, consultez [rôles d’appareil pour les applications DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d1246-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="d1246-137">Pour prendre en charge une telle application, vous pouvez modifier le constructeur dans l’exemple de code précédent pour accepter deux paramètres d’entrée supplémentaires : un GUID de session et un indicateur pour indiquer si la session qui doit être analysée est une session inter-processus ou spécifique au processus.</span><span class="sxs-lookup"><span data-stu-id="d1246-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="d1246-138">Transmettez ces paramètres à l’appel à la méthode [**IAudioSessionManager :: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) dans le constructeur.</span><span class="sxs-lookup"><span data-stu-id="d1246-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="d1246-139">Une fois que le constructeur a appelé la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) pour s’inscrire aux notifications, l’application continue à recevoir des notifications uniquement tant que l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ou [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) existe.</span><span class="sxs-lookup"><span data-stu-id="d1246-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="d1246-140">L’objet AudioVolumeEvents dans l’exemple de code précédent contient des références à ces interfaces jusqu’à ce que son destructeur soit appelé.</span><span class="sxs-lookup"><span data-stu-id="d1246-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="d1246-141">Ce comportement garantit que l’application continuera à recevoir des notifications pendant la durée de vie de l’objet AudioVolumeEvents.</span><span class="sxs-lookup"><span data-stu-id="d1246-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="d1246-142">Au lieu de sélectionner implicitement un périphérique audio en fonction de son rôle d’appareil, une application Windows multimédia DirectSound ou héritée peut permettre à l’utilisateur de sélectionner explicitement un appareil dans la liste des appareils disponibles identifiés par leur nom convivial.</span><span class="sxs-lookup"><span data-stu-id="d1246-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="d1246-143">Pour prendre en charge ce comportement, l’exemple de code précédent doit être modifié afin de générer des notifications d’événements audio pour l’appareil sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d1246-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="d1246-144">Deux modifications sont requises.</span><span class="sxs-lookup"><span data-stu-id="d1246-144">Two modifications are required.</span></span> <span data-ttu-id="d1246-145">Tout d’abord, modifiez la définition du constructeur pour accepter une [chaîne d’ID de point de terminaison](endpoint-id-strings.md) en tant que paramètre d’entrée (à la place des paramètres de workflow et de rôle dans l’exemple de code).</span><span class="sxs-lookup"><span data-stu-id="d1246-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="d1246-146">Cette chaîne identifie le périphérique de point de terminaison audio qui correspond à l’appareil DirectSound ou à la forme d’onde héritée sélectionné.</span><span class="sxs-lookup"><span data-stu-id="d1246-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="d1246-147">Ensuite, remplacez l’appel à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) par un appel à la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="d1246-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="d1246-148">L’appel **GetDevice** prend la chaîne d’ID de point de terminaison comme paramètre d’entrée et crée une instance de l’appareil de point de terminaison identifié par la chaîne.</span><span class="sxs-lookup"><span data-stu-id="d1246-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="d1246-149">La technique d’obtention de la chaîne d’ID de point de terminaison pour un périphérique DirectSound ou un appareil Waveform hérité est la suivante.</span><span class="sxs-lookup"><span data-stu-id="d1246-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="d1246-150">Tout d’abord, pendant l’énumération d’appareils, DirectSound fournit la chaîne d’ID de point de terminaison pour chaque périphérique énuméré.</span><span class="sxs-lookup"><span data-stu-id="d1246-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="d1246-151">Pour commencer l’énumération de l’appareil, l’application passe un pointeur de fonction de rappel comme paramètre d’entrée à la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** .</span><span class="sxs-lookup"><span data-stu-id="d1246-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="d1246-152">La définition de la fonction de rappel est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d1246-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="d1246-153">Dans Windows Vista, le paramètre *lpcstrModule* pointe vers la chaîne d’ID de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d1246-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="d1246-154">(Dans les versions antérieures de Windows, y compris Windows Server 2003, Windows XP et Windows 2000, le paramètre *lpcstrModule* pointe vers le nom du module de pilote de l’appareil.) Le paramètre *lpcstrDescription* pointe vers une chaîne qui contient le nom convivial de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d1246-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="d1246-155">Pour plus d’informations sur l’énumération des appareils DirectSound, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d1246-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="d1246-156">Deuxièmement, pour obtenir la chaîne d’ID de point de terminaison pour un périphérique Waveform hérité, utilisez la fonction **waveOutMessage** ou **waveInMessage** pour envoyer un \_ message DRV QUERYFUNCTIONINSTANCEID au pilote de périphérique Waveform.</span><span class="sxs-lookup"><span data-stu-id="d1246-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="d1246-157">Pour obtenir un exemple de code illustrant l’utilisation de ce message, consultez [rôles d’appareil pour les applications multimédias Windows héritées](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d1246-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1246-158">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d1246-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1246-159">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="d1246-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



