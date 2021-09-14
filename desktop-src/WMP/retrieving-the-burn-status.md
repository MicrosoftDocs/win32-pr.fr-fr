---
title: Récupération de l’état d’avancement
description: Récupération de l’état d’avancement
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Lecteur Windows Media, gravage de CD
- modèle d’objet Lecteur Windows Media, gravage de CD
- modèle d’objet, gravage de CD
- contrôle de ActiveX Lecteur Windows Media, gravure de CD
- contrôle de ActiveX, gravure de CD
- Lecteur Windows Media contrôle de ActiveX Mobile, gravage de CD
- Lecteur Windows Media Mobile, gravage de CD
- Gravage de CD, récupération de l’état de gravure
- gravure de CD, récupération de l’état d’avancement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010896"
---
# <a name="retrieving-the-burn-status"></a>Récupération de l’état d’avancement

Dans l’exemple de code qui suit, les contrôles de boîte de dialogue suivants sont définis :



| ID du contrôle           | Description                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| \_État de gravure IDC \_     | Texte statique qui représente l’état de l’opération de gravure de CD.             |
| progression d’IDC \_        | Barre de progression avec une plage comprise entre 0 et 100 qui représente la progression totale de la gravure. |
| \_texte de progression IDC \_  | Texte statique qui représente la progression totale de la gravure sous la forme d’un nombre compris entre 0 et 100. |
| \_heure disponible d’IDC \_ | Texte statique pour afficher l’heure disponible sur le CD, en secondes.               |
| \_espace libre \_ IDC     | Texte statique pour afficher l’espace libre sur le CD, en octets.                     |
| \_espace total \_ IDC    | Texte statique pour afficher la capacité totale du CD, en octets.                 |



 

Vous pouvez surveiller la progression de l’opération de gravure en appelant régulièrement [IWMPCdromBurn :: obten \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) pendant la gravure du CD. Cette méthode récupère une valeur de progression pour l’ensemble de l’opération de gravure. La valeur récupérée est un nombre qui représente le pourcentage de brûlures terminées, de 0 à 100.


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



Vous pouvez récupérer l’état actuel de l’opération de gravure en appelant [IWMPCdromBurn :: obten \_ burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate). Cette méthode récupère une énumération spécifiant l’opération en cours d’exécution.


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



Pour récupérer le nombre de secondes que le CD peut contenir, appelez [IWMPCdromBurn :: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) avec « AvailableTime » comme premier paramètre. La valeur récupérée par cette fonction est représentée par une chaîne.


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



Pour récupérer la quantité d’espace libre sur un disque, appelez **IWMPCdromBurn :: getItemInfo** avec « FreeSpace » comme premier paramètre. La valeur récupérée par cette fonction est une chaîne qui représente le nombre d’octets libres disponibles sur le disque.


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



Pour récupérer la capacité totale d’un disque, appelez **IWMPCdromBurn :: getItemInfo** avec « TotalSpace » comme premier paramètre. La valeur récupérée par cette fonction est une chaîne qui correspond au nombre total d’octets sur le disque.


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gravure d’un CD**](burning-a-cd.md)
</dt> <dt>

[**Récupération de l’interface de gravure de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Démarrage du processus de gravure**](starting-the-burn-process.md)
</dt> <dt>

[**Effacement d’un CD réinscriptible**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Récupération de l’état du lecteur et du disque**](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




