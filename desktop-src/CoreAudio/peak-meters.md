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
# <a name="peak-meters"></a><span data-ttu-id="2d328-103">Compteurs de pic</span><span class="sxs-lookup"><span data-stu-id="2d328-103">Peak Meters</span></span>

<span data-ttu-id="2d328-104">Pour prendre en charge les applications Windows qui affichent des compteurs de pic, l' [API EndpointVolume](endpointvolume-api.md) comprend une interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) .</span><span class="sxs-lookup"><span data-stu-id="2d328-104">To support Windows applications that display peak meters, the [EndpointVolume API](endpointvolume-api.md) includes an [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface.</span></span> <span data-ttu-id="2d328-105">Cette interface représente un compteur de pic sur un [périphérique de point de terminaison audio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2d328-105">This interface represents a peak meter on an [audio endpoint device](audio-endpoint-devices.md).</span></span> <span data-ttu-id="2d328-106">Pour un périphérique de rendu, la valeur récupérée à partir du compteur de pic représente la valeur d’échantillon maximale rencontrée dans le flux de sortie à l’appareil au cours de la période de mesure précédente.</span><span class="sxs-lookup"><span data-stu-id="2d328-106">For a rendering device, the value retrieved from the peak meter represents the maximum sample value encountered in the output stream to the device during the preceding metering period.</span></span> <span data-ttu-id="2d328-107">Pour un appareil de capture, la valeur récupérée à partir du compteur de pic représente la valeur d’échantillon maximale rencontrée dans le flux d’entrée de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d328-107">For a capture device, the value retrieved from the peak meter represents the maximum sample value encountered in the input stream from the device.</span></span>

<span data-ttu-id="2d328-108">Les valeurs de haut-compteur obtenues à partir des méthodes de l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) sont des nombres à virgule flottante dans la plage normalisée comprise entre 0,0 et 1,0.</span><span class="sxs-lookup"><span data-stu-id="2d328-108">The peak-meter values obtained from the methods in the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface are floating-point numbers in the normalized range from 0.0 to 1.0.</span></span> <span data-ttu-id="2d328-109">Par exemple, si un flux PCM contient des exemples de 16 bits et que la valeur d’échantillon de pic au cours d’une période de mesure particulière est : 8914, la valeur absolue enregistrée par le compteur de pic est 8914, et la valeur de pic normalisée signalée par l’interface **IAudioMeterInformation** est 8914/32768 = 0,272.</span><span class="sxs-lookup"><span data-stu-id="2d328-109">For example, if a PCM stream contains 16-bit samples, and the peak sample value during a particular metering period is —8914, then the absolute value recorded by the peak meter is 8914, and the normalized peak value reported by the **IAudioMeterInformation** interface is 8914/32768 = 0.272.</span></span>

