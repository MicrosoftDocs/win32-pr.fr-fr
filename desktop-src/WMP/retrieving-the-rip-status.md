---
title: Récupération de l’État RIP
description: Récupération de l’État RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Lecteur Windows Media, extraction de CD
- Modèle d’objet du lecteur Windows Media, extraction de CD
- modèle d’objet, extraction de CD
- Contrôle Windows Media Player ActiveX, extraction de CD
- Contrôle ActiveX, extraction de CD
- Windows Media Player Mobile contrôle ActiveX, extraction de CD
- Windows Media Player Mobile, extraction de CD
- Extraction de CD, récupération de l’État RIP
- extraction de CD, récupération de l’État RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030844"
---
# <a name="retrieving-the-rip-status"></a>Récupération de l’État RIP

Vous pouvez surveiller la progression de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Cette méthode récupère une valeur de progression pour l’opération d’extraction entière. La valeur récupérée est un nombre qui représente le pourcentage d’extraction terminé, de 0 à 100.

La valeur de progression représente le pourcentage terminé de l’ensemble du processus d’extraction. Pour déterminer la progression d’une piste spécifique, utilisez [IWMPMedia :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) avec « RipProgress » comme nom d’attribut. Pour déterminer l’index de la piste actuellement extraite, appelez **IWMPPlaylist :: getItemInfo** avec « CurrentRipTrackIndex » comme nom d’attribut.

Vous pouvez surveiller l’état de l’opération d’extraction en appelant périodiquement [IWMPCdromRip :: obten \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Cette méthode récupère une valeur d’énumération [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) qui indique si l’opération est en cours ou arrêtée. Vous pouvez également surveiller l’état de l’opération d’extraction en gérant l’événement [IWMPEvents3 :: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . (Consultez [gestion des événements en C++](handling-events-in-c.md).) Veillez à comparer le pointeur **IWMPCdromRip** (fourni par l’événement) au pointeur qui représente votre opération d’extraction, pour vous assurer que l’événement a été déclenché par votre opération.

L’exemple de code suivant montre comment utiliser ces fonctions pour récupérer l’état d’une opération d’extraction.

Les contrôles de boîte de dialogue suivants sont définis pour l’exemple de code.



| ID du contrôle                   | Description                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_suivi actuel \_ IDC          | Texte statique qui représente l’index de la piste actuellement extraite.                                         |
| IDC \_ suivre \_ le \_ texte de progression   | Texte statique qui représente la progression de la piste en cours d’extraction en tant que pourcentage.                      |
| \_suivi de progression IDC \_         | Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression de la piste en cours d’extraction en tant que pourcentage. |
| \_texte de \_ progression \_ général IDC | Texte statique qui représente la progression du processus d’extraction total sous la forme d’un pourcentage.                             |
| \_progression IDC \_ globale       | Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression du processus d’extraction total sous la forme d’un pourcentage.        |
| \_État RIP \_ IDC              | Texte statique qui affiche l’opération en cours d’exécution (« extraction », « arrêt » ou « inconnu »)             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extraction d’un CD**](ripping-a-cd.md)
</dt> <dt>

[**Récupération de l’interface d’extraction**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Démarrage du processus RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Sélection d’éléments pour l’extraction**](selecting-items-for-ripping.md)
</dt> </dl>

 

 




