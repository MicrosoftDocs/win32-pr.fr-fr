---
description: Écriture du fichier
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Écriture du fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cabb5575f371c6525e58cc8ede7d05c2701acc31be325af46e3b00e6e2d8d20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051398"
---
# <a name="writing-the-file"></a>Écriture du fichier

Pour écrire le fichier, il vous suffit d’exécuter le graphique de filtre en appelant la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Attendez la fin de la lecture et arrêtez explicitement le graphique en appelant [**IMediaControl :: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); dans le cas contraire, le fichier n’est pas écrit correctement.

Pour afficher la progression de l’opération d’écriture de fichiers, interrogez le filtre MUX pour l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Appelez la méthode [**IMediaSeeking :: GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) pour récupérer la durée du fichier. Périodiquement, lorsque le graphique est en cours d’exécution, appelez la méthode [**IMediaSeeking :: getCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) pour récupérer la position actuelle du graphique dans le flux. La position actuelle divisée par la durée indique que le pourcentage est terminé.

> [!Note]  
> une application interroge généralement le gestionnaire de Graph de filtre pour **IMediaSeeking**, mais l’écriture de fichier est une exception à cette règle. le gestionnaire de Graph de filtre calcule la position actuelle à partir de la position de départ et la durée d’exécution du graphique, ce qui est précis pour la lecture de fichier, mais pas pour l’écriture de fichier. Par conséquent, pour obtenir un résultat précis, vous devez récupérer la position à partir du filtre MUX.

 

Le code suivant permet d’obtenir la durée du fichier, de démarrer un minuteur pour mettre à jour l’interface utilisateur de l’application et d’exécuter le graphique de filtre. (La vérification des erreurs est omise par souci de clarté.)


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



Lorsque l’application reçoit un événement de minuteur, elle peut mettre à jour l’interface utilisateur avec la position actuelle :


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



lorsque l’application reçoit un événement d’achèvement DirectShow, elle doit arrêter le graphique, comme illustré dans le code suivant :


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



 

 



