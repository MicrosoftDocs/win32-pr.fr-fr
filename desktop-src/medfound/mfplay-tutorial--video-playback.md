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
# <a name="mfplay-tutorial-video-playback"></a><span data-ttu-id="8c582-103">Didacticiel MFPlay : lecture vidéo</span><span class="sxs-lookup"><span data-stu-id="8c582-103">MFPlay Tutorial: Video Playback</span></span>

<span data-ttu-id="8c582-104">\[MFPlay peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="8c582-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c582-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8c582-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8c582-106">\]</span><span class="sxs-lookup"><span data-stu-id="8c582-106">\]</span></span>

<span data-ttu-id="8c582-107">Ce didacticiel présente une application complète qui lit des vidéos à l’aide de MFPlay.</span><span class="sxs-lookup"><span data-stu-id="8c582-107">This tutorial presents a complete application that plays video using MFPlay.</span></span> <span data-ttu-id="8c582-108">Il est basé sur l’exemple du kit de développement logiciel (SDK) [SimplePlay](simpleplay-sample.md) .</span><span class="sxs-lookup"><span data-stu-id="8c582-108">It is based on the [SimplePlay](simpleplay-sample.md) SDK sample.</span></span>

<span data-ttu-id="8c582-109">Ce didacticiel contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c582-109">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="8c582-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c582-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8c582-111">Fichiers d’en-tête et de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c582-111">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="8c582-112">Variables globales</span><span class="sxs-lookup"><span data-stu-id="8c582-112">Global Variables</span></span>](#global-variables)
-   [<span data-ttu-id="8c582-113">Déclarer la classe de rappel</span><span class="sxs-lookup"><span data-stu-id="8c582-113">Declare the Callback Class</span></span>](#declare-the-callback-class)
-   [<span data-ttu-id="8c582-114">Déclarer la fonction SafeRelease</span><span class="sxs-lookup"><span data-stu-id="8c582-114">Declare the SafeRelease Function</span></span>](#declare-the-saferelease-function)
-   [<span data-ttu-id="8c582-115">Ouvrir un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="8c582-115">Open a Media File</span></span>](#open-a-media-file)
-   [<span data-ttu-id="8c582-116">Gestionnaires de messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="8c582-116">Window Message Handlers</span></span>](#window-message-handlers)
-   [<span data-ttu-id="8c582-117">Implémenter la méthode de rappel</span><span class="sxs-lookup"><span data-stu-id="8c582-117">Implement the Callback Method</span></span>](#implement-the-callback-method)
-   [<span data-ttu-id="8c582-118">Implémenter WinMain</span><span class="sxs-lookup"><span data-stu-id="8c582-118">Implement WinMain</span></span>](#implement-winmain)
-   [<span data-ttu-id="8c582-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c582-119">Related topics</span></span>](#related-topics)

<span data-ttu-id="8c582-120">Pour obtenir une présentation plus détaillée de l’API MFPlay, consultez [prise en main avec MFPlay](getting-started-with-mfplay.md).</span><span class="sxs-lookup"><span data-stu-id="8c582-120">For a more detailed discussion of the MFPlay API, see [Getting Started with MFPlay](getting-started-with-mfplay.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c582-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c582-121">Requirements</span></span>

<span data-ttu-id="8c582-122">MFPlay requiert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c582-122">MFPlay requires Windows 7.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="8c582-123">Fichiers d’en-tête et de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c582-123">Header and Library Files</span></span>

<span data-ttu-id="8c582-124">Incluez les fichiers d’en-tête suivants dans votre projet :</span><span class="sxs-lookup"><span data-stu-id="8c582-124">Include the following header files in your project:</span></span>


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



<span data-ttu-id="8c582-125">Lien vers les bibliothèques de code suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c582-125">Link to the following code libraries:</span></span>

-   <span data-ttu-id="8c582-126">mfplay. lib</span><span class="sxs-lookup"><span data-stu-id="8c582-126">mfplay.lib</span></span>
-   <span data-ttu-id="8c582-127">Shlwapi. lib</span><span class="sxs-lookup"><span data-stu-id="8c582-127">shlwapi.lib</span></span>

## <a name="global-variables"></a><span data-ttu-id="8c582-128">Variables globales</span><span class="sxs-lookup"><span data-stu-id="8c582-128">Global Variables</span></span>

<span data-ttu-id="8c582-129">Déclarez les variables globales suivantes :</span><span class="sxs-lookup"><span data-stu-id="8c582-129">Declare the following global variables:</span></span>


```C++
IMFPMediaPlayer         *g_pPlayer = NULL;      // The MFPlay player object.
MediaPlayerCallback     *g_pPlayerCB = NULL;    // Application callback object.

BOOL                    g_bHasVideo = FALSE;
```



<span data-ttu-id="8c582-130">Ces variables sont utilisées comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c582-130">These variables will be used as follows:</span></span>

<dl> <dt>

<span data-ttu-id="8c582-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*HWND de g \_*</span><span class="sxs-lookup"><span data-stu-id="8c582-131"><span id="g_hwnd"></span><span id="G_HWND"></span>*g\_hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="8c582-132">Handle de la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="8c582-132">A handle to the application window.</span></span>

</dd> <dt>

<span data-ttu-id="8c582-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*\_bVideo g*</span><span class="sxs-lookup"><span data-stu-id="8c582-133"><span id="g_bVideo"></span><span id="g_bvideo"></span><span id="G_BVIDEO"></span>*g\_bVideo*</span></span>
</dt> <dd>

<span data-ttu-id="8c582-134">Valeur booléenne qui effectue le suivi de la durée de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="8c582-134">A Boolean value that tracks whether video is playing.</span></span>

</dd> <dt>

<span data-ttu-id="8c582-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*\_pPlayer g*</span><span class="sxs-lookup"><span data-stu-id="8c582-135"><span id="g_pPlayer"></span><span id="g_pplayer"></span><span id="G_PPLAYER"></span>*g\_pPlayer*</span></span>
</dt> <dd>

<span data-ttu-id="8c582-136">Pointeur vers l’interface [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) .</span><span class="sxs-lookup"><span data-stu-id="8c582-136">A pointer to the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) interface.</span></span> <span data-ttu-id="8c582-137">Cette interface est utilisée pour contrôler la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c582-137">This interface is used to control playback.</span></span>

</dd> <dt>

<span data-ttu-id="8c582-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*\_pCallback g*</span><span class="sxs-lookup"><span data-stu-id="8c582-138"><span id="g_pCallback"></span><span id="g_pcallback"></span><span id="G_PCALLBACK"></span>*g\_pCallback*</span></span>
</dt> <dd>

<span data-ttu-id="8c582-139">Pointeur vers l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="8c582-139">A pointer to the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="8c582-140">L’application implémente cette interface de rappel pour recevoir des notifications de l’objet Player.</span><span class="sxs-lookup"><span data-stu-id="8c582-140">The application implements this callback interface to get notifications from the player object.</span></span>

</dd> </dl>

## <a name="declare-the-callback-class"></a><span data-ttu-id="8c582-141">Déclarer la classe de rappel</span><span class="sxs-lookup"><span data-stu-id="8c582-141">Declare the Callback Class</span></span>

<span data-ttu-id="8c582-142">Pour recevoir des notifications d’événements à partir de l’objet Player, l’application doit implémenter l’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="8c582-142">To get event notifications from the player object, the application must implement the [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface.</span></span> <span data-ttu-id="8c582-143">Le code suivant déclare une classe qui implémente l’interface.</span><span class="sxs-lookup"><span data-stu-id="8c582-143">The following code declares a class that implements the interface.</span></span> <span data-ttu-id="8c582-144">La seule variable membre est *m \_ cref*, qui stocke le nombre de références.</span><span class="sxs-lookup"><span data-stu-id="8c582-144">The only member variable is *m\_cRef*, which stores the reference count.</span></span>

<span data-ttu-id="8c582-145">Les méthodes **IUnknown** sont implémentées en ligne.</span><span class="sxs-lookup"><span data-stu-id="8c582-145">The **IUnknown** methods are implemented inline.</span></span> <span data-ttu-id="8c582-146">L’implémentation de la méthode [**IMFPMediaPlayerCallback :: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) est indiquée plus tard ; consultez [implémenter la méthode de rappel](#implement-the-callback-method).</span><span class="sxs-lookup"><span data-stu-id="8c582-146">The implementation of the [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is shown later; see [Implement the Callback Method](#implement-the-callback-method).</span></span>


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



## <a name="declare-the-saferelease-function"></a><span data-ttu-id="8c582-147">Déclarer la fonction SafeRelease</span><span class="sxs-lookup"><span data-stu-id="8c582-147">Declare the SafeRelease Function</span></span>

<span data-ttu-id="8c582-148">Tout au long de ce didacticiel, la fonction [SafeRelease](saferelease.md) est utilisée pour libérer des pointeurs d’interface :</span><span class="sxs-lookup"><span data-stu-id="8c582-148">Throughout this tutorial, the [SafeRelease](saferelease.md) function is used to release interface pointers:</span></span>


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



## <a name="open-a-media-file"></a><span data-ttu-id="8c582-149">Ouvrir un fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="8c582-149">Open a Media File</span></span>

<span data-ttu-id="8c582-150">La `PlayMediaFile` fonction ouvre un fichier multimédia, comme suit :</span><span class="sxs-lookup"><span data-stu-id="8c582-150">The `PlayMediaFile` function opens a media file, as follows:</span></span>

1.  <span data-ttu-id="8c582-151">Si *g \_ pPlayer* a la **valeur null**, la fonction appelle [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) pour créer une nouvelle instance de l’objet Media Player.</span><span class="sxs-lookup"><span data-stu-id="8c582-151">If *g\_pPlayer* is **NULL**, the function calls [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) to create a new instance of the media player object.</span></span> <span data-ttu-id="8c582-152">Les paramètres d’entrée de **MFPCreateMediaPlayer** incluent un pointeur vers l’interface de rappel et un handle vers la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="8c582-152">The input parameters to **MFPCreateMediaPlayer** include a pointer to the callback interface and a handle to the video window.</span></span>
2.  <span data-ttu-id="8c582-153">Pour ouvrir le fichier multimédia, la fonction appelle [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), en passant l’URL du fichier.</span><span class="sxs-lookup"><span data-stu-id="8c582-153">To open the media file, the function calls [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl), passing in the URL of the file.</span></span> <span data-ttu-id="8c582-154">Cette méthode se termine de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8c582-154">This method completes asynchronously.</span></span> <span data-ttu-id="8c582-155">Une fois l’opération terminée, la méthode [**IMFPMediaPlayerCallback :: OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) de l’application est appelée.</span><span class="sxs-lookup"><span data-stu-id="8c582-155">When it completes, the application's [**IMFPMediaPlayerCallback::OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent) method is called.</span></span>


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



<span data-ttu-id="8c582-156">La `OnFileOpen` fonction affiche la boîte de dialogue de fichier commune, qui permet à l’utilisateur de sélectionner un fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c582-156">The `OnFileOpen` function displays the common file dialog, which enables the user to select a file for playback.</span></span> <span data-ttu-id="8c582-157">L’interface **IFileOpenDialog** est utilisée pour afficher la boîte de dialogue de fichier commune.</span><span class="sxs-lookup"><span data-stu-id="8c582-157">The **IFileOpenDialog** interface is used to display the common file dialog.</span></span> <span data-ttu-id="8c582-158">Cette interface fait partie des API de l’interpréteur de commandes Windows. Il a été introduit dans Windows Vista en remplacement de l’ancienne fonction **GetOpenFileName** .</span><span class="sxs-lookup"><span data-stu-id="8c582-158">This interface is part of the Windows Shell APIs; it was introduced in Windows Vista as a replacement for the older **GetOpenFileName** function.</span></span> <span data-ttu-id="8c582-159">Une fois que l’utilisateur a sélectionné un fichier, `OnFileOpen` appelle `PlayMediaFile` pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c582-159">After the user selects a file, `OnFileOpen` calls `PlayMediaFile` to start playback.</span></span>


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



## <a name="window-message-handlers"></a><span data-ttu-id="8c582-160">Gestionnaires de messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="8c582-160">Window Message Handlers</span></span>

<span data-ttu-id="8c582-161">Ensuite, déclarez les gestionnaires de messages pour les messages de fenêtre suivants :</span><span class="sxs-lookup"><span data-stu-id="8c582-161">Next, declare message handlers for the following window messages:</span></span>

-   <span data-ttu-id="8c582-162">**\_peinture WM**</span><span class="sxs-lookup"><span data-stu-id="8c582-162">**WM\_PAINT**</span></span>
-   <span data-ttu-id="8c582-163">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="8c582-163">**WM\_SIZE**</span></span>
-   <span data-ttu-id="8c582-164">**\_Fermer WM**</span><span class="sxs-lookup"><span data-stu-id="8c582-164">**WM\_CLOSE**</span></span>

<span data-ttu-id="8c582-165">Pour le message **WM \_ Paint** , vous devez suivre si la vidéo est en cours de diffusion.</span><span class="sxs-lookup"><span data-stu-id="8c582-165">For the **WM\_PAINT** message, you must track whether video is currently playing.</span></span> <span data-ttu-id="8c582-166">Si c’est le cas, appelez la méthode [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) .</span><span class="sxs-lookup"><span data-stu-id="8c582-166">If so, call the [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo) method.</span></span> <span data-ttu-id="8c582-167">Cette méthode fait en sorte que l’objet Player redessine la trame vidéo la plus récente.</span><span class="sxs-lookup"><span data-stu-id="8c582-167">This method causes the player object to redraw the most recent video frame.</span></span>

<span data-ttu-id="8c582-168">S’il n’y a pas de vidéo, l’application est chargée de peindre la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c582-168">If there is no video, the application is responsible for painting the window.</span></span> <span data-ttu-id="8c582-169">Pour ce didacticiel, l’application appelle simplement la fonction GDI **fillRect** pour remplir toute la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="8c582-169">For this tutorial, the application simply calls the GDI **FillRect** function to fill the entire client area.</span></span>


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



<span data-ttu-id="8c582-170">Pour le message de **\_ taille WM** , appelez [**IMFPMediaPlayer :: UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span><span class="sxs-lookup"><span data-stu-id="8c582-170">For the **WM\_SIZE** message, call [**IMFPMediaPlayer::UpdateVideo**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo).</span></span> <span data-ttu-id="8c582-171">Cette méthode fait en sorte que l’objet Player réajuste la vidéo pour qu’elle corresponde à la taille actuelle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c582-171">This method causes the player object to readjust the video to match the current size of the window.</span></span> <span data-ttu-id="8c582-172">Notez que **UpdateVideo** est utilisé à la fois pour la **\_ peinture WM** et pour la **\_ taille WM**.</span><span class="sxs-lookup"><span data-stu-id="8c582-172">Note that **UpdateVideo** is used for both **WM\_PAINT** and **WM\_SIZE**.</span></span>


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



<span data-ttu-id="8c582-173">Pour le message **WM \_ Close** , libérez les pointeurs [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) et [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) .</span><span class="sxs-lookup"><span data-stu-id="8c582-173">For the **WM\_CLOSE** message, release the [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer) and [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) pointers.</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    SafeRelease(&g_pPlayer);
    SafeRelease(&g_pPlayerCB);
    PostQuitMessage(0);
}
```



## <a name="implement-the-callback-method"></a><span data-ttu-id="8c582-174">Implémenter la méthode de rappel</span><span class="sxs-lookup"><span data-stu-id="8c582-174">Implement the Callback Method</span></span>

<span data-ttu-id="8c582-175">L’interface [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) définit une méthode unique, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span><span class="sxs-lookup"><span data-stu-id="8c582-175">The [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback) interface defines a single method, [**OnMediaPlayerEvent**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent).</span></span> <span data-ttu-id="8c582-176">Cette méthode avertit l’application chaque fois qu’un événement se produit pendant la lecture.</span><span class="sxs-lookup"><span data-stu-id="8c582-176">This method notifies the application whenever an event occurs during playback.</span></span> <span data-ttu-id="8c582-177">La méthode accepte un paramètre, un pointeur vers une structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) .</span><span class="sxs-lookup"><span data-stu-id="8c582-177">The method takes one parameter, a pointer to an [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure.</span></span> <span data-ttu-id="8c582-178">Le membre **eEventType** de la structure spécifie l’événement qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="8c582-178">The **eEventType** member of the structure specifies the event that occurred.</span></span>

<span data-ttu-id="8c582-179">La structure d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) peut être suivie de données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8c582-179">The [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) structure may be followed by additional data.</span></span> <span data-ttu-id="8c582-180">Pour chaque type d’événement, une macro est définie et effectue un cast du pointeur d' **\_ \_ en-tête d’événement MFP** vers une structure spécifique à un événement.</span><span class="sxs-lookup"><span data-stu-id="8c582-180">For each event type, a macro is defined that casts the **MFP\_EVENT\_HEADER** pointer to an event-specific structure.</span></span> <span data-ttu-id="8c582-181">(Voir [**\_ \_ type d’événement MFP**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span><span class="sxs-lookup"><span data-stu-id="8c582-181">(See [**MFP\_EVENT\_TYPE**](/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type).)</span></span>

<span data-ttu-id="8c582-182">Pour ce didacticiel, deux événements sont significatifs :</span><span class="sxs-lookup"><span data-stu-id="8c582-182">For this tutorial, two events are significant:</span></span>



| <span data-ttu-id="8c582-183">Événement</span><span class="sxs-lookup"><span data-stu-id="8c582-183">Event</span></span>                                    | <span data-ttu-id="8c582-184">Description</span><span class="sxs-lookup"><span data-stu-id="8c582-184">Description</span></span>                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c582-185">**\_type d’événement MFP \_ \_ MEDIAITEM \_ créé**</span><span class="sxs-lookup"><span data-stu-id="8c582-185">**MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED**</span></span> | <span data-ttu-id="8c582-186">Envoyé lorsque le [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) est terminé.</span><span class="sxs-lookup"><span data-stu-id="8c582-186">Sent when the [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) completes.</span></span> |
| <span data-ttu-id="8c582-187">**\_type d’événement MFP \_ \_ MEDIAITEM \_ Set**</span><span class="sxs-lookup"><span data-stu-id="8c582-187">**MFP\_EVENT\_TYPE\_MEDIAITEM\_SET**</span></span>     | <span data-ttu-id="8c582-188">Envoyé lorsque [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) est terminé.</span><span class="sxs-lookup"><span data-stu-id="8c582-188">Sent when [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) completes.</span></span>                         |



 

<span data-ttu-id="8c582-189">Le code suivant montre comment effectuer un cast du pointeur d' [**\_ \_ en-tête d’événement MFP**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) vers la structure spécifique à l’événement.</span><span class="sxs-lookup"><span data-stu-id="8c582-189">The following code shows how to cast the [**MFP\_EVENT\_HEADER**](/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header) pointer to the event-specific structure.</span></span>


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



<span data-ttu-id="8c582-190">L’événement de **\_ type d’événement MFP \_ \_ MEDIAITEM \_ créé** informe l’application que la méthode [**IMFPMediaPlayer :: CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) est terminée.</span><span class="sxs-lookup"><span data-stu-id="8c582-190">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event notifies the application that the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method has completed.</span></span> <span data-ttu-id="8c582-191">La structure d’événement contient un pointeur vers l’interface [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) , qui représente l’élément multimédia créé à partir de l’URL.</span><span class="sxs-lookup"><span data-stu-id="8c582-191">The event structure contains a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface, which represents the media item created from the URL.</span></span> <span data-ttu-id="8c582-192">Pour effectuer la mise en file d’attente de l’élément pour la lecture, transmettez ce pointeur à la méthode [**IMFPMediaPlayer :: SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) :</span><span class="sxs-lookup"><span data-stu-id="8c582-192">To queue the item for playback, pass this pointer to the [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method:</span></span>


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



<span data-ttu-id="8c582-193">Le **\_ type d’événement MFP \_ \_ MEDIAITEM \_ Set** Event informe l’application que [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) est terminée.</span><span class="sxs-lookup"><span data-stu-id="8c582-193">The **MFP\_EVENT\_TYPE\_MEDIAITEM\_SET** event notifies the application that [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) has completed.</span></span> <span data-ttu-id="8c582-194">Appeler [**IMFPMediaPlayer ::P poser**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) pour démarrer la lecture :</span><span class="sxs-lookup"><span data-stu-id="8c582-194">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback:</span></span>


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



## <a name="implement-winmain"></a><span data-ttu-id="8c582-195">Implémenter WinMain</span><span class="sxs-lookup"><span data-stu-id="8c582-195">Implement WinMain</span></span>

<span data-ttu-id="8c582-196">Dans le reste de ce didacticiel, il n’y a aucun appel à Media Foundation API.</span><span class="sxs-lookup"><span data-stu-id="8c582-196">In the remainder of this tutorial, there are no calls to Media Foundation APIs.</span></span> <span data-ttu-id="8c582-197">Le code suivant illustre la procédure de fenêtre :</span><span class="sxs-lookup"><span data-stu-id="8c582-197">The following code shows the window procedure:</span></span>


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



<span data-ttu-id="8c582-198">La `InitializeWindow` fonction enregistre la classe de fenêtre de l’application et crée la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="8c582-198">The `InitializeWindow` function registers the application's window class and creates the window.</span></span>


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



<span data-ttu-id="8c582-199">Enfin, implémentez le point d’entrée de l’application :</span><span class="sxs-lookup"><span data-stu-id="8c582-199">Finally, implement the application entry point:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8c582-200">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c582-200">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c582-201">Utilisation de MFPlay pour la lecture audio/vidéo</span><span class="sxs-lookup"><span data-stu-id="8c582-201">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



