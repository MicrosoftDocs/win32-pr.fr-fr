---
title: Bloc-notes Windows Touch utilisant l’exemple de stylet en temps réel (C++)
description: Consultez un exemple C++ de bloc-notes Windows Touch (MTScratchpadRTStylus), qui montre comment utiliser des messages tactiles Windows pour dessiner des traces des points tactiles dans une fenêtre.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch, exemples de code
- Tactile Windows, exemple de code
- Exemples tactiles Windows, bloc-notes
- Exemples de bloc-notes
- Interface tactile Windows, objet de stylet (RTS) en temps réel
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 42e32e66942f3dcfad11b8b777e846e0cee6c0b3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406292"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="25444-108">Bloc-notes Windows Touch utilisant l’exemple de stylet en temps réel (C++)</span><span class="sxs-lookup"><span data-stu-id="25444-108">Windows Touch Scratchpad using the Real-time Stylus Sample (C++)</span></span>

<span data-ttu-id="25444-109">L’exemple du bloc-notes Windows Touch ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) montre comment utiliser des messages tactiles Windows pour dessiner les traces des points tactiles dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="25444-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="25444-110">Le suivi du doigt principal, celui qui a été placé en premier dans le digitaliseur, est dessiné en noir.</span><span class="sxs-lookup"><span data-stu-id="25444-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="25444-111">Les doigts secondaires sont dessinés dans six autres couleurs : rouge, vert, bleu, cyan, magenta et jaune.</span><span class="sxs-lookup"><span data-stu-id="25444-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta, and yellow.</span></span> <span data-ttu-id="25444-112">La capture d’écran suivante montre comment l’application peut se présenter lors de son exécution.</span><span class="sxs-lookup"><span data-stu-id="25444-112">The following screen shot shows how the application could look while running.</span></span>

![capture d’écran montrant l’exemple de bloc-notes tactile Windows utilisant le stylet en temps réel, avec un vert, un rouge, trois noirs et une ligne bleue à l’écran](images/mtscratchpadrtstylus.png)

<span data-ttu-id="25444-114">Pour cet exemple, l’objet de stylet (RTS) en temps réel est créé et la prise en charge de plusieurs points de contact est activée.</span><span class="sxs-lookup"><span data-stu-id="25444-114">For this sample, the Real-time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="25444-115">Un plug-in DynamicRenderer est ajouté au RTS pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="25444-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="25444-116">Un plug-in, **CSyncEventHandlerRTS**, est implémenté pour effectuer le suivi du nombre de doigts et pour modifier la couleur de dessin du convertisseur dynamique.</span><span class="sxs-lookup"><span data-stu-id="25444-116">A plug-in, **CSyncEventHandlerRTS**, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="25444-117">Avec les deux plug-ins dans la pile de plug-in RTS, l’application Windows Touch du bloc-notes affiche le contact principal en noir et le reste des contacts dans les différentes couleurs.</span><span class="sxs-lookup"><span data-stu-id="25444-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="25444-118">Le code suivant illustre la création de l’objet RTS avec prise en charge de plusieurs points de contact.</span><span class="sxs-lookup"><span data-stu-id="25444-118">The following code shows how the RTS object is created with support for multiple contact points.</span></span>

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

<span data-ttu-id="25444-119">Le code suivant montre comment le plug-in de rendu dynamique est créé et ajouté au RTS.</span><span class="sxs-lookup"><span data-stu-id="25444-119">The following code shows how the dynamic renderer plug-in is created and added to the RTS.</span></span>

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

<span data-ttu-id="25444-120">Le code suivant modifie la couleur de trait du stylet du gestionnaire d’événements **StylusDown** dans le **CSyncEventHandlerRTS**, un plug-in RTS personnalisé.</span><span class="sxs-lookup"><span data-stu-id="25444-120">The following code changes the stylus stroke color for the **StylusDown** event handler in the **CSyncEventHandlerRTS**, a custom RTS plug-in.</span></span>

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

<span data-ttu-id="25444-121">Lorsque la valeur *m_nContacts* est incrémentée, elle modifie le jeu de couleurs dans le convertisseur dynamique.</span><span class="sxs-lookup"><span data-stu-id="25444-121">When the *m_nContacts* value is incremented, it will change the color set in the dynamic renderer.</span></span> <span data-ttu-id="25444-122">Les traits qui ne sont pas le contact principal sont dessinés avec des couleurs différentes.</span><span class="sxs-lookup"><span data-stu-id="25444-122">Strokes that are not the primary contact will be drawn with different colors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25444-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="25444-123">Related topics</span></span>

<span data-ttu-id="25444-124">[Application multipoint de bloc-notes (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [application de bloc-notes multipoint (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [exemples de fonctions tactiles Windows](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="25444-124">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
