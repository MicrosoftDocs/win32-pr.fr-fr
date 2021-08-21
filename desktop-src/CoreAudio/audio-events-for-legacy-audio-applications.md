---
description: Événements audio pour les applications audio héritées
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: Événements audio pour les applications audio héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030561123ba8501a66a2837bcc323a6505226a80c385f3dcaa532b2e6cd8c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018487"
---
# <a name="audio-events-for-legacy-audio-applications"></a>Événements audio pour les applications audio héritées

les api audio héritées telles que DirectSound, DirectShow et les fonctions **waveOutXxx** permettent aux applications d’acquérir et de définir les niveaux de volume des flux audio. Les applications peuvent utiliser les fonctionnalités de contrôle de volume de ces API pour afficher des curseurs de volume dans leurs fenêtres d’application.

dans Windows Vista, le programme de contrôle de volume système, Sndvol, permet aux utilisateurs de contrôler les niveaux de volume audio pour des applications individuelles. Les curseurs de volume affichés par les applications doivent être liés aux curseurs de volume correspondants dans sndvol. Si un utilisateur ajuste le volume d’application par le biais d’un curseur de volume dans une fenêtre d’application, le curseur de volume correspondant dans sndvol se déplace immédiatement pour indiquer le nouveau niveau de volume. À l’inverse, si l’utilisateur ajuste le volume d’application par le biais de sndvol, les curseurs de volume dans la fenêtre d’application doivent être déplacés pour indiquer le nouveau niveau de volume.

dans Windows Vista, Sndvol reflète immédiatement les modifications de volume qu’une application effectue via des appels à la méthode **IDirectSoundBuffer :: SetVolume** ou à la fonction **waveOutSetVolume** . Toutefois, une API audio héritée telle que DirectSound ou les fonctions **waveOutXxx** ne fournit aucun moyen de notifier une application lorsque l’utilisateur modifie le volume d’application par le biais de sndvol. Si une application affiche un curseur de volume, mais ne reçoit pas de notifications de modifications de volume, le curseur ne reflète pas les modifications apportées par l’utilisateur dans sndvol. Pour implémenter le comportement approprié, le concepteur d’application doit compenser l’absence de notifications par l’API audio héritée.

L’une des solutions peut être que l’application doit définir un minuteur pour lui rappeler régulièrement de vérifier le niveau du volume pour voir s’il a changé.

Une solution plus élégante consiste à ce que l’application utilise les fonctionnalités de notification d’événements des API audio principales. En particulier, l’application peut inscrire une interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) pour recevoir des rappels lorsque des modifications de volume ou d’autres types d’événements audio se produisent. Lorsque le volume change, la routine de rappel de modification de volume peut immédiatement mettre à jour le curseur de volume de l’application pour refléter la modification.

L’exemple de code suivant montre comment une application peut s’inscrire pour recevoir des notifications de modifications de volume et d’autres événements audio :


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



L’exemple de code précédent implémente une classe nommée AudioVolumeEvents. Pendant l’initialisation du programme, l’application audio active les notifications d’événements audio en créant un objet AudioVolumeEvents. Le constructeur de cette classe accepte trois paramètres d’entrée :

-   *Flow*: sens du flux de données de l' [appareil de point de terminaison audio](audio-endpoint-devices.md) (valeur d’énumération [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).
-   *rôle*: rôle d' [appareil](device-roles.md) actuel de l’appareil de point de terminaison (valeur d’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *pAudioEvents*: pointeur vers un objet (instance d’interface [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ) qui contient un ensemble de routines de rappel implémentées par l’application.

Le constructeur fournit les valeurs de workflow et de rôle en tant que paramètres d’entrée à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) . La méthode crée un objet [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) qui encapsule l’appareil de point de terminaison audio avec la direction de flux de données et le rôle d’appareil spécifiés.

L’application implémente l’objet pointé par *pAudioEvents*. (L’implémentation n’est pas illustrée dans l’exemple de code précédent. Pour obtenir un exemple de code qui implémente une interface **IAudioSessionEvents** , consultez [événements de session audio](audio-session-events.md).) Chaque méthode de cette interface reçoit des notifications d’un type particulier d’événement audio. Si l’application ne s’intéresse pas à un type d’événement particulier, la méthode pour ce type d’événement ne doit faire rien, mais retourner la valeur \_ OK.

La méthode [**IAudioSessionEvents :: OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) reçoit des notifications de modifications de volume. En général, cette méthode met à jour le curseur de volume de l’application.

