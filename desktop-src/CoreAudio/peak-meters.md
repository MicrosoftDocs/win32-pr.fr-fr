---
description: Compteurs de pic
ms.assetid: 02f5d1b4-ba4f-424a-897f-b113d1f7cd6b
title: Compteurs de pic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ccd2f1ce0b8fd45fbf1cb3710c878c05544f7d4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110978"
---
# <a name="peak-meters"></a>Compteurs de pic

Pour prendre en charge les applications Windows qui affichent des compteurs de pic, l' [API EndpointVolume](endpointvolume-api.md) comprend une interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) . Cette interface représente un compteur de pic sur un [périphérique de point de terminaison audio](audio-endpoint-devices.md). Pour un périphérique de rendu, la valeur récupérée à partir du compteur de pic représente la valeur d’échantillon maximale rencontrée dans le flux de sortie à l’appareil au cours de la période de mesure précédente. Pour un appareil de capture, la valeur récupérée à partir du compteur de pic représente la valeur d’échantillon maximale rencontrée dans le flux d’entrée de l’appareil.

Les valeurs de haut-compteur obtenues à partir des méthodes de l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) sont des nombres à virgule flottante dans la plage normalisée comprise entre 0,0 et 1,0. Par exemple, si un flux PCM contient des exemples de 16 bits et que la valeur d’échantillon de pic au cours d’une période de mesure particulière est : 8914, la valeur absolue enregistrée par le compteur de pic est 8914, et la valeur de pic normalisée signalée par l’interface **IAudioMeterInformation** est 8914/32768 = 0,272.

Si l’appareil de point de terminaison audio implémente le seuil de pic dans le matériel, l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) utilise le compteur de pic matériel. Dans le cas contraire, l’interface implémente le compteur de pic dans le logiciel.

Si un appareil a un indicateur de pic matériel, le compteur de pic est actif à la fois en mode partagé et en mode exclusif. Si un appareil ne dispose pas de l’indicateur de pic matériel, le compteur de pic est actif en mode partagé, mais pas en mode exclusif. En mode exclusif, l’application et le matériel audio échangent directement des données audio, en ignorant le compteur de pic de logiciel (qui signale toujours une valeur maximale de 0,0).

L’exemple de code C++ suivant est une application Windows qui affiche un compteur maximal pour le périphérique de rendu par défaut :


```C++
// Peakmeter.cpp -- WinMain and dialog box functions

#include <windows.h>
#include <mmdeviceapi.h>
#include <endpointvolume.h>
#include "resource.h"

static BOOL CALLBACK DlgProc(HWND, UINT, WPARAM, LPARAM);
static void DrawPeakMeter(HWND, float);

// Timer ID and period (in milliseconds)
#define ID_TIMER  1
#define TIMER_PERIOD  125

#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

//-----------------------------------------------------------
// WinMain -- Opens a dialog box that contains a peak meter.
//   The peak meter displays the peak sample value that plays
//   through the default rendering device.
//-----------------------------------------------------------
int APIENTRY WinMain(HINSTANCE hInstance,
                     HINSTANCE hPrevInstance,
                     LPSTR lpCmdLine,
                     int nCmdShow)
{
    HRESULT hr;
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioMeterInformation *pMeterInfo = NULL;

    if (hPrevInstance)
    {
        return 0;
    }

    CoInitialize(NULL);

    // Get enumerator for audio endpoint devices.
    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                          NULL, CLSCTX_INPROC_SERVER,
                          __uuidof(IMMDeviceEnumerator),
                          (void**)&pEnumerator);
    EXIT_ON_ERROR(hr)

    // Get peak meter for default audio-rendering device.
    hr = pEnumerator->GetDefaultAudioEndpoint(eRender, eConsole, &pDevice);
    EXIT_ON_ERROR(hr)

    hr = pDevice->Activate(__uuidof(IAudioMeterInformation),
                           CLSCTX_ALL, NULL, (void**)&pMeterInfo);
    EXIT_ON_ERROR(hr)

    DialogBoxParam(hInstance, L"PEAKMETER", NULL, (DLGPROC)DlgProc, (LPARAM)pMeterInfo);

Exit:
    if (FAILED(hr))
    {
        MessageBox(NULL, TEXT("This program requires Windows Vista."),
                   TEXT("Error termination"), MB_OK);
    }
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
    SAFE_RELEASE(pMeterInfo)
    CoUninitialize();
    return 0;
}

//-----------------------------------------------------------
// DlgProc -- Dialog box procedure
//-----------------------------------------------------------

BOOL CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    static IAudioMeterInformation *pMeterInfo = NULL;
    static HWND hPeakMeter = NULL;
    static float peak = 0;
    HRESULT hr;

    switch (message)
    {
    case WM_INITDIALOG:
        pMeterInfo = (IAudioMeterInformation*)lParam;
        SetTimer(hDlg, ID_TIMER, TIMER_PERIOD, NULL);
        hPeakMeter = GetDlgItem(hDlg, IDC_PEAK_METER);
        return TRUE;

    case WM_COMMAND:
        switch ((int)LOWORD(wParam))
        {
        case IDCANCEL:
            KillTimer(hDlg, ID_TIMER);
            EndDialog(hDlg, TRUE);
            return TRUE;
        }
        break;

    case WM_TIMER:
        switch ((int)wParam)
        {
        case ID_TIMER:
            // Update the peak meter in the dialog box.
            hr = pMeterInfo->GetPeakValue(&peak);
            if (FAILED(hr))
            {
                MessageBox(hDlg, TEXT("The program will exit."),
                           TEXT("Fatal error"), MB_OK);
                KillTimer(hDlg, ID_TIMER);
                EndDialog(hDlg, TRUE);
                return TRUE;
            }
            DrawPeakMeter(hPeakMeter, peak);
            return TRUE;
        }
        break;

    case WM_PAINT:
        // Redraw the peak meter in the dialog box.
        ValidateRect(hPeakMeter, NULL);
        DrawPeakMeter(hPeakMeter, peak);
        break;
    }
    return FALSE;
}

//-----------------------------------------------------------
// DrawPeakMeter -- Draws the peak meter in the dialog box.
//-----------------------------------------------------------

void DrawPeakMeter(HWND hPeakMeter, float peak)
{
    HDC hdc;
    RECT rect;

    GetClientRect(hPeakMeter, &rect);
    hdc = GetDC(hPeakMeter);
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DSHADOW+1));
    rect.left++;
    rect.top++;
    rect.right = rect.left +
                 max(0, (LONG)(peak*(rect.right-rect.left)-1.5));
    rect.bottom--;
    FillRect(hdc, &rect, (HBRUSH)(COLOR_3DHIGHLIGHT+1));
    ReleaseDC(hPeakMeter, hdc);
}
```



