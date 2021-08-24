---
title: Indication de la progression de la synchronisation
description: Indication de la progression de la synchronisation
ms.assetid: 5ca4d6ae-822e-4ddc-950d-cf7df6889108
keywords:
- Lecteur Windows Media, appareils mobiles
- modèle objet Lecteur Windows Media, appareils mobiles
- modèle objet, appareils mobiles
- contrôle de ActiveX Lecteur Windows Media, appareils mobiles
- contrôle de ActiveX, appareils mobiles
- Lecteur Windows Media contrôle Mobile ActiveX, appareils mobiles
- Lecteur Windows Media Mobile, appareils mobiles
- périphériques portables, progression de la synchronisation
- synchronisation de l’appareil, indication de la progression
- synchronisation des appareils, indication de la progression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6126bff5f96aa9b18c1729d0da12b05a73da6eb43dd63d8135baf0544e19ada5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833290"
---
# <a name="showing-synchronization-progress"></a>Indication de la progression de la synchronisation

Vous pouvez afficher la progression de la synchronisation pour l’utilisateur. L’exemple de code suivant montre comment créer un minuteur pour récupérer périodiquement la valeur actuelle de progression à l’aide de **IWMPSyncDevice :: obtenir la \_ progression**. Notez que la valeur de progression Récupérée représente la progression de la totalité de l’opération de synchronisation pour chaque appareil. La récupération de la progression de la synchronisation pour des éléments multimédias individuels n’est pas prise en charge.

Pour déterminer quand démarrer ou arrêter le minuteur, gérez l’événement **DeviceSyncStateChange** . L’exemple de fonction suivant illustre ce type de gestionnaire d’événements. Le code affiche également l’état de synchronisation actuel sous la forme d’une chaîne de texte à l’aide d’un contrôle de texte statique nommé IDC \_ SYNCSTATE.


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



Lorsque le minuteur est en cours d’exécution, il envoie un \_ message de minuteur WM à intervalles d’une seconde. L’application gère le \_ minuteur WM dans sa boucle de message.

L’exemple de fonction suivant montre comment afficher la progression à l’aide d’un contrôle de texte statique (IDC \_ PROGSTATIC) et à l’aide d’un contrôle Progress (IDC \_ SYNCPROG). Appelez cette fonction en réponse au message du \_ minuteur WM et à l’achèvement du processus de synchronisation, comme indiqué dans l’exemple précédent.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Énumération des appareils**](enumerating-devices.md)
</dt> <dt>

[**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**IWMPSyncDevice :: obtient la \_ progression**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_progress)
</dt> <dt>

[**IWMPSyncDevice::isIdentical**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