Dans l’exemple de code précédent, le constructeur de la classe AudioVolumeEvents s’inscrit aux notifications sur la [session audio](audio-sessions.md) spécifique au processus qui est identifiée par la valeur GUID de la valeur GUID de session \_ . par défaut, les api audio héritées telles que DirectSound, DirectShow et les fonctions **waveOutXxx** affectent leurs flux à cette session. toutefois, une application DirectSound ou DirectShow peut, en option, remplacer le comportement par défaut et assigner ses flux à une session inter-processus ou à une session qui est identifiée par une valeur guid autre que guid \_ NULL. (Aucun mécanisme n’est actuellement fourni pour qu’une application **waveOutXxx** remplace le comportement par défaut de la même manière.) pour obtenir un exemple de code d’une application DirectShow avec ce comportement, consultez [rôles d’appareil pour les Applications DirectShow](device-roles-for-directshow-applications.md). Pour prendre en charge une telle application, vous pouvez modifier le constructeur dans l’exemple de code précédent pour accepter deux paramètres d’entrée supplémentaires : un GUID de session et un indicateur pour indiquer si la session qui doit être analysée est une session inter-processus ou spécifique au processus. Transmettez ces paramètres à l’appel à la méthode [**IAudioSessionManager :: GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) dans le constructeur.

Une fois que le constructeur a appelé la méthode [**IAudioSessionControl :: RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) pour s’inscrire aux notifications, l’application continue à recevoir des notifications uniquement tant que l’interface [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) ou [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) existe. L’objet AudioVolumeEvents dans l’exemple de code précédent contient des références à ces interfaces jusqu’à ce que son destructeur soit appelé. Ce comportement garantit que l’application continuera à recevoir des notifications pendant la durée de vie de l’objet AudioVolumeEvents.

au lieu de sélectionner implicitement un périphérique audio en fonction de son rôle d’appareil, une application multimédia DirectSound ou héritée Windows peut permettre à l’utilisateur de sélectionner explicitement un appareil dans la liste des appareils disponibles identifiés par leur nom convivial. Pour prendre en charge ce comportement, l’exemple de code précédent doit être modifié afin de générer des notifications d’événements audio pour l’appareil sélectionné. Deux modifications sont requises. Tout d’abord, modifiez la définition du constructeur pour accepter une [chaîne d’ID de point de terminaison](endpoint-id-strings.md) en tant que paramètre d’entrée (à la place des paramètres de workflow et de rôle dans l’exemple de code). Cette chaîne identifie le périphérique de point de terminaison audio qui correspond à l’appareil DirectSound ou à la forme d’onde héritée sélectionné. Ensuite, remplacez l’appel à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) par un appel à la méthode [**IMMDeviceEnumerator :: GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . L’appel **GetDevice** prend la chaîne d’ID de point de terminaison comme paramètre d’entrée et crée une instance de l’appareil de point de terminaison identifié par la chaîne.

La technique d’obtention de la chaîne d’ID de point de terminaison pour un périphérique DirectSound ou un appareil Waveform hérité est la suivante.

Tout d’abord, pendant l’énumération d’appareils, DirectSound fournit la chaîne d’ID de point de terminaison pour chaque périphérique énuméré. Pour commencer l’énumération de l’appareil, l’application passe un pointeur de fonction de rappel comme paramètre d’entrée à la fonction **DirectSoundCreate** ou **DirectSoundCaptureCreate** . La définition de la fonction de rappel est la suivante :


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



dans Windows Vista, le paramètre *lpcstrModule* pointe vers la chaîne d’ID de point de terminaison. (dans les versions antérieures de Windows, y compris Windows Server 2003, Windows XP et Windows 2000, le paramètre *lpcstrModule* pointe vers le nom du module de pilote de l’appareil.) Le paramètre *lpcstrDescription* pointe vers une chaîne qui contient le nom convivial de l’appareil. pour plus d’informations sur l’énumération des appareils DirectSound, consultez la documentation SDK Windows.

Deuxièmement, pour obtenir la chaîne d’ID de point de terminaison pour un périphérique Waveform hérité, utilisez la fonction **waveOutMessage** ou **waveInMessage** pour envoyer un \_ message DRV QUERYFUNCTIONINSTANCEID au pilote de périphérique Waveform. pour obtenir un exemple de code illustrant l’utilisation de ce message, consultez [rôles d’appareil pour les Applications multimédias héritées Windows](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



