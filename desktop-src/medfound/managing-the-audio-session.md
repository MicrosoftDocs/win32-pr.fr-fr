---
description: Cette rubrique explique comment contrôler le volume audio lors de l’utilisation de MFPlay pour la lecture audio/vidéo.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Gestion de la session audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318038"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="1d505-103">Gestion de la session audio</span><span class="sxs-lookup"><span data-stu-id="1d505-103">Managing the Audio Session</span></span>

<span data-ttu-id="1d505-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="1d505-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1d505-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1d505-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1d505-106">\]</span><span class="sxs-lookup"><span data-stu-id="1d505-106">\]</span></span>

<span data-ttu-id="1d505-107">Cette rubrique explique comment contrôler le volume audio lors de l’utilisation de MFPlay pour la lecture audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="1d505-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="1d505-108">MFPlay fournit les méthodes suivantes pour contrôler le volume audio pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="1d505-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="1d505-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="1d505-109">Method</span></span>                                                            | <span data-ttu-id="1d505-110">Description</span><span class="sxs-lookup"><span data-stu-id="1d505-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="1d505-111">**IMFPMediaPlayer::SetBalance**</span><span class="sxs-lookup"><span data-stu-id="1d505-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="1d505-112">Définit l’équilibre entre les canaux gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="1d505-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="1d505-113">**IMFPMediaPlayer::SetMute**</span><span class="sxs-lookup"><span data-stu-id="1d505-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="1d505-114">Active ou désactive le son.</span><span class="sxs-lookup"><span data-stu-id="1d505-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="1d505-115">**IMFPMediaPlayer::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="1d505-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="1d505-116">Définit le niveau du volume.</span><span class="sxs-lookup"><span data-stu-id="1d505-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="1d505-117">Pour comprendre le comportement de ces méthodes, vous devez connaître la terminologie de l’API de session audio Windows (WASAPI), qui implémente les fonctionnalités audio de bas niveau utilisées par MFPlay.</span><span class="sxs-lookup"><span data-stu-id="1d505-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="1d505-118">Dans WASAPI, chaque flux audio appartient à une seule *session audio*, qui est un groupe de flux audio associés.</span><span class="sxs-lookup"><span data-stu-id="1d505-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="1d505-119">En règle générale, une application gère une seule session audio, bien que les applications puissent créer plusieurs sessions.</span><span class="sxs-lookup"><span data-stu-id="1d505-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="1d505-120">Le programme de contrôle du volume système (sndvol) affiche un contrôle du volume pour chaque session audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="1d505-121">Par le biais de sndvol, un utilisateur peut ajuster le volume d’une session audio en dehors de l’application.</span><span class="sxs-lookup"><span data-stu-id="1d505-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="1d505-122">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="1d505-122">The following image illustrates this process.</span></span>

![Diagramme montrant les flux audio passant par le contrôle du volume aux orateurs ; application et sndvol pointer vers le contrôle du volume](images/audio-session.gif)

<span data-ttu-id="1d505-124">Dans MFPlay, un élément multimédia peut avoir un ou plusieurs flux audio actifs (en général, un seul).</span><span class="sxs-lookup"><span data-stu-id="1d505-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="1d505-125">En interne, MFPlay utilise le [convertisseur audio de streaming](streaming-audio-renderer.md) (SAR) pour restituer les flux audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="1d505-126">Sauf si vous le configurez dans le cas contraire, le SAR rejoint la session audio par défaut de l’application.</span><span class="sxs-lookup"><span data-stu-id="1d505-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="1d505-127">Les méthodes audio MFPlay contrôlent uniquement les flux qui appartiennent à l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="1d505-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="1d505-128">Ils n’affectent pas le volume de tous les autres flux appartenant à la même session audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="1d505-129">En termes de WASAPI, les méthodes MFPlay contrôlent les niveaux de volume *par canal* , et non le niveau de volume principal.</span><span class="sxs-lookup"><span data-stu-id="1d505-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="1d505-130">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="1d505-130">The following image illustrates this process.</span></span>

![diagramme similaire au précédent, mais le deuxième flux démarre au niveau de l’élément multimédia, et l’application pointe vers le deuxième flux et le contrôle du volume](images/audio-session02.gif)

