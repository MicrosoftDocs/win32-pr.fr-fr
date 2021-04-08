---
description: Ce didacticiel présente une application complète qui lit des vidéos à l’aide de MFPlay.
ms.assetid: f72a7c1f-b059-474c-96f2-8fad3b1f7035
title: 'Didacticiel MFPlay : lecture vidéo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30bbadae22e72799c64a42d09b6eed904b56a60d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755293"
---
# <a name="mfplay-tutorial-video-playback"></a>Didacticiel MFPlay : lecture vidéo

\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. \]

Ce didacticiel présente une application complète qui lit des vidéos à l’aide de MFPlay. Il est basé sur l’exemple du kit de développement logiciel (SDK) [SimplePlay](simpleplay-sample.md) .

Ce didacticiel contient les sections suivantes :

-   [Configuration requise](#requirements)
-   [Fichiers d’en-tête et de bibliothèque](#header-and-library-files)
-   [Variables globales](#global-variables)
-   [Déclarer la classe de rappel](#declare-the-callback-class)
-   [Déclarer la fonction SafeRelease](#declare-the-saferelease-function)
-   [Ouvrir un fichier multimédia](#open-a-media-file)
-   [Gestionnaires de messages de fenêtre](#window-message-handlers)
-   [Implémenter la méthode de rappel](#implement-the-callback-method)
-   [Implémenter WinMain](#implement-winmain)
-   [Rubriques connexes](#related-topics)

Pour obtenir une présentation plus détaillée de l’API MFPlay, consultez [prise en main avec MFPlay](getting-started-with-mfplay.md).

## <a name="requirements"></a>Configuration requise

MFPlay requiert Windows 7.

## <a name="header-and-library-files"></a>Fichiers d’en-tête et de bibliothèque

Incluez les fichiers d’en-tête suivants dans votre projet :


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <new>
#include <windows.h>
#include <windowsx.h>
#include <mfplay.h>
#include <mferror.h>
#include <shobjidl.h>   // defines IFileOpenDialog
#include <strsafe.h>
#include <Shlwapi.h>
```



Lien vers les bibliothèques de code suivantes :

-   mfplay. lib
-   Shlwapi. lib

## <a name="global-variables"></a>Variables globales

Déclarez les variables globales suivantes :


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



Ces variables sont utilisées comme suit :

<dl> <dt>

<span id="g_hwnd"></span><span id="G_HWND"></span>*HWND de g \_*
</dt> <dd>

Handle de la fenêtre d’application.

</dd> <dt>

<span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*\_bVideo g*
</dt> <dd>

Valeur booléenne qui effectue le suivi de la durée de la vidéo.

</dd> <dt>

<span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*\_pPlayer g*
</dt> <dd>

Pointeur vers l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) . Cette interface est utilisée pour contrôler la lecture.

</dd> <dt>

<span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*\_pCallback g*
</dt> <dd>

Pointeur vers l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . L’application implémente cette interface de rappel pour recevoir des notifications de l’objet Player.

</dd> </dl>

## <a name="declare-the-callback-class"></a>Déclarer la classe de rappel

Pour recevoir des notifications d’événements à partir de l’objet Player, l’application doit implémenter l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) . Le code suivant déclare une classe qui implémente l’interface. La seule variable membre est *m \_ cref*, qui stocke le nombre de références.

Les méthodes **IUnknown** sont implémentées en ligne. L’implémentation de la méthode [**IMFPMediaPlayerCallback :: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) est indiquée plus tard ; consultez [implémenter la méthode de rappel](#implement-the-callback-method).


```C++
// Implements the callback interface for MFPlay events.

class MediaPlayerCallback : public IMFPMediaPlayerCallback
{
    long m_cRef; // Reference count

public:

    MediaPlayerCallback() : m_cRef(1)
    {
    }

    IFACEMETHODIMP QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] =
        {
            QITABENT(MediaPlayerCallback, IMFPMediaPlayerCallback),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    IFACEMETHODIMP_(ULONG) AddRef()
    {
        return InterlockedIncrement(&m_cRef);
    }

    IFACEMETHODIMP_(ULONG) Release()
    {
        ULONG count = InterlockedDecrement(&m_cRef);
        if (count == 0)
        {
            delete this;
            return 0;
        }
        return count;
    }

    // IMFPMediaPlayerCallback methods
    IFACEMETHODIMP_(void) OnMediaPlayerEvent(MFP_EVENT_HEADER *pEventHeader);
};
```



## <a name="declare-the-saferelease-function"></a>Déclarer la fonction SafeRelease

Tout au long de ce didacticiel, la fonction [SafeRelease](saferelease.md) est utilisée pour libérer des pointeurs d’interface :


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="open-a-media-file"></a>Ouvrir un fichier multimédia

La `PlayMediaFile` fonction ouvre un fichier multimédia, comme suit :

1.  Si *g \_ pPlayer* a la **valeur null**, la fonction appelle [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) pour créer une nouvelle instance de l’objet Media Player. Les paramètres d’entrée de **MFPCreateMediaPlayer** incluent un pointeur vers l’interface de rappel et un handle vers la fenêtre vidéo.
2.  Pour ouvrir le fichier multimédia, la fonction appelle [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), en passant l’URL du fichier. Cette méthode se termine de façon asynchrone. Une fois l’opération terminée, la méthode [**IMFPMediaPlayerCallback :: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) de l’application est appelée.


```C++
HRESULT PlayMediaFile(HWND hwnd, PCWSTR pszURL)
{
    HRESULT hr = S_OK;

    // Create the MFPlayer object.
    if (g_pPlayer == NULL)
    {
        g_pPlayerCB = new (std::nothrow) MediaPlayerCallback();

        if (g_pPlayerCB == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFPCreateMediaPlayer(
            NULL,
            FALSE,          // Start playback automatically?
            0,              // Flags
            g_pPlayerCB,    // Callback pointer
            hwnd,           // Video window
            &g_pPlayer
            );
    }

    // Create a new media item for this URL.

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromURL(pszURL, FALSE, 0, NULL);
    }

    // The CreateMediaItemFromURL method completes asynchronously.
    // The application will receive an MFP_EVENT_TYPE_MEDIAITEM_CREATED
    // event. See MediaPlayerCallback::OnMediaPlayerEvent().

    return hr;
}
```



La `OnFileOpen` fonction affiche la boîte de dialogue de fichier commune, qui permet à l’utilisateur de sélectionner un fichier pour la lecture. L’interface **IFileOpenDialog** est utilisée pour afficher la boîte de dialogue de fichier commune. Cette interface fait partie des API de l’interpréteur de commandes Windows. Il a été introduit dans Windows Vista en remplacement de l’ancienne fonction **GetOpenFileName** . Une fois que l’utilisateur a sélectionné un fichier, `OnFileOpen` appelle `PlayMediaFile` pour démarrer la lecture.


```C++
void OnFileOpen(HWND hwnd)
{
    IFileOpenDialog *pFileOpen = NULL;
    IShellItem *pItem = NULL;
    PWSTR pwszFilePath = NULL;

    // Create the FileOpenDialog object.
    HRESULT hr = CoCreateInstance(__uuidof(FileOpenDialog), NULL,
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pFileOpen));
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->SetTitle(L"Select a File to Play");
    }

    // Show the file-open dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->Show(hwnd);
    }

    if (hr == HRESULT_FROM_WIN32(ERROR_CANCELLED))
    {
        // User canceled.
        SafeRelease(&pFileOpen);
        return;
    }

    // Get the file name from the dialog.
    if (SUCCEEDED(hr))
    {
        hr = pFileOpen->GetResult(&pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pItem->GetDisplayName(SIGDN_URL, &pwszFilePath);
    }

    // Open the media file.
    if (SUCCEEDED(hr))
    {
        hr = PlayMediaFile(hwnd, pwszFilePath);
    }

    if (FAILED(hr))
    {
        ShowErrorMessage(L"Could not open file.", hr);
    }

    CoTaskMemFree(pwszFilePath);

    SafeRelease(&pItem);
    SafeRelease(&pFileOpen);
}
```



## <a name="window-message-handlers"></a>Gestionnaires de messages de fenêtre

Ensuite, déclarez les gestionnaires de messages pour les messages de fenêtre suivants :

-   **\_peinture WM**
-   **taille du WM \_**
-   **\_Fermer WM**

Pour le message **WM \_ Paint** , vous devez suivre si la vidéo est en cours de diffusion. Si c’est le cas, appelez la méthode [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) . Cette méthode fait en sorte que l’objet Player redessine la trame vidéo la plus récente.

S’il n’y a pas de vidéo, l’application est chargée de peindre la fenêtre. Pour ce didacticiel, l’application appelle simplement la fonction GDI **fillRect** pour remplir toute la zone cliente.


```C++
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_bHasVideo)
    {
        // Playback has started and there is video.

        // Do not draw the window background, because the video
        // frame fills the entire client area.

        g_pPlayer->UpdateVideo();
    }
    else
    {
        // There is no video stream, or playback has not started.
        // Paint the entire client area.

        FillRect(hdc, &ps.rcPaint, (HBRUSH) (COLOR_WINDOW+1));
    }

    EndPaint(hwnd, &ps);
}
```



Pour le message de **\_ taille WM** , appelez [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo). Cette méthode fait en sorte que l’objet Player réajuste la vidéo pour qu’elle corresponde à la taille actuelle de la fenêtre. Notez que **UpdateVideo** est utilisé à la fois pour la **\_ peinture WM** et pour la **\_ taille WM**.


```C++
void OnSize(HWND /*hwnd*/, UINT state, int /*cx*/, int /*cy*/)
{
    if (state == SIZE_RESTORED)
    {
        if (g_pPlayer)
        {
            // Resize the video.
            g_pPlayer->UpdateVideo();
        }
    }
}
```



Pour le message **WM \_ Close** , libérez les pointeurs [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) et [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a>Implémenter la méthode de rappel

L’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) définit une méthode unique, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent). Cette méthode avertit l’application chaque fois qu’un événement se produit pendant la lecture. La méthode accepte un paramètre, un pointeur vers une structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) . Le membre **eEventType** de la structure spécifie l’événement qui s’est produit.

La structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) peut être suivie de données supplémentaires. Pour chaque type d’événement, une macro est définie et effectue un cast du pointeur d' **\_ \_ en-tête d’événement MFP** vers une structure spécifique à un événement. (Voir [**\_ \_ type d’événement MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)

Pour ce didacticiel, deux événements sont significatifs :



| Événement                                    | Description                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| **\_type d’événement MFP \_ \_ MEDIAITEM \_ créé** | Envoyé lorsque le [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) est terminé. |
| **\_type d’événement MFP \_ \_ MEDIAITEM \_ Set**     | Envoyé lorsque [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) est terminé.                         |



 

Le code suivant montre comment effectuer un cast du pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) vers la structure spécifique à l’événement.


```C++
void MediaPlayerCallback::OnMediaPlayerEvent(MFP_EVENT_HEADER * pEventHeader)
{
    if (FAILED(pEventHeader->hrEvent))
    {
        ShowErrorMessage(L"Playback error", pEventHeader->hrEvent);
        return;
    }

    switch (pEventHeader->eEventType)
    {
    case MFP_EVENT_TYPE_MEDIAITEM_CREATED:
        OnMediaItemCreated(MFP_GET_MEDIAITEM_CREATED_EVENT(pEventHeader));
        break;

    case MFP_EVENT_TYPE_MEDIAITEM_SET:
        OnMediaItemSet(MFP_GET_MEDIAITEM_SET_EVENT(pEventHeader));
        break;
    }
}
```



L’événement de **\_ type d’événement MFP \_ \_ MEDIAITEM \_ créé** informe l’application que la méthode [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) est terminée. La structure d’événement contient un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , qui représente l’élément multimédia créé à partir de l’URL. Pour effectuer la mise en file d’attente de l’élément pour la lecture, transmettez ce pointeur à la méthode [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    // The media item was created successfully.

    if (g_pPlayer)
    {
        BOOL    bHasVideo = FALSE;
        BOOL    bIsSelected = FALSE;

        // Check if the media item contains video.
        HRESULT hr = pEvent->pMediaItem->HasVideo(&bHasVideo, &bIsSelected);
        if (SUCCEEDED(hr))
        {
            g_bHasVideo = bHasVideo && bIsSelected;

            // Set the media item on the player. This method completes
            // asynchronously.
            hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
        }

        if (FAILED(hr))
        {
            ShowErrorMessage(L"Error playing this file.", hr);
        }
   }
}
```



Le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ Set** Event informe l’application que [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) est terminée. Appeler [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour démarrer la lecture :


```C++
void OnMediaItemSet(MFP_MEDIAITEM_SET_EVENT * /*pEvent*/)
{
    HRESULT hr = g_pPlayer->Play();
    if (FAILED(hr))
    {
        ShowErrorMessage(L"IMFPMediaPlayer::Play failed.", hr);
    }
}
```



## <a name="implement-winmain"></a>Implémenter WinMain

Dans le reste de ce didacticiel, il n’y a aucun appel à Media Foundation API. Le code suivant illustre la procédure de fenêtre :


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        HANDLE_MSG(hwnd, WM_CLOSE,   OnClose);
        HANDLE_MSG(hwnd, WM_PAINT,   OnPaint);
        HANDLE_MSG(hwnd, WM_COMMAND, OnCommand);
        HANDLE_MSG(hwnd, WM_SIZE,    OnSize);

    case WM_ERASEBKGND:
        return 1;

    default:
        return DefWindowProc(hwnd, uMsg, wParam, lParam);
    }
}
```



La `InitializeWindow` fonction enregistre la classe de fenêtre de l’application et crée la fenêtre.


```C++
BOOL InitializeWindow(HWND *pHwnd)
{
    const wchar_t CLASS_NAME[]  = L"MFPlay Window Class";
    const wchar_t WINDOW_NAME[] = L"MFPlay Sample Application";

    WNDCLASS wc = {};

    wc.lpfnWndProc   = WindowProc;
    wc.hInstance     = GetModuleHandle(NULL);
    wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wc.lpszClassName = CLASS_NAME;
    wc.lpszMenuName  = MAKEINTRESOURCE(IDR_MENU1);

    RegisterClass(&wc);

    HWND hwnd = CreateWindow(
        CLASS_NAME, WINDOW_NAME, WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT,
        NULL, NULL, GetModuleHandle(NULL), NULL);

    if (!hwnd)
    {
        return FALSE;
    }

    ShowWindow(hwnd, SW_SHOWDEFAULT);
    UpdateWindow(hwnd);

    *pHwnd = hwnd;

    return TRUE;
}
```



Enfin, implémentez le point d’entrée de l’application :


```C++
int WINAPI wWinMain(HINSTANCE, HINSTANCE, PWSTR, int)
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    HRESULT hr = CoInitializeEx(NULL,
        COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        return 0;
    }

    HWND hwnd = NULL;
    if (InitializeWindow(&hwnd))
    {
        // Message loop
        MSG msg = {};
        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }

        DestroyWindow(hwnd);
    }
    CoUninitialize();

    return 0;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de MFPlay pour la lecture audio/vidéo](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