Dans l’exemple de code précédent, la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelle la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) du périphérique de rendu par défaut. **WinMain** appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour obtenir l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) de l’appareil et ouvre une boîte de dialogue pour afficher un compteur maximal pour l’appareil. Pour plus d’informations sur **WinMain** et **CoCreateInstance**, consultez la documentation SDK Windows. Pour plus d’informations sur **IMMDeviceEnumerator** et **IMMDevice**, consultez [énumération des périphériques audio](enumerating-audio-devices.md).

Dans l’exemple de code précédent, la fonction DlgProc affiche le compteur de pic dans la boîte de dialogue. Lors du traitement du \_ message WM INITDIALOG, DlgProc appelle la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) pour configurer un minuteur qui génère des messages de minuterie WM à des intervalles de \_ temps réguliers. Quand DlgProc reçoit un \_ message de minuteur WM, il appelle [**IAudioMeterInformation :: GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) pour obtenir la dernière lecture du compteur de pointe pour le flux. DlgProc appelle ensuite la fonction DrawPeakMeter pour dessiner le compteur de pic mis à jour dans la boîte de dialogue. Pour plus d’informations sur **SetTimer** et les \_ messages du minuteur WM INITDIALOG et WM \_ , consultez la documentation SDK Windows.

Vous pouvez facilement modifier l’exemple de code précédent pour afficher un compteur maximal pour le périphérique de capture par défaut. Dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , remplacez la valeur du premier paramètre de l’appel de [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender par eCapture.

L’exemple de code suivant est le script de ressources qui définit les contrôles qui apparaissent dans l’exemple de code précédent :


```C++
// Peakmeter.rc -- Resource script

#include "resource.h"
#include "windows.h"

//
// Dialog
//
PEAKMETER DIALOGEX 0, 0, 150, 34
STYLE DS_MODALFRAME | WS_CAPTION | WS_SYSMENU | DS_SETFONT
CAPTION "Peak Meter"
FONT 8, "Arial Rounded MT Bold", 400, 0, 0x0
BEGIN
    CTEXT      "",IDC_PEAK_METER,34,14,82,5
    LTEXT      "Min",IDC_STATIC_MINVOL,10,12,20,12
    RTEXT      "Max",IDC_STATIC_MAXVOL,120,12,20,12
END
```



L’exemple de code suivant est le fichier d’en-tête de ressource qui définit les identificateurs de contrôle qui s’affichent dans les exemples de code précédents :


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Contrôles de volume](volume-controls.md)
</dt> </dl>

 

 
