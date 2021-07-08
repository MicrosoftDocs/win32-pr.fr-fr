---
description: Contrôles du volume du point de terminaison
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Contrôles du volume du point de terminaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57be477a86a1de4584a7590d20d4e0199e782f10
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481884"
---
# <a name="endpoint-volume-controls"></a><span data-ttu-id="c429d-103">Contrôles du volume du point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c429d-103">Endpoint Volume Controls</span></span>

<span data-ttu-id="c429d-104">Les interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)et [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permettent aux clients de contrôler les niveaux de volume des [sessions audio](audio-sessions.md), qui sont des collections de flux audio en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="c429d-104">The [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), and [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interfaces enable clients to control the volume levels of [audio sessions](audio-sessions.md), which are collections of shared-mode audio streams.</span></span> <span data-ttu-id="c429d-105">Ces interfaces ne fonctionnent pas avec les flux audio en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="c429d-105">These interfaces do not work with exclusive-mode audio streams.</span></span>

<span data-ttu-id="c429d-106">Les applications qui gèrent des flux en mode exclusif peuvent contrôler les niveaux de volume de ces flux par le biais de l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) .</span><span class="sxs-lookup"><span data-stu-id="c429d-106">Applications that manage exclusive-mode streams can control the volume levels of those streams through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface.</span></span> <span data-ttu-id="c429d-107">Cette interface contrôle le niveau de volume de l' [appareil de point de terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="c429d-107">This interface controls the volume level of the [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="c429d-108">Elle utilise le contrôle du volume matériel pour le périphérique de point de terminaison si le matériel audio implémente un tel contrôle.</span><span class="sxs-lookup"><span data-stu-id="c429d-108">It uses the hardware volume control for the endpoint device if the audio hardware implements such a control.</span></span> <span data-ttu-id="c429d-109">Dans le cas contraire, l’interface **IAudioEndpointVolume** implémente le contrôle du volume dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="c429d-109">Otherwise, the **IAudioEndpointVolume** interface implements the volume control in software.</span></span>

<span data-ttu-id="c429d-110">Si un appareil a un contrôle de volume matériel, les modifications apportées au contrôle par le biais de l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) affectent le niveau de volume en mode partagé et en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="c429d-110">If a device has a hardware volume control, changes made to the control through the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface affect the volume level both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="c429d-111">Si un appareil ne dispose pas de contrôles de volume matériel et de contrôle muet, les modifications apportées au volume logiciel et les contrôles muet via cette interface affectent le niveau du volume en mode partagé, mais pas en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="c429d-111">If a device lacks hardware volume and mute controls, changes made to the software volume and mute controls through this interface affect the volume level in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="c429d-112">En mode exclusif, l’application et le matériel audio échangent directement des données audio, en ignorant les contrôles logiciels.</span><span class="sxs-lookup"><span data-stu-id="c429d-112">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software controls.</span></span>

<span data-ttu-id="c429d-113">En règle générale, les applications doivent éviter d’utiliser l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) pour contrôler les niveaux de volume des flux en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="c429d-113">As a general rule, applications should avoid using the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume levels of shared-mode streams.</span></span> <span data-ttu-id="c429d-114">Au lieu de cela, les applications doivent utiliser l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)ou [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) à cet effet.</span><span class="sxs-lookup"><span data-stu-id="c429d-114">Instead, applications should use the [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume), or [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) interface for that purpose.</span></span>

