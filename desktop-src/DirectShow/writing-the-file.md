---
description: Écriture du fichier
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Écriture du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521446"
---
# <a name="writing-the-file"></a><span data-ttu-id="93c94-103">Écriture du fichier</span><span class="sxs-lookup"><span data-stu-id="93c94-103">Writing the File</span></span>

<span data-ttu-id="93c94-104">Pour écrire le fichier, il vous suffit d’exécuter le graphique de filtre en appelant la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) .</span><span class="sxs-lookup"><span data-stu-id="93c94-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="93c94-105">Attendez la fin de la lecture et arrêtez explicitement le graphique en appelant [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); dans le cas contraire, le fichier n’est pas écrit correctement.</span><span class="sxs-lookup"><span data-stu-id="93c94-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="93c94-106">Pour afficher la progression de l’opération d’écriture de fichiers, interrogez le filtre MUX pour l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="93c94-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="93c94-107">Appelez la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) pour récupérer la durée du fichier.</span><span class="sxs-lookup"><span data-stu-id="93c94-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="93c94-108">Périodiquement, lorsque le graphique est en cours d’exécution, appelez la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) pour récupérer la position actuelle du graphique dans le flux.</span><span class="sxs-lookup"><span data-stu-id="93c94-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="93c94-109">La position actuelle divisée par la durée indique que le pourcentage est terminé.</span><span class="sxs-lookup"><span data-stu-id="93c94-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="93c94-110">Une application interroge généralement le gestionnaire de graphique de filtre pour **IMediaSeeking**, mais l’écriture de fichier est une exception à cette règle.</span><span class="sxs-lookup"><span data-stu-id="93c94-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="93c94-111">Le gestionnaire de graphes de filtres calcule la position actuelle à partir de la position de départ et la durée d’exécution du graphique, ce qui est précis pour la lecture de fichier, mais pas pour l’écriture de fichier.</span><span class="sxs-lookup"><span data-stu-id="93c94-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="93c94-112">Par conséquent, pour obtenir un résultat précis, vous devez récupérer la position à partir du filtre MUX.</span><span class="sxs-lookup"><span data-stu-id="93c94-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="93c94-113">Le code suivant permet d’obtenir la durée du fichier, de démarrer un minuteur pour mettre à jour l’interface utilisateur de l’application et d’exécuter le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="93c94-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="93c94-114">(La vérification des erreurs est omise par souci de clarté.)</span><span class="sxs-lookup"><span data-stu-id="93c94-114">(Error checking is omitted for clarity.)</span></span>


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



<span data-ttu-id="93c94-115">Lorsque l’application reçoit un événement de minuteur, elle peut mettre à jour l’interface utilisateur avec la position actuelle :</span><span class="sxs-lookup"><span data-stu-id="93c94-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



<span data-ttu-id="93c94-116">Lorsque l’application reçoit un événement d’achèvement DirectShow, elle doit arrêter le graphique, comme illustré dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="93c94-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



