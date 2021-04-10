---
description: Contrôles du volume du point de terminaison
ms.assetid: 667c3659-69ae-469d-9ae0-e32a189cbc71
title: Contrôles du volume du point de terminaison
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526403be9c600f67791650956bd7e5096f6c9afc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950676"
---
# <a name="endpoint-volume-controls"></a>Contrôles du volume du point de terminaison

Les interfaces [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)et [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) permettent aux clients de contrôler les niveaux de volume des [sessions audio](audio-sessions.md), qui sont des collections de flux audio en mode partagé. Ces interfaces ne fonctionnent pas avec les flux audio en mode exclusif.

Les applications qui gèrent des flux en mode exclusif peuvent contrôler les niveaux de volume de ces flux par le biais de l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Cette interface contrôle le niveau de volume de l' [appareil de point de terminaison audio](audio-endpoint-devices.md). Elle utilise le contrôle du volume matériel pour le périphérique de point de terminaison si le matériel audio implémente un tel contrôle. Dans le cas contraire, l’interface **IAudioEndpointVolume** implémente le contrôle du volume dans le logiciel.

Si un appareil a un contrôle de volume matériel, les modifications apportées au contrôle par le biais de l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) affectent le niveau de volume en mode partagé et en mode exclusif. Si un appareil ne dispose pas de contrôles de volume matériel et de contrôle muet, les modifications apportées au volume logiciel et les contrôles muet via cette interface affectent le niveau du volume en mode partagé, mais pas en mode exclusif. En mode exclusif, l’application et le matériel audio échangent directement des données audio, en ignorant les contrôles logiciels.

En règle générale, les applications doivent éviter d’utiliser l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) pour contrôler les niveaux de volume des flux en mode partagé. Au lieu de cela, les applications doivent utiliser l’interface [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume), [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)ou [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume) à cet effet.

Si une application affiche un contrôle de volume qui utilise l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) pour contrôler le niveau de volume d’un périphérique de point de terminaison audio, ce contrôle de volume doit mettre en miroir le contrôle du volume du point de terminaison affiché par le programme de contrôle du volume système, sndvol. Comme expliqué précédemment, le contrôle du volume du point de terminaison apparaît sur le côté gauche de la fenêtre sndvol, dans la zone de groupe intitulée **appareil**. Si l’utilisateur modifie le volume du point de terminaison d’un périphérique via le contrôle du volume dans sndvol, le contrôle du volume du point de terminaison correspondant dans l’application doit se déplacer de pair avec le contrôle dans sndvol. De même, si l’utilisateur modifie le niveau de volume via le contrôle du volume du point de terminaison dans la fenêtre d’application, le contrôle du volume correspondant dans sndvol doit se déplacer de concert avec le contrôle du volume de l’application.

Pour vous assurer que le contrôle du volume du point de terminaison dans une fenêtre d’application reflète le contrôle du volume du point de terminaison dans sndvol, l’application doit implémenter une interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) et inscrire cette interface pour recevoir des notifications. Ensuite, chaque fois que l’utilisateur modifie le niveau du volume du point de terminaison dans sndvol, l’application reçoit un appel de notification par le biais de sa méthode [**IAudioEndpointVolumeCallback :: OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) . Pendant cet appel, la méthode **OnNotify** peut mettre à jour le contrôle du volume du point de terminaison dans la fenêtre d’application pour qu’il corresponde au paramètre de contrôle indiqué dans sndvol. De même, chaque fois que l’utilisateur modifie le niveau du volume du point de terminaison par le biais du contrôle du volume dans la fenêtre d’application, sndvol reçoit une notification et met immédiatement à jour son contrôle du volume du point de terminaison pour afficher le nouveau niveau de volume.

L’exemple de code suivant est un fichier d’en-tête qui illustre une implémentation possible de l’interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) :


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



La classe CAudioEndpointVolumeCallback de l’exemple de code précédent est une implémentation de l’interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) . Comme **IAudioEndpointVolumeCallback** hérite de [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), la définition de classe contient des implémentations des méthodes **IUnknown** [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)et [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). La méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) dans la définition de classe est appelée chaque fois que l’une des méthodes suivantes modifie le niveau du volume du point de terminaison :

-   [**IAudioEndpointVolume::SetChannelVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevel)
-   [**IAudioEndpointVolume::SetChannelVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setchannelvolumelevelscalar)
-   [**IAudioEndpointVolume::SetMasterVolumeLevel**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevel)
-   [**IAudioEndpointVolume::SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar)
-   [**IAudioEndpointVolume::SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute)
-   [**IAudioEndpointVolume::VolumeStepDown**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepdown)
-   [**IAudioEndpointVolume::VolumeStepUp**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-volumestepup)

L’implémentation de la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) dans l’exemple de code précédent envoie des messages au contrôle de volume dans la fenêtre d’application pour mettre à jour le niveau de volume affiché.

