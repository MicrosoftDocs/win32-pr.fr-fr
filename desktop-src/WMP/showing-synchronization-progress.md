---
title: Indication de la progression de la synchronisation
description: Indication de la progression de la synchronisation
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Lecteur Windows Media, appareils mobiles
- Modèle objet du lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- Contrôle ActiveX du lecteur Windows Media, appareils mobiles
- Contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile contrôle ActiveX, appareils mobiles
- Windows Media Player Mobile, appareils mobiles
- périphériques portables, progression de la synchronisation
- synchronisation de l’appareil, indication de la progression
- synchronisation des appareils, indication de la progression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f109f09d4efacef620a2c21691f50cc0ac2143
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103841897"
---
# <a name="showing-synchronization-progress"></a><span data-ttu-id="da206-113">Indication de la progression de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="da206-113">Showing Synchronization Progress</span></span>

<span data-ttu-id="da206-114">Vous pouvez afficher la progression de la synchronisation pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da206-114">You can display synchronization progress to the user.</span></span> <span data-ttu-id="da206-115">L’exemple de code suivant montre comment créer un minuteur pour récupérer périodiquement la valeur actuelle de progression à l’aide de **IWMPSyncDevice :: obtenir la \_ progression**.</span><span class="sxs-lookup"><span data-stu-id="da206-115">The following example code shows how to create a timer to periodically retrieve the current progress value by using **IWMPSyncDevice::get\_progress**.</span></span> <span data-ttu-id="da206-116">Notez que la valeur de progression Récupérée représente la progression de la totalité de l’opération de synchronisation pour chaque appareil.</span><span class="sxs-lookup"><span data-stu-id="da206-116">Note that the progress value retrieved represents the progress for the entire synchronization operation for each device.</span></span> <span data-ttu-id="da206-117">La récupération de la progression de la synchronisation pour des éléments multimédias individuels n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="da206-117">Retrieving synchronization progress for individual media items is not supported.</span></span>

<span data-ttu-id="da206-118">Pour déterminer quand démarrer ou arrêter le minuteur, gérez l’événement **DeviceSyncStateChange** .</span><span class="sxs-lookup"><span data-stu-id="da206-118">To determine when to start or stop the timer, handle the **DeviceSyncStateChange** event.</span></span> <span data-ttu-id="da206-119">L’exemple de fonction suivant illustre ce type de gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="da206-119">The following example function demonstrates such an event handler.</span></span> <span data-ttu-id="da206-120">Le code affiche également l’état de synchronisation actuel sous la forme d’une chaîne de texte à l’aide d’un contrôle de texte statique nommé IDC \_ SYNCSTATE.</span><span class="sxs-lookup"><span data-stu-id="da206-120">The code also displays the current synchronization state as a text string using a static text control, named IDC\_SYNCSTATE.</span></span>


```C++
void CMainDlg::DeviceSyncStateChange( IWMPSyncDevice * pDevice, WMPSyncState NewState )
{
    if(NULL == pDevice)
    {
        return;
    }

    HRESULT hr = E_POINTER;
    VARIANT_BOOL  vbIdentical = VARIANT_FALSE;
    // Window handle for static text control that shows the sync state.
    HWND hwndSyncStateText = GetDlgItem(IDC_SYNCSTATE); 

    // Strings to show sync state.
    const TCHAR *szSyncState[3] = {
    _T("Unknown"),
    _T("Synchronizing"),
    _T("Stopped")};

    // Get a pointer to the device the user selected in the list box.    
    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[GetSelectedDeviceIndex()]); 
    // Cache the pointer to the device that raised the event.
    CComPtr<IWMPSyncDevice> spDeviceParam(pDevice); 

    if(spDevice.p)
    {
        // Test whether the device that raised the event is the same as 
        // the one the user selected.
        hr = spDevice->isIdentical(spDeviceParam, &vbIdentical);
    }

    if(SUCCEEDED(hr) &&
        vbIdentical == VARIANT_TRUE)
    {    
        // Display the sync state.
        SendMessage(hwndSyncStateText, WM_SETTEXT, 0, (LPARAM)szSyncState[NewState]);

        switch(NewState)
        {
        case wmpssSynchronizing:
            // Start the progress timer.
            SetTimer(1, 1000, NULL);
            SetUIState(Synchronizing, TRUE);
            break;
        case wmpssStopped:
            // Stop the progress timer.
            KillTimer(1);
            // Make sure the final progress is displayed.            
            ShowProgress(GetSelectedDeviceIndex());
            SetUIState(Partnership, TRUE);
            break;      
        default:
            break;
        }
    }    
}
```