<span data-ttu-id="1d505-132">Il est important de comprendre certaines implications de cette fonctionnalité de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="1d505-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="1d505-133">Tout d’abord, une application peut ajuster le volume de lecture sans affecter les autres flux audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="1d505-134">Vous pouvez utiliser cette fonctionnalité si MFPlay pour implémenter le fondu croisé audio, en créant deux instances de l’objet MFPlay et en ajustant le volume séparément.</span><span class="sxs-lookup"><span data-stu-id="1d505-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="1d505-135">Si vous utilisez les méthodes MFPlay pour modifier l’état du volume ou du silence, les modifications n’apparaissent pas dans sndvol.</span><span class="sxs-lookup"><span data-stu-id="1d505-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="1d505-136">Par exemple, vous pouvez appeler [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) pour désactiver le son, mais sndvol n’affichera pas la session comme étant muette.</span><span class="sxs-lookup"><span data-stu-id="1d505-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="1d505-137">À l’inverse, si SndVol est utilisé pour ajuster le volume de session, les modifications ne sont pas reflétées dans les valeurs retournées par [**IMFPMediaPlayer :: GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) ou [**IMFPMediaPlayer :: GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span><span class="sxs-lookup"><span data-stu-id="1d505-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="1d505-138">Pour chaque instance de l’objet MFPlay Player, le niveau de volume effectif est égal à *fPlayerVolume* × *FSessionVolume*, où *fPlayerVolume* est la valeur retournée par [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), et *fSessionVolume* est le volume maître de la session.</span><span class="sxs-lookup"><span data-stu-id="1d505-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="1d505-139">Pour les scénarios de lecture simples, il peut être préférable d’utiliser le WASAPI pour contrôler le volume audio de la session entière, plutôt que d’utiliser les méthodes MFPlay.</span><span class="sxs-lookup"><span data-stu-id="1d505-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="1d505-140">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="1d505-140">Example Code</span></span>

<span data-ttu-id="1d505-141">Ce qui suit est une classe C++ qui gère les tâches de base dans WASAPI :</span><span class="sxs-lookup"><span data-stu-id="1d505-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="1d505-142">Contrôle de l’état du volume et du silence pour la session.</span><span class="sxs-lookup"><span data-stu-id="1d505-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="1d505-143">Obtention de notifications chaque fois que l’état du volume ou du silence change.</span><span class="sxs-lookup"><span data-stu-id="1d505-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="1d505-144">Déclaration de classe</span><span class="sxs-lookup"><span data-stu-id="1d505-144">Class Declaration</span></span>

<span data-ttu-id="1d505-145">La `CAudioSessionVolume` déclaration de classe implémente l’interface [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , qui est l’interface de rappel pour les événements de session audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="1d505-146">Lorsque l' `CAudioSessionVolume` objet reçoit un événement de session audio, il publie un message de fenêtre privée dans l’application.</span><span class="sxs-lookup"><span data-stu-id="1d505-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="1d505-147">Le handle de fenêtre et le message de fenêtre sont fournis en tant que paramètres à la `CAudioSessionVolume::CreateInstance` méthode statique.</span><span class="sxs-lookup"><span data-stu-id="1d505-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="1d505-148">Obtention des pointeurs d’interface WASAPI</span><span class="sxs-lookup"><span data-stu-id="1d505-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="1d505-149">`CAudioSessionVolume` utilise deux interfaces WASAPI principales :</span><span class="sxs-lookup"><span data-stu-id="1d505-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="1d505-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) gère la session audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="1d505-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) contrôle le niveau de volume et l’état de silence de la session.</span><span class="sxs-lookup"><span data-stu-id="1d505-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="1d505-152">Pour accéder à ces interfaces, vous devez énumérer le point de terminaison audio utilisé par le SAR.</span><span class="sxs-lookup"><span data-stu-id="1d505-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="1d505-153">Un *point de terminaison audio* est un périphérique matériel qui capture ou consomme des données audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="1d505-154">Pour la lecture audio, un point de terminaison est simplement un conférencier ou une autre sortie audio.</span><span class="sxs-lookup"><span data-stu-id="1d505-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="1d505-155">Par défaut, le SAR utilise le point de terminaison par défaut pour le rôle d’appareil **eConsole** .</span><span class="sxs-lookup"><span data-stu-id="1d505-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="1d505-156">Un *rôle d’appareil* est un rôle affecté à un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="1d505-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="1d505-157">Les rôles d’appareil sont spécifiés par l’énumération [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , qui est documenté dans les [API audio principales](../coreaudio/core-audio-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="1d505-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="1d505-158">Le code suivant illustre l’énumération du point de terminaison et l’obtention des interfaces WASAPI.</span><span class="sxs-lookup"><span data-stu-id="1d505-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="1d505-159">Contrôle du volume</span><span class="sxs-lookup"><span data-stu-id="1d505-159">Controlling the Volume</span></span>

<span data-ttu-id="1d505-160">Les `CAudioSessionVolume` méthodes qui contrôlent le volume audio appellent les méthodes [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) équivalentes.</span><span class="sxs-lookup"><span data-stu-id="1d505-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="1d505-161">Par exemple, `CAudioSessionVolume::SetVolume` appelle [**ISimpleAudioVolume :: SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="1d505-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="1d505-162">Code CAudioSessionVolume complet</span><span class="sxs-lookup"><span data-stu-id="1d505-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="1d505-163">Voici la liste complète des méthodes de la `CAudioSessionVolume` classe.</span><span class="sxs-lookup"><span data-stu-id="1d505-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="1d505-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d505-164">Requirements</span></span>

<span data-ttu-id="1d505-165">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1d505-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d505-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d505-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d505-167">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="1d505-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