Une application appelle la méthode [**IAudioEndpointVolume :: RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) pour inscrire son interface [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) afin de recevoir des notifications. Lorsque l’application ne requiert plus de notifications, elle appelle la méthode [**IAudioEndpointVolume :: UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) pour supprimer l’inscription.

L’exemple de code suivant est une application Windows qui appelle les méthodes [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) et [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) pour inscrire et annuler l’inscription de la classe CAudioEndpointVolumeCallback dans l’exemple de code précédent :


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
    if (pEnumerator != NULL)
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



Dans l’exemple de code précédent, la fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelle la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) du périphérique de rendu par défaut. **WinMain** appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour obtenir l’interface [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) de l’appareil et appelle [**RegisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-registercontrolchangenotify) pour inscrire l’application afin de recevoir des notifications de modifications du volume du point de terminaison. Ensuite, **WinMain** ouvre une boîte de dialogue pour afficher un contrôle du volume du point de terminaison pour l’appareil. La boîte de dialogue affiche également une case à cocher qui indique si l’appareil est muet. La case à cocher contrôle du volume du point de terminaison et muet de la boîte de dialogue reflète les paramètres du contrôle du volume du point de terminaison et de la case à cocher muet affichés par sndvol. Pour plus d’informations sur **WinMain** et **CoCreateInstance**, consultez la documentation SDK Windows. Pour plus d’informations sur **IMMDeviceEnumerator** et **IMMDevice**, consultez [énumération des périphériques audio](enumerating-audio-devices.md).

La procédure de boîte de dialogue, DlgProc, dans l’exemple de code précédent, gère les modifications apportées par l’utilisateur aux paramètres de volume et de silence à travers les contrôles de la boîte de dialogue. Quand DlgProc appelle [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) ou [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute), sndvol reçoit la notification de la modification et met à jour le contrôle correspondant dans sa fenêtre pour refléter le nouveau volume ou le paramètre muet. Si, au lieu d’utiliser la boîte de dialogue, l’utilisateur met à jour les paramètres de volume et de silence via les contrôles de la fenêtre sndvol, la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la classe CAudioEndpointVolumeCallback met à jour les contrôles dans la boîte de dialogue pour afficher les nouveaux paramètres.

Si l’utilisateur modifie le volume via les contrôles de la boîte de dialogue, la méthode [**OnNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolumecallback-onnotify) de la classe CAudioEndpointVolumeCallback n’envoie pas de messages pour mettre à jour les contrôles dans la boîte de dialogue. Pour ce faire, il est redondant. **OnNotify** met à jour les contrôles dans la boîte de dialogue uniquement si la modification du volume provient de sndvol ou d’une autre application. Le deuxième paramètre dans les appels de méthode [**SetMasterVolumeLevelScalar**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmastervolumelevelscalar) et [**SetMute**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-setmute) dans la fonction DlgProc est un pointeur vers un GUID de contexte d’événement que l’une ou l’autre méthode transmet à **OnNotify**. **OnNotify** vérifie la valeur du GUID de contexte d’événement pour déterminer si la boîte de dialogue est la source de la modification du volume. Pour plus d’informations sur les GUID de contexte d’événement, consultez **IAudioEndpointVolumeCallback :: OnNotify**.

Quand l’utilisateur quitte la boîte de dialogue, l’appel [**UnregisterControlChangeNotify**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudioendpointvolume-unregistercontrolchangenotify) dans l’exemple de code précédent supprime l’inscription de la classe CAudioEndpointVolumeCallback avant la fin du programme.

Vous pouvez facilement modifier l’exemple de code précédent pour afficher les contrôles de volume et de sourdine pour le périphérique de capture par défaut. Dans la fonction [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) , remplacez la valeur du premier paramètre de l’appel à la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender par eCapture.

L’exemple de code suivant est le script de ressources qui définit le volume et les contrôles muet qui apparaissent dans l’exemple de code précédent :


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



L’exemple de code suivant est le fichier d’en-tête de ressource qui définit les identificateurs de contrôle qui s’affichent dans les exemples de code précédents :


```C++
// Resource.h -- Control identifiers (epvolume)

#define IDC_SLIDER_VOLUME      1001
#define IDC_CHECK_MUTE         1002
#define IDC_STATIC_MINVOL      1003
#define IDC_STATIC_MAXVOL      1004
```



Les exemples de code précédents sont combinés pour former une application simple pour le contrôle et la surveillance du volume de point de terminaison du périphérique de rendu par défaut. Une application plus utile peut en outre notifier l’utilisateur lorsque l’état de l’appareil change. Par exemple, l’appareil peut être désactivé, débranché ou supprimé. Pour plus d’informations sur la surveillance de ces types d’événements, consultez [événements d’appareil](device-events.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de volume](volume-controls.md)
</dt> </dl>

 

 