<span data-ttu-id="da206-121">Lorsque le minuteur est en cours d’exécution, il envoie un \_ message de minuteur WM à intervalles d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="da206-121">When the timer is running, it sends a WM\_TIMER message at one-second intervals.</span></span> <span data-ttu-id="da206-122">L’application gère le \_ minuteur WM dans sa boucle de message.</span><span class="sxs-lookup"><span data-stu-id="da206-122">The application handles WM\_TIMER in its message loop.</span></span>

<span data-ttu-id="da206-123">L’exemple de fonction suivant montre comment afficher la progression à l’aide d’un contrôle de texte statique (IDC \_ PROGSTATIC) et à l’aide d’un contrôle Progress (IDC \_ SYNCPROG).</span><span class="sxs-lookup"><span data-stu-id="da206-123">The following example function demonstrates how to show progress by using both a static text control (IDC\_PROGSTATIC), and using a progress control (IDC\_SYNCPROG).</span></span> <span data-ttu-id="da206-124">Appelez cette fonction en réponse au message du \_ minuteur WM et à l’achèvement du processus de synchronisation, comme indiqué dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="da206-124">Call this function in response to the WM\_TIMER message and upon completion of the synchronization process, as shown in the preceding example.</span></span>


```C++
STDMETHODIMP CMainDlg::ShowProgress(long lIndex)
{  
    ATLASSERT(m_ppWMPDevices);

    long lProgress = 0;
    WCHAR buffer[10]; // Buffer larger than needed to hold progress string.
    ZeroMemory(buffer, sizeof WCHAR * 10);

    // Retrieve a handle to the progress control
    HWND  hwndSyncProgressCtl = GetDlgItem(IDC_SYNCPROG); 
    // Retrieve a handle to the static control that displays 
    // progress as text.
    HWND  hwndSyncProgressText = GetDlgItem(IDC_PROGSTATIC); 

    CComPtr<IWMPSyncDevice> spDevice(m_ppWMPDevices[lIndex]);
    
    HRESULT hr = spDevice->get_progress(&lProgress);

    // Convert progress to a string and add the percent character.
    _ltow(lProgress, buffer, 10);
    CComBSTR bstrProgress(buffer);
    bstrProgress += " %";

    // Display the text.
    ::SendMessage(hwndSyncProgressText, WM_SETTEXT, 0, (LPARAM)(LPCTSTR)COLE2T(bstrProgress));
    // Set the progress control position.
    ::SendMessage(hwndSyncProgressCtl, PBM_SETPOS, (WPARAM)(int)lProgress, 0);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="da206-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="da206-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da206-126">**Énumération des appareils**</span><span class="sxs-lookup"><span data-stu-id="da206-126">**Enumerating Devices**</span></span>](enumerating-devices.md)
</dt> <dt>

[<span data-ttu-id="da206-127">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="da206-127">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[<span data-ttu-id="da206-128">**IWMPSyncDevice :: obtient la \_ progression**</span><span class="sxs-lookup"><span data-stu-id="da206-128">**IWMPSyncDevice::get\_progress**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[<span data-ttu-id="da206-129">**IWMPSyncDevice::isIdentical**</span><span class="sxs-lookup"><span data-stu-id="da206-129">**IWMPSyncDevice::isIdentical**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[<span data-ttu-id="da206-130">**Utilisation d’appareils mobiles**</span><span class="sxs-lookup"><span data-stu-id="da206-130">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