<span data-ttu-id="2d328-110">Si l’appareil de point de terminaison audio implémente le seuil de pic dans le matériel, l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) utilise le compteur de pic matériel.</span><span class="sxs-lookup"><span data-stu-id="2d328-110">If the audio endpoint device implements the peak meter in hardware, the [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface uses the hardware peak meter.</span></span> <span data-ttu-id="2d328-111">Dans le cas contraire, l’interface implémente le compteur de pic dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="2d328-111">Otherwise, the interface implements the peak meter in software.</span></span>

<span data-ttu-id="2d328-112">Si un appareil a un indicateur de pic matériel, le compteur de pic est actif à la fois en mode partagé et en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="2d328-112">If a device has a hardware peak meter, the peak meter is active both in shared mode and in exclusive mode.</span></span> <span data-ttu-id="2d328-113">Si un appareil ne dispose pas de l’indicateur de pic matériel, le compteur de pic est actif en mode partagé, mais pas en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="2d328-113">If a device lacks hardware peak meter, the peak meter is active in shared mode, but not in exclusive mode.</span></span> <span data-ttu-id="2d328-114">En mode exclusif, l’application et le matériel audio échangent directement des données audio, en ignorant le compteur de pic de logiciel (qui signale toujours une valeur maximale de 0,0).</span><span class="sxs-lookup"><span data-stu-id="2d328-114">In exclusive mode, the application and the audio hardware exchange audio data directly, bypassing the software peak meter (which always reports a peak value of 0.0).</span></span>

<span data-ttu-id="2d328-115">L’exemple de code C++ suivant est une application Windows qui affiche un compteur maximal pour le périphérique de rendu par défaut :</span><span class="sxs-lookup"><span data-stu-id="2d328-115">The following C++ code example is a Windows application that displays a peak meter for the default rendering device:</span></span>


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



<span data-ttu-id="2d328-116">Dans l’exemple de code précédent, la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) appelle la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer une instance de l’interface [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) et appelle la méthode [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour obtenir l’interface [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) du périphérique de rendu par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d328-116">In the preceding code example, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface, and it calls the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method to obtain the [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) interface of the default rendering device.</span></span> <span data-ttu-id="2d328-117">**WinMain** appelle la méthode [**IMMDevice :: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) pour obtenir l’interface [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) de l’appareil et ouvre une boîte de dialogue pour afficher un compteur maximal pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d328-117">**WinMain** calls the [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) method to obtain the device's [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) interface, and it opens a dialog box to display a peak meter for the device.</span></span> <span data-ttu-id="2d328-118">Pour plus d’informations sur **WinMain** et **CoCreateInstance**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2d328-118">For more information about **WinMain** and **CoCreateInstance**, see the Windows SDK documentation.</span></span> <span data-ttu-id="2d328-119">Pour plus d’informations sur **IMMDeviceEnumerator** et **IMMDevice**, consultez [énumération des périphériques audio](enumerating-audio-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2d328-119">For more information about **IMMDeviceEnumerator** and **IMMDevice**, see [Enumerating Audio Devices](enumerating-audio-devices.md).</span></span>

<span data-ttu-id="2d328-120">Dans l’exemple de code précédent, la fonction DlgProc affiche le compteur de pic dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2d328-120">In the preceding code example, the DlgProc function displays the peak meter in the dialog box.</span></span> <span data-ttu-id="2d328-121">Lors du traitement du \_ message WM INITDIALOG, DlgProc appelle la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) pour configurer un minuteur qui génère des messages de minuterie WM à des intervalles de \_ temps réguliers.</span><span class="sxs-lookup"><span data-stu-id="2d328-121">During processing of the WM\_INITDIALOG message, DlgProc calls the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function to set up a timer that will generate WM\_TIMER messages at regular time intervals.</span></span> <span data-ttu-id="2d328-122">Quand DlgProc reçoit un \_ message de minuteur WM, il appelle [**IAudioMeterInformation :: GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) pour obtenir la dernière lecture du compteur de pointe pour le flux.</span><span class="sxs-lookup"><span data-stu-id="2d328-122">When DlgProc receives a WM\_TIMER message, it calls [**IAudioMeterInformation::GetPeakValue**](/windows/desktop/api/Endpointvolume/nf-endpointvolume-iaudiometerinformation-getpeakvalue) to obtain the latest peak-meter reading for the stream.</span></span> <span data-ttu-id="2d328-123">DlgProc appelle ensuite la fonction DrawPeakMeter pour dessiner le compteur de pic mis à jour dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="2d328-123">DlgProc then calls the DrawPeakMeter function to draw the updated peak meter in the dialog box.</span></span> <span data-ttu-id="2d328-124">Pour plus d’informations sur **SetTimer** et les \_ messages du minuteur WM INITDIALOG et WM \_ , consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2d328-124">For more information about **SetTimer** and the WM\_INITDIALOG and WM\_TIMER messages, see the Windows SDK documentation.</span></span>

<span data-ttu-id="2d328-125">Vous pouvez facilement modifier l’exemple de code précédent pour afficher un compteur maximal pour le périphérique de capture par défaut.</span><span class="sxs-lookup"><span data-stu-id="2d328-125">You can easily modify the preceding code example to display a peak meter for the default capture device.</span></span> <span data-ttu-id="2d328-126">Dans la fonction [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) , remplacez la valeur du premier paramètre de l’appel de [**IMMDeviceEnumerator :: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) de eRender par eCapture.</span><span class="sxs-lookup"><span data-stu-id="2d328-126">In the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function, change the value of the first parameter in the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) from eRender to eCapture.</span></span>

<span data-ttu-id="2d328-127">L’exemple de code suivant est le script de ressources qui définit les contrôles qui apparaissent dans l’exemple de code précédent :</span><span class="sxs-lookup"><span data-stu-id="2d328-127">The following code example is the resource script that defines the controls that appear in the preceding code example:</span></span>


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



<span data-ttu-id="2d328-128">L’exemple de code suivant est le fichier d’en-tête de ressource qui définit les identificateurs de contrôle qui s’affichent dans les exemples de code précédents :</span><span class="sxs-lookup"><span data-stu-id="2d328-128">The following code example is the resource header file that defines the control identifiers that appear in the preceding code examples:</span></span>


```C++
// Resource.h -- Control identifiers

#define IDC_STATIC_MINVOL      1001
#define IDC_STATIC_MAXVOL      1002
#define IDC_PEAK_METER         1003
```



## <a name="related-topics"></a><span data-ttu-id="2d328-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2d328-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d328-130">Contrôles de volume</span><span class="sxs-lookup"><span data-stu-id="2d328-130">Volume Controls</span></span>](volume-controls.md)
</dt> </dl>

 

 