<span data-ttu-id="c429d-115">Si une application affiche un contrôle de volume qui utilise l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) pour contrôler le niveau de volume d’un périphérique de point de terminaison audio, ce contrôle de volume doit mettre en miroir le contrôle du volume du point de terminaison affiché par le programme de contrôle du volume système, sndvol.</span><span class="sxs-lookup"><span data-stu-id="c429d-115">If an application displays a volume control that uses the [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface to control the volume level of an audio endpoint device, that volume control should mirror the endpoint volume control displayed by the system volume-control program, Sndvol.</span></span> <span data-ttu-id="c429d-116">Comme expliqué précédemment, le contrôle du volume du point de terminaison apparaît sur le côté gauche de la fenêtre sndvol, dans la zone de groupe intitulée **appareil**.</span><span class="sxs-lookup"><span data-stu-id="c429d-116">As explained previously, the endpoint volume control appears on the left side of the Sndvol window, in the group box labeled **Device**.</span></span> <span data-ttu-id="c429d-117">Si l’utilisateur modifie le volume du point de terminaison d’un périphérique via le contrôle du volume dans sndvol, le contrôle du volume du point de terminaison correspondant dans l’application doit se déplacer de pair avec le contrôle dans sndvol.</span><span class="sxs-lookup"><span data-stu-id="c429d-117">If the user changes the endpoint volume of a device through the volume control in Sndvol, the corresponding endpoint volume control in the application should move in unison with the control in Sndvol.</span></span> <span data-ttu-id="c429d-118">De même, si l’utilisateur modifie le niveau de volume via le contrôle du volume du point de terminaison dans la fenêtre d’application, le contrôle du volume correspondant dans sndvol doit se déplacer de concert avec le contrôle du volume de l’application.</span><span class="sxs-lookup"><span data-stu-id="c429d-118">Similarly, if the user changes the volume level through the endpoint volume control in the application window, the corresponding volume control in Sndvol should move in unison with the application's volume control.</span></span>

<span data-ttu-id="c429d-119">Pour vous assurer que le contrôle du volume du point de terminaison dans une fenêtre d’application reflète le contrôle du volume du point de terminaison dans sndvol, l’application doit implémenter une interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) et inscrire cette interface pour recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="c429d-119">To ensure that the endpoint volume control in an application window mirrors the endpoint volume control in Sndvol, the application should implement an [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface and register that interface to receive notifications.</span></span> <span data-ttu-id="c429d-120">Ensuite, chaque fois que l’utilisateur modifie le niveau du volume du point de terminaison dans sndvol, l’application reçoit un appel de notification par le biais de sa méthode [**IAudioEndpointVolumeCallback :: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) .</span><span class="sxs-lookup"><span data-stu-id="c429d-120">Thereafter, each time the user changes the endpoint volume level in Sndvol, the application receives a notification call through its [**IAudioEndpointVolumeCallback::OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method.</span></span> <span data-ttu-id="c429d-121">Pendant cet appel, la méthode **OnNotify** peut mettre à jour le contrôle du volume du point de terminaison dans la fenêtre d’application pour qu’il corresponde au paramètre de contrôle indiqué dans sndvol.</span><span class="sxs-lookup"><span data-stu-id="c429d-121">During this call, the **OnNotify** method can update the endpoint volume control in the application window to match the control setting shown in Sndvol.</span></span> <span data-ttu-id="c429d-122">De même, chaque fois que l’utilisateur modifie le niveau du volume du point de terminaison par le biais du contrôle du volume dans la fenêtre d’application, sndvol reçoit une notification et met immédiatement à jour son contrôle du volume du point de terminaison pour afficher le nouveau niveau de volume.</span><span class="sxs-lookup"><span data-stu-id="c429d-122">Similarly, each time the user changes the endpoint volume level through volume control in the application window, Sndvol receives a notification and immediately updates its endpoint volume control to display the new volume level.</span></span>

<span data-ttu-id="c429d-123">L’exemple de code suivant est un fichier d’en-tête qui illustre une implémentation possible de l’interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :</span><span class="sxs-lookup"><span data-stu-id="c429d-123">The following code example is a header file that shows a possible implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface:</span></span>


```C++
// Epvolume.h -- Implementation of IAudioEndpointVolumeCallback interface

#include <windows.h>
#include <commctrl.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

// Dialog handle from dialog box procedure
extern HWND g_hDlg;

// Client's proprietary event-context GUID
extern GUID g_guidMyContext;

// Maximum volume level on trackbar
#define MAX_VOL  100

#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// Client implementation of IAudioEndpointVolumeCallback
// interface. When a method in the IAudioEndpointVolume
// interface changes the volume level or muting state of the
// endpoint device, the change initiates a call to the
// client's IAudioEndpointVolumeCallback::OnNotify method.
//-----------------------------------------------------------
class CAudioEndpointVolumeCallback : public IAudioEndpointVolumeCallback
{
    LONG _cRef;

public:
    CAudioEndpointVolumeCallback() :
        _cRef(1)
    {
    }

    ~CAudioEndpointVolumeCallback()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(REFIID riid, VOID **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioEndpointVolumeCallback) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioEndpointVolumeCallback*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Callback method for endpoint-volume-change notifications.

    HRESULT STDMETHODCALLTYPE OnNotify(PAUDIO_VOLUME_NOTIFICATION_DATA pNotify)
    {
        if (pNotify == NULL)
        {
            return E_INVALIDARG;
        }
        if (g_hDlg != NULL && pNotify->guidEventContext != g_guidMyContext)
        {
            PostMessage(GetDlgItem(g_hDlg, IDC_CHECK_MUTE), BM_SETCHECK,
                        (pNotify->bMuted) ? BST_CHECKED : BST_UNCHECKED, 0);

            PostMessage(GetDlgItem(g_hDlg, IDC_SLIDER_VOLUME),
                        TBM_SETPOS, TRUE,
                        LPARAM((UINT32)(MAX_VOL*pNotify->fMasterVolume + 0.5)));
        }
        return S_OK;
    }
};
```



<span data-ttu-id="c429d-124">La classe CAudioEndpointVolumeCallback de l’exemple de code précédent est une implémentation de l’interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .</span><span class="sxs-lookup"><span data-stu-id="c429d-124">The CAudioEndpointVolumeCallback class in the preceding code example is an implementation of the [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface.</span></span> <span data-ttu-id="c429d-125">Comme **IAudioEndpointVolumeCallback** hérite de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la définition de classe contient des implémentations des méthodes **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="c429d-125">Because **IAudioEndpointVolumeCallback** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="c429d-126">La méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) dans la définition de classe est appelée chaque fois que l’une des méthodes suivantes modifie le niveau du volume du point de terminaison :</span><span class="sxs-lookup"><span data-stu-id="c429d-126">The [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the class definition is called each time one of the following methods changes the endpoint volume level:</span></span>

-   [<span data-ttu-id="c429d-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="c429d-127">**IAudioEndpointVolume::SetChannelVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [<span data-ttu-id="c429d-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="c429d-128">**IAudioEndpointVolume::SetChannelVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [<span data-ttu-id="c429d-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span><span class="sxs-lookup"><span data-stu-id="c429d-129">**IAudioEndpointVolume::SetMasterVolumeLevel**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [<span data-ttu-id="c429d-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span><span class="sxs-lookup"><span data-stu-id="c429d-130">**IAudioEndpointVolume::SetMasterVolumeLevelScalar**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [<span data-ttu-id="c429d-131">**IAudioEndpointVolume::SetMute**</span><span class="sxs-lookup"><span data-stu-id="c429d-131">**IAudioEndpointVolume::SetMute**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [<span data-ttu-id="c429d-132">**IAudioEndpointVolume::VolumeStepDown**</span><span class="sxs-lookup"><span data-stu-id="c429d-132">**IAudioEndpointVolume::VolumeStepDown**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [<span data-ttu-id="c429d-133">**IAudioEndpointVolume::VolumeStepUp**</span><span class="sxs-lookup"><span data-stu-id="c429d-133">**IAudioEndpointVolume::VolumeStepUp**</span></span>](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

<span data-ttu-id="c429d-134">L’implémentation de la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) dans l’exemple de code précédent envoie des messages au contrôle de volume dans la fenêtre d’application pour mettre à jour le niveau de volume affiché.</span><span class="sxs-lookup"><span data-stu-id="c429d-134">The implementation of the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the preceding code example sends messages to the volume control in the application window to update the displayed volume level.</span></span>

<span data-ttu-id="c429d-135">Une application appelle la méthode [**IAudioEndpointVolume :: RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) pour inscrire son interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) afin de recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="c429d-135">An application calls the [**IAudioEndpointVolume::RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) method to register its [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) interface to receive notifications.</span></span> <span data-ttu-id="c429d-136">Lorsque l’application ne requiert plus de notifications, elle appelle la méthode [**IAudioEndpointVolume :: UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) pour supprimer l’inscription.</span><span class="sxs-lookup"><span data-stu-id="c429d-136">When the application no longer requires notifications, it calls the [**IAudioEndpointVolume::UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) method to delete the registration.</span></span>

<span data-ttu-id="c429d-137">l’exemple de code suivant est une application Windows qui appelle les méthodes [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) et [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) pour inscrire et annuler l’inscription de la classe CAudioEndpointVolumeCallback dans l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="c429d-137">The following code example is a Windows application that calls the [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) and [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) methods to register and unregister the CAudioEndpointVolumeCallback class in the preceding code example:</span></span>


```C++
// Epvolume.cpp -- WinMain and dialog box functions

#include "stdafx.h"
#include "Epvolume.h"

HWND g_hDlg = NULL;
GUID g_guidMyContext = GUID_NULL;

static IAudioEndpointVolume *g_pEndptVol = NULL;
static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define ERROR_CANCEL(hr)  \
              if (FAILED(hr)) {  \
                  MessageBox(hDlg, TEXT("The program will exit."),  \
                             TEXT("Fatal error"), MB_OK);  \
                  EndDialog(hDlg, TRUE); return TRUE; }

//-----------------------------------------------------------
// WinMain -- Registers an IAudioEndpointVolumeCallback
//   interface to monitor endpoint volume level, and opens
//   a dialog box that displays a volume control that will
//   mirror the endpoint volume control in SndVol.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr = S_OK;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    CAudioEndpointVolumeCallback EPVolEvents;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    hr = CoCreateGuid(&g_guidMyContext);
    EXIT_ON_ERROR(hr)

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioEndpointVolume),
                           CLSCTX_ALL, NULL, (void**)&g_pEndptVol);
    EXIT_ON_ERROR(hr)

    hr = g_pEndptVol->RegisterControlChangeNotify(
                     (IAudioEndpointVolumeCallback*)&EPVolEvents);
    EXIT_ON_ERROR(hr)

    InitCommonControls();
    DialogBox(hInstance, L"VOLUMECONTROL", NULL, (DLGPROC)DlgProc);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    if (g_pEndptVol != NULL)
    {
        g_pEndptVol->UnregisterControlChangeNotify(
                    (IAudioEndpointVolumeCallback*)&EPVolEvents);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(g_pEndptVol)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    HRESULT hr;
    BOOL bMute;
    float fVolume;
    int nVolume;
    int nChecked;

    switch (message)
    {
    case WM_INITDIALOG:
        g_hDlg = hDlg;
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMIN, FALSE, 0);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETRANGEMAX, FALSE, MAX_VOL);
        hr = g_pEndptVol->GetMute(&bMute);
        ERROR_CANCEL(hr)
        SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK,
                           bMute ? BST_CHECKED : BST_UNCHECKED, 0);
        hr = g_pEndptVol->GetMasterVolumeLevelScalar(&fVolume);
        ERROR_CANCEL(hr)
        nVolume = (int)(MAX_VOL*fVolume + 0.5);
        SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_SETPOS, TRUE, nVolume);
        return TRUE;

    case WM_HSCROLL:
        switch (LOWORD(wParam))
        {
        case SB_THUMBPOSITION:
        case SB_THUMBTRACK:
        case SB_LINERIGHT:
        case SB_LINELEFT:
        case SB_PAGERIGHT:
        case SB_PAGELEFT:
        case SB_RIGHT:
        case SB_LEFT:
            // The user moved the volume slider in the dialog box.
            SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_SETCHECK, BST_UNCHECKED, 0);
            hr = g_pEndptVol->SetMute(FALSE, &g_guidMyContext);
            ERROR_CANCEL(hr)
            nVolume = SendDlgItemMessage(hDlg, IDC_SLIDER_VOLUME, TBM_GETPOS, 0, 0);
            fVolume = (float)nVolume/MAX_VOL;
            hr = g_pEndptVol->SetMasterVolumeLevelScalar(fVolume, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        }
        break;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDC_CHECK_MUTE:
            // The user selected the Mute check box in the dialog box.
            nChecked = SendDlgItemMessage(hDlg, IDC_CHECK_MUTE, BM_GETCHECK, 0, 0);
            bMute = (BST_CHECKED == nChecked);
            hr = g_pEndptVol->SetMute(bMute, &g_guidMyContext);
            ERROR_CANCEL(hr)
            return TRUE;
        case IDCANCEL:
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;
    }
    return FALSE;
}
```



<span data-ttu-id="c429d-138">Dans l’exemple de code précédent, la fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelle la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) du périphérique de rendu par défaut.</span><span class="sxs-lookup"><span data-stu-id="c429d-138">In the preceding code example, the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="c429d-139">**WinMain** appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour obtenir l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de l’appareil et appelle [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) pour inscrire l’application afin de recevoir des notifications de modifications du volume du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="c429d-139">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) interface, and it calls [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) to register the application to receive notifications of endpoint volume changes.</span></span> <span data-ttu-id="c429d-140">Ensuite, **WinMain** ouvre une boîte de dialogue pour afficher un contrôle du volume du point de terminaison pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c429d-140">Next, **WinMain** opens a dialog box to display an endpoint volume control for the device.</span></span> <span data-ttu-id="c429d-141">La boîte de dialogue affiche également une case à cocher qui indique si l’appareil est muet.</span><span class="sxs-lookup"><span data-stu-id="c429d-141">The dialog box also displays a check box that indicates whether the device is muted.</span></span> <span data-ttu-id="c429d-142">La case à cocher contrôle du volume du point de terminaison et muet de la boîte de dialogue reflète les paramètres du contrôle du volume du point de terminaison et de la case à cocher muet affichés par sndvol.</span><span class="sxs-lookup"><span data-stu-id="c429d-142">The endpoint volume control and mute check box in the dialog box mirror the settings of the endpoint volume control and mute check box displayed by Sndvol.</span></span> <span data-ttu-id="c429d-143">pour plus d’informations sur **WinMain** et **CoCreateInstance**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c429d-143">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="c429d-144">Pour plus d’informations sur **IMMDeviceEnumerator** et **IMMDevice**, consultez [énumération des périphériques audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="c429d-144">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="c429d-145">La procédure de boîte de dialogue, DlgProc, dans l’exemple de code précédent, gère les modifications apportées par l’utilisateur aux paramètres de volume et de silence à travers les contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c429d-145">The dialog box procedure, DlgProc, in the preceding code example, handles the changes that the user makes to the volume and mute settings through the controls in the dialog box.</span></span> <span data-ttu-id="c429d-146">Quand DlgProc appelle [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) ou [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), sndvol reçoit la notification de la modification et met à jour le contrôle correspondant dans sa fenêtre pour refléter le nouveau volume ou le paramètre muet.</span><span class="sxs-lookup"><span data-stu-id="c429d-146">When DlgProc calls [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) or [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), Sndvol receives notification of the change and updates the corresponding control in its window to reflect the new volume or mute setting.</span></span> <span data-ttu-id="c429d-147">Si, au lieu d’utiliser la boîte de dialogue, l’utilisateur met à jour les paramètres de volume et de silence via les contrôles de la fenêtre sndvol, la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la classe CAudioEndpointVolumeCallback met à jour les contrôles dans la boîte de dialogue pour afficher les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="c429d-147">If, instead of using the dialog box, the user updates the volume and mute settings through the controls in the Sndvol window, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class updates the controls in the dialog box to display the new settings.</span></span>

<span data-ttu-id="c429d-148">Si l’utilisateur modifie le volume via les contrôles de la boîte de dialogue, la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la classe CAudioEndpointVolumeCallback n’envoie pas de messages pour mettre à jour les contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c429d-148">If the user changes the volume through the controls in the dialog box, the [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) method in the CAudioEndpointVolumeCallback class does not send messages to update the controls in the dialog box.</span></span> <span data-ttu-id="c429d-149">Pour ce faire, il est redondant.</span><span class="sxs-lookup"><span data-stu-id="c429d-149">To do so would be redundant.</span></span> <span data-ttu-id="c429d-150">**OnNotify** met à jour les contrôles dans la boîte de dialogue uniquement si la modification du volume provient de sndvol ou d’une autre application.</span><span class="sxs-lookup"><span data-stu-id="c429d-150">**OnNotify** updates the controls in the dialog box only if the volume change originated in Sndvol or in some other application.</span></span> <span data-ttu-id="c429d-151">Le deuxième paramètre dans les appels de méthode [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) et [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) dans la fonction DlgProc est un pointeur vers un GUID de contexte d’événement que l’une ou l’autre méthode transmet à **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="c429d-151">The second parameter in the [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) and [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) method calls in the DlgProc function is a pointer to an event-context GUID that either method passes to **OnNotify**.</span></span> <span data-ttu-id="c429d-152">**OnNotify** vérifie la valeur du GUID de contexte d’événement pour déterminer si la boîte de dialogue est la source de la modification du volume.</span><span class="sxs-lookup"><span data-stu-id="c429d-152">**OnNotify** checks the value of the event-context GUID to determine whether the dialog box is the source of the volume change.</span></span> <span data-ttu-id="c429d-153">Pour plus d’informations sur les GUID de contexte d’événement, consultez **IAudioEndpointVolumeCallback :: OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="c429d-153">For more information about event-context GUIDs, see **IAudioEndpointVolumeCallback::OnNotify**.</span></span>

<span data-ttu-id="c429d-154">Quand l’utilisateur quitte la boîte de dialogue, l’appel [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) dans l’exemple de code précédent supprime l’inscription de la classe CAudioEndpointVolumeCallback avant la fin du programme.</span><span class="sxs-lookup"><span data-stu-id="c429d-154">When the user exits the dialog box, the [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) call in the preceding code example deletes the registration of the CAudioEndpointVolumeCallback class before the program terminates.</span></span>

<span data-ttu-id="c429d-155">Vous pouvez facilement modifier l’exemple de code précédent pour afficher les contrôles de volume et de sourdine pour le périphérique de capture par défaut.</span><span class="sxs-lookup"><span data-stu-id="c429d-155">You can easily modify the preceding code example to display volume and mute controls for the default capture device.</span></span> <span data-ttu-id="c429d-156">Dans la fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) , remplacez la valeur du premier paramètre de l’appel à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender par eCapture.</span><span class="sxs-lookup"><span data-stu-id="c429d-156">In the [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method from eRender to eCapture.</span></span>

<span data-ttu-id="c429d-157">L’exemple de code suivant est le script de ressources qui définit le volume et les contrôles muet qui apparaissent dans l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="c429d-157">The following code example is the resource script that defines the volume and mute controls that appear in the preceding code example:</span></span>


```C++
// Epvolume.rc -- Resource script

#include "resource.h"
#include "windows.h"
#include "commctrl.h"

//
// Dialog box
//
VOLUMECONTROL DIALOGEX 0, 0, 160, 60
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Audio Endpoint Volume"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    LTEXT      "Min",IDC_STATIC_MINVOL,10,10,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,130,10,20,12
    CONTROL    "",IDC_SLIDER_VOLUME,"msctls_trackbar32",
               TBS_BOTH | TBS_NOTICKS | WS_TABSTOP,10,20,140,12
    CONTROL    "Mute",IDC_CHECK_MUTE,"Button",
               BS_AUTOCHECKBOX | WS_TABSTOP,20,40,70,12
END
```



<span data-ttu-id="c429d-158">L’exemple de code suivant est le fichier d’en-tête de ressource qui définit les identificateurs de contrôle qui s’affichent dans les exemples de code précédents :</span><span class="sxs-lookup"><span data-stu-id="c429d-158">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



<span data-ttu-id="c429d-159">Les exemples de code précédents sont combinés pour former une application simple pour le contrôle et la surveillance du volume de point de terminaison du périphérique de rendu par défaut.</span><span class="sxs-lookup"><span data-stu-id="c429d-159">The preceding code examples combine to form a simple application for controlling and monitoring the endpoint volume of the default rendering device.</span></span> <span data-ttu-id="c429d-160">Une application plus utile peut en outre notifier l’utilisateur lorsque l’état de l’appareil change.</span><span class="sxs-lookup"><span data-stu-id="c429d-160">A more useful application might additionally notify the user when the status of the device changes.</span></span> <span data-ttu-id="c429d-161">Par exemple, l’appareil peut être désactivé, débranché ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="c429d-161">For example, the device might be disabled, unplugged, or removed.</span></span> <span data-ttu-id="c429d-162">Pour plus d’informations sur la surveillance de ces types d’événements, consultez [événements d’appareil](device-events.md).</span><span class="sxs-lookup"><span data-stu-id="c429d-162">For more information about monitoring these types of events, see [Device Events](device-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c429d-163">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c429d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c429d-164">Contrôles de volume</span><span class="sxs-lookup"><span data-stu-id="c429d-164">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
